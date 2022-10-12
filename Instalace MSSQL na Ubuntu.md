# Instalace MSSQL na Ubuntu
https://learn.microsoft.com/en-us/sql/linux/sql-server-linux-setup?view=sql-server-ver16

1. MSSQL není standardní package pro Ubuntu, tak je potřeba přidat MS repository:
```
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
sudo add-apt-repository "$(wget -qO- https://packages.microsoft.com/config/ubuntu/20.04/mssql-server-2019.list)"
```
2. Teď můžu nainstalovat MSSQL:
```
sudo apt-get update
sudo apt-get install -y mssql-server
```
3. Když mám nainstalováno, musím nakonfigurovat:
```
sudo /opt/mssql/bin/mssql-conf setup
```
tady je potřeba zadat edici (asi Developer ne?) a heslo pro **sa**.

4. Nastavit správnou timezone:
```
sudo dpkg-reconfigure tzdata
```
a následovat nastavení, co se objevuje na terminálu.

5. Instalace command-line nástrojů
```
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
```
sudo /opt/mssql/bin/mssql-conf set network.tcpport 5050
sudo systemctl restart mssql-server
```
tak třeba tuto se mi ještě nepovedlo rozchodit. Pořád jedu přes 1433.

7. Vytvořit nové adresáře pro datové soubory, logy, atd. Vytvářím na disku ```/datadrive```
```
sudo mkdir /datadrive/SQLDATA
sudo chown mssql:mssql /datadrive/SQLDATA
```
a takhle si vytvořím adresáře pro data ```SQLDATA```, logy ```SQLLOGS``` a zálohy ```backups```

8. Nastavit default collation na Czech_CI_AS
```
sudo /opt/mssql/bin/mssql-conf set-collation
```

9. Nastavit jiné default adresáře pro datové soubory, logy, atd.
```
sudo /opt/mssql/bin/mssql-conf set filelocation.defaultdumpdir /datadrive/SQLLOGS
sudo /opt/mssql/bin/mssql-conf set filelocation.errorlogfile /datadrive/SQLLOGS/errorlog
sudo /opt/mssql/bin/mssql-conf set filelocation.defaultlogdir /datadrive/SQLDATA
sudo /opt/mssql/bin/mssql-conf set filelocation.defaultdatadir /datadrive/SQLDATA
```

10. Kontrola nastavených parametrů
```
sudo cat /var/opt/mssql/mssql.conf
```

výsledek by měl být něco jako
```
[sqlagent]
enabled = false

[EULA]
accepteula = Y

[network]
tcpport = 1433

[filelocation]
defaultdatadir = /datadrive/SQLDATA
defaultlogdir = /datadrive/SQLDATA
errorlogfile = /datadrive/SQLLOGS/errorlog
defaultdumpdir = /datadrive/SQLLOGS
```

11. Je dobrý MSSQL restartovat, po všech změnách
```
sudo systemctl restart mssql-server
```