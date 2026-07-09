# MariaDB Setup

## Installation

```bash
sudo apt install mariadb-server
```

## Secure Installation

```bash
sudo mysql_secure_installation
```

## Create Database

```sql
CREATE DATABASE glpi;
```

## Create User

```sql
CREATE USER 'glpi'@'localhost' IDENTIFIED BY 'StrongPassword';
```

## Grant Permissions

```sql
GRANT ALL PRIVILEGES ON glpi.* TO 'glpi'@'localhost';
FLUSH PRIVILEGES;
```

## Verification

Successfully connected GLPI installation wizard to MariaDB database.
