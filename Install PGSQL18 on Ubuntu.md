# Install PGSQL18 on Ubuntu 24.04.3 LTS
## Příprava

```bash
sudo apt update
sudo apt install postgresql-common ca-certificates
sudo /usr/share/postgresql-common/pgdg/apt.postgresql.org.sh
```

## Instalace
```bash
sudo apt update
sudo apt install postgresql-18 postgresql-contrib-18

psql --version
```
Mělo by se zobrazit něco jako:
```text
psql (PostgreSQL) 18.1 (Ubuntu 18.1-1.pgdg24.04+2)
```
## Vytvoření uživatelské DB
```bash
sudo -u postgres psql
```

```sql
create database mydb;
create user myuser with encrypted password 'mypass';
grant all privileges on database mydb to myuser;
```

## postgresql.conf
```bash
sudo vim /etc/postgresql/18/main/postgresql.conf
```
```ini
listen_addresses = '*'
port = 55432
max_connections = 10
```
## pg_hba.conf
```bash
sudo vim /etc/postgresql/18/main/pg_hba.conf
```

```text
host    <dbname nebo all>         <user nebo all>         212.79.110.248/32       password
```