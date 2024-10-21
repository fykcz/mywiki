# Instalace MSSQL na Ubuntu
https://learn.microsoft.com/en-us/sql/linux/sql-server-linux-setup?view=sql-server-ver16

https://learn.microsoft.com/cs-cz/sql/linux/sql-server-linux-configure-mssql-conf?view=sql-server-ver16

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

15. Pokud je potřeba nastavit traceflag 272 globálně:
```shell
sudo /opt/mssql/bin/mssql-conf traceflag 272 on
```
ale není to nutnost, od SQL2017 je k dispozici parametr [`IDENTITY_CACHE`](https://learn.microsoft.com/en-us/sql/t-sql/statements/alter-database-scoped-configuration-transact-sql?view=sql-server-ver16).

16. Konfigurační hodnoty je možný odmazat
```shell
sudo /opt/mssql/bin/mssql-conf traceflag 272 off
```
pro traceflagy nebo pro celý parametry
```shell
sudo /opt/mssql/bin/mssql-conf unset network.tcpport
```

## Upgrade SQL Serveru
https://www.mssqltips.com/sqlservertip/4647/upgrading-sql-server-running-on-ubuntu-to-latest-update/

https://www.dropbox.com/scl/fi/0ulc70mssrrps3hw40m7e/SQL-Server-2019-Diagnostic-Information-Queries.sql?rlkey=dzjo336wm8uaffhwr3x4xygdr&e=2&dl=0

```
#check sql server package details
sudo apt-cache show mssql-server
```

```
#update packages list
sudo apt-get update
```

```
#check available updates for SQL Server
sudo apt-get --just-print upgrade
```

```
#Run apt-get update to update the source list of package.
sudo apt-get update mssql-server
```

https://learn.microsoft.com/en-us/sql/linux/sql-server-linux-change-repo?view=sql-server-ver16&pivots=ld2-ubuntu

```
# Check for previously configured repositories
sudo cat /etc/apt/sources.list
```

```
# Import the public repository GPG keys
sudo curl https://packages.microsoft.com/keys/microsoft.asc | sudo tee /etc/apt/trusted.gpg.d/microsoft.asc
```

```
# configure the repository
sudo add-apt-repository "$(curl https://packages.microsoft.com/config/ubuntu/20.04/mssql-server-2019.list)"
```

```
sudo apt-get update
```

```
#Upgrade SQL Server.
sudo apt-get install mssql-server
```

