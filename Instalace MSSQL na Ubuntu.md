# Instalace MSSQL na Ubuntu
https://learn.microsoft.com/en-us/sql/linux/sql-server-linux-setup?view=sql-server-ver16

1. MSSQL není standardní package pro Ubuntu, tak je potřeba přidat MS repository:
```shell
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
sudo add-apt-repository "$(wget -qO- https://packages.microsoft.com/config/ubuntu/20.04/mssql-server-2019.list)"
```
2. Teď můžu nainstalovat MSSQL:
```shell
sudo apt-get update
sudo apt-get install -y mssql-server
```
3. Když mám nainstalováno, musím nakonfigurovat:
```shell
sudo /opt/mssql/bin/mssql-conf setup
```
tady je potřeba zadat edici (asi Developer ne?) a heslo pro **sa**.

4. Nastavit správnou timezone:
```shell
sudo dpkg-reconfigure tzdata
```
a následovat nastavení, co se objevuje na terminálu.

5. Instalace command-line nástrojů
```shell
sudo apt-get update 
sudo apt install curl
curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
curl https://packages.microsoft.com/config/ubuntu/20.04/prod.list | sudo tee /etc/apt/sources.list.d/msprod.list
sudo apt-get update 
sudo apt-get install mssql-tools unixodbc-dev
echo 'export PATH="$PATH:/opt/mssql-tools/bin"' >> ~/.bash_profile
echo 'export PATH="$PATH:/opt/mssql-tools/bin"' >> ~/.bashrc
source ~/.bashrc
```

6. Nastavit jinej port pro MSSQL, např. **5050**
```shell
sudo /opt/mssql/bin/mssql-conf set network.tcpport 5050
sudo systemctl restart mssql-server
```
tak třeba tuto se mi ještě nepovedlo rozchodit. Pořád jedu přes 1433.

7. Vytvořit nové adresáře pro datové soubory, logy, atd. Vytvářím na disku ```/datadrive```
```shell
sudo mkdir /datadrive/SQLDATA
sudo chown mssql:mssql /datadrive/SQLDATA
```
a takhle si vytvořím všechny adresáře pro data `SQLDATA`, logy `SQLLOGS`, zálohy `backups`, dumpy `dumps` a soubory logů `logs`

8. Nastavit default collation na `Czech_CI_AS`

*musí bejt zastavenej service **mssql-server**!!!*
```shell
sudo systemctl stop mssql-server
sudo /opt/mssql/bin/mssql-conf set-collation
```
a zadat `Czech_CI_AS`

9. Nastavit jiné default adresáře pro datové soubory, logy, backupy, atd.
```shell
sudo /opt/mssql/bin/mssql-conf set filelocation.defaultdumpdir /datadrive/dumps
sudo /opt/mssql/bin/mssql-conf set filelocation.errorlogfile /datadrive/logs/errorlog
sudo /opt/mssql/bin/mssql-conf set filelocation.defaultlogdir /datadrive/SQLLOGS
sudo /opt/mssql/bin/mssql-conf set filelocation.defaultdatadir /datadrive/SQLDATA
sudo /opt/mssql/bin/mssql-conf set filelocation.defaultbackupdir /datadrive/backups
```

10. Nastavení max. paměti pro MSSQL
```shell
sudo /opt/mssql/bin/mssql-conf set memory.memorylimitmb 10240
```
je to v MB, takže nastavuju na 10G.

11. Nastavení dumpování
```shell
sudo /opt/mssql/bin/mssql-conf set coredump.disablecoredump false
sudo /opt/mssql/bin/mssql-conf set coredump.captureminiandfull false
sudo /opt/mssql/bin/mssql-conf set coredump.coredumptype miniplus
```

12. Kontrola nastavených parametrů
```shell
sudo cat /var/opt/mssql/mssql.conf
```

výsledek by měl být něco jako
```INI
[sqlagent]
enabled = false

[EULA]
accepteula = Y

[network]
tcpport = 1433

[filelocation]
defaultdatadir = /datadrive/SQLDATA
defaultlogdir = /datadrive/SQLLOGS
errorlogfile = /datadrive/logs/errorlog
defaultdumpdir = /datadrive/dumps
defaultbackupdir = /datadrive/backups

[memory]
memorylimitmb = 10240

[coredump]
disablecoredump = false
captureminiandfull = false
coredumptype = miniplus
```

13. Je dobrý MSSQL restartovat, po všech změnách
```shell
sudo systemctl restart mssql-server
```

14. Pak je dobrý některý věci nastavit přes T-SQL
```SQL
EXEC sys.sp_configure N'show advanced options', N'1'  RECONFIGURE WITH OVERRIDE
GO
EXEC sys.sp_configure N'max server memory (MB)', N'10240'
GO
RECONFIGURE WITH OVERRIDE
GO
```
