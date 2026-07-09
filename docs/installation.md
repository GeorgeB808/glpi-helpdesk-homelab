# GLPI Help Desk Homelab - Installation Guide

## Overview

This project documents the deployment of a self-hosted **GLPI 10.0.16** IT Service Management (ITSM) platform on **Ubuntu Server 24.04 LTS**. The environment simulates an enterprise Help Desk with ticketing, asset management, user administration, and a knowledge base.

---

# Lab Environment

| Component        | Version                 |
| ---------------- | ----------------------- |
| Operating System | Ubuntu Server 24.04 LTS |
| GLPI             | 10.0.16                 |
| Web Server       | Apache 2                |
| PHP              | 8.3                     |
| Database         | MariaDB                 |
| Virtualization   | VMware Workstation      |

---

# System Requirements

* 2 vCPUs
* 4–8 GB RAM
* 40 GB Storage (80 GB recommended)
* Internet Connection
* Ubuntu Server 24.04 LTS

---

# Step 1 – Update Ubuntu

Update the operating system before installing any packages.

```bash
sudo apt update
sudo apt upgrade -y
```

Verify the server is up to date.

---

# Step 2 – Install Apache

Install the Apache web server.

```bash
sudo apt install apache2 -y
```

Verify Apache is running.

```bash
sudo systemctl status apache2
```

Expected output:

```
Active: active (running)
```

---

# Step 3 – Install PHP

Install PHP and the required extensions for GLPI.

```bash
sudo apt install php php-cli php-common php-mysql php-gd php-curl php-intl php-mbstring php-xml php-zip php-bz2 php-imap php-ldap -y
```

Verify PHP.

```bash
php -v
```

Expected output:

```
PHP 8.3.x
```

---

# Step 4 – Install MariaDB

Install the database server.

```bash
sudo apt install mariadb-server -y
```

Verify the service.

```bash
sudo systemctl status mariadb
```

---

# Step 5 – Secure MariaDB

Run the security wizard.

```bash
sudo mysql_secure_installation
```

Recommended options:

* Set root password
* Remove anonymous users
* Disallow remote root login
* Remove test database
* Reload privilege tables

---

# Step 6 – Create the GLPI Database

Log into MariaDB.

```bash
sudo mysql
```

Create the database.

```sql
CREATE DATABASE glpi;
```

Create a database user.

```sql
CREATE USER 'glpi'@'localhost' IDENTIFIED BY 'StrongPassword';
```

Grant permissions.

```sql
GRANT ALL PRIVILEGES ON glpi.* TO 'glpi'@'localhost';
FLUSH PRIVILEGES;
EXIT;
```

---

# Step 7 – Download and Install GLPI

Download the GLPI archive from the official website.

Extract the files into:

```
/var/www/html/glpi
```

Set ownership.

```bash
sudo chown -R www-data:www-data /var/www/html/glpi
```

Restart Apache.

```bash
sudo systemctl restart apache2
```

---

# Step 8 – Access GLPI

Determine the server IP.

```bash
hostname -I
```

Open a browser and navigate to:

```
http://SERVER-IP/glpi/index.php
```

Example:

```
http://192.168.1.33/glpi/index.php
```

Complete the installation wizard using the MariaDB database credentials created earlier.

---

# Step 9 – First Login

Default credentials:

**Username**

```
glpi
```

**Password**

```
glpi
```

Immediately change the default administrator password after logging in.

---

# Step 10 – Initial Configuration

Configure:

* Company Locations
* Users
* Profiles
* Computers
* Printers
* Network Equipment
* Ticket Categories
* Knowledge Base

---

# Lab Completed

The completed lab includes:

* Ubuntu Server administration
* Apache configuration
* PHP configuration
* MariaDB configuration
* GLPI deployment
* User administration
* Asset inventory
* Incident ticket management
* Knowledge Base creation

---

# Skills Demonstrated

* Linux Administration
* Apache Web Server
* PHP Configuration
* MariaDB Administration
* IT Service Management (ITSM)
* Asset Management
* Help Desk Operations
* Technical Documentation
* Troubleshooting
* Enterprise System Administration

---

# Lessons Learned

During this project several real-world troubleshooting scenarios were resolved, including:

* Apache displaying raw PHP source code
* PHP module verification
* DirectoryIndex configuration
* GLPI login issues
* Knowledge Base publication
* User account administration

These issues strengthened Linux troubleshooting skills and reinforced best practices for deploying enterprise web applications.
