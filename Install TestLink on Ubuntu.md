# Install TestLink on Ubuntu
https://medium.com/@samueltcsantos/installing-the-teslink-in-ubuntu-fca5b01257a5
## Install *apache2*
```shell
$ sudo apt-get install apache2
```
## Install *php*
```shell
$ sudo apt-get install php php-mysql php-gd php-ldap php-json php-curl php-mbstring
```
## Install *mysql*
```shell
$ sudo apt-get install mysql-server
```
## Enable php in apache
```shell
$ sudo a2enmod php
```
https://stackoverflow.com/questions/35988990/how-to-enable-php7-module-in-apache
### Change data directory
https://stackoverflow.com/questions/1795176/how-to-change-mysql-data-directory
Potřebuju změnit adresář s datama na ```/datadrive/mysqldata```. Zkopíroval jsem adresáře mysql:
```shell
$ sudo cp -R -p /var/lib/mysql /datadrive/mysqldata
$ sudo cp -R -p /var/lib/mysql-files /datadrive/mysqldata
$ sudo cp -R -p /var/lib/mysql-keyring /datadrive/mysqldata
$ sudo mkdir /datadrive/log
```
Musí se změnit vlastník
```shell
$sudo chown -R mysql /datadrive/mysqldata
$sudo chgrp -R mysql /datadrive/mysqldata
```

```shell
$ sudo service mysql stop
$ sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf
```
Změna ```shell datadir=/datadrive/mysqldata/mysql```
No a pak je potřeba odstranit službu *apparmor*, která mi znemožňovala přesunout data pro mysql na jinej disk.
```shell
$ sudo /etc/init.d/apparmor stop
$ sudo /etc/init.d/apparmor teardown #tuto mi nefunguje, asi jina verze, nevadi
$ sudo update-rc.d -f apparmor remove
$ sudo apt-get purge apparmor
$ sudo reboot
```
Někdo zas uvádí
```shell
$ sudo service apparmor stop
$ sudo service apparmor teardown
$ sudo update-rc.d -f apparmor remove
$ sudo apt-get purge apparmor
$ sudo reboot
```
Když se nejdřív nastaví ten datadir, tak po rebootu mi už mysql naběhne.
## Příprava a konfigurace prostředků
### PHP app
* Stáhnout testlink z adresy https://sourceforge.net/projects/testlink/.
* Mě se stáhnul zip, takže rozzipovat někde ```shell unzip testlink-1.9.0```
* Přejmenovat adresář ```testlink-1.9.0``` na ```testlink```
* Přesunout adresář na správný místo
```shell
$ sudo mv testlink /var/www/html/
```
* Nastavit správný práva
```shell
$ sudo chmod -R 777 /var/www/html/testlink
```
* Pak nějaký další dva adresáře, netuším, k čemu, ale v návodu to je
```shell
$ cd /var
$ sudo mkdir testlink
$ sudo mkdir testlink/logs
$ sudo mkdir testlink/upload_area
$ sudo chmod 777 /var/testlink/ -R
```
### Zprovoznění databáze
```shell
$ sudo mysql -uroot
```
je to bez hesla, protože je to po instalaci. Takže změníme heslo.
#### Změna *root* hesla pro mysql
```shell
$ sudo mysql -uroot
```
```mysql
mysql> flush privileges;
mysql> use mysql;
mysql> alter user 'root'@'localhost' identified by 'novyheslo';
mysql> quit
```
```shell
$ sudo service mysql stop
$ sudo killall -u mysql
$ sudo service mysql start
```
#### Vytvoření databáze pro testlink
```mysql
mysql> create database testlink;
mysql> quit;
```
### Konfigurace PHPčka
Vytvořit soubor ```/var/www.html/testlink/config_db.inc.php``` a do něj zapsat:
```php
<?php
definir('DB_TYPE','mysql');
definir('DB_USER','root');
definir('DB_PASS','...'); # to nový heslo
definir('DB_HOST','localhost');
definir('DB_NAME','testlink');
definir('DB_TABLE_PREFIX','');
?>
```
A nakonec změnit práva na soubor
```shell
$ sudo chmod 777 /var/www.html/testlink/config_db.inc.php
```
a restartovat Apache
```shell
$ sudo service apache2 restart
```
## Instalace a konfigurace Testlink z prohlížeče
* Spustit http://.../testlink/install/index.php.
* Vybrat New installation
* 