# GLPI Help Desk Homelab

> Enterprise-style IT Help Desk & Asset Management homelab built with **GLPI 10.0.16**, **Ubuntu Server 24.04 LTS**, **Apache**, **PHP**, and **MariaDB**.

![GLPI](screenshots/dashboard.png)

---

# Project Overview

This project demonstrates the deployment and administration of a self-hosted IT Service Management (ITSM) platform using GLPI. The lab simulates a real-world Help Desk environment by managing users, IT assets, incident tickets, and technical documentation.

The objective was to gain practical experience with Linux server administration, web server configuration, database management, and enterprise Help Desk workflows.

---

# Technologies Used

* Ubuntu Server 24.04 LTS
* GLPI 10.0.16
* Apache 2
* PHP 8.3
* MariaDB
* Linux CLI
* VMware Workstation

---

# Skills Demonstrated

* Linux System Administration
* Apache Web Server Configuration
* PHP Configuration
* MariaDB Administration
* GLPI Installation
* IT Asset Management
* Help Desk Ticket Management
* Incident Lifecycle Management
* Knowledge Base Administration
* User & Role Management
* Technical Documentation
* Troubleshooting

---

# Lab Architecture

```text
                     Internet
                         │
                  Home Network
                         │
                Ubuntu Server VM
                         │
        Apache + PHP + MariaDB
                         │
                  GLPI 10.0.16
                         │
     ┌───────────┬────────────┬────────────┐
     │           │            │
   Users      Assets       Knowledge Base
     │           │            │
  Tickets   Computers     Articles
             Printers
        Network Equipment
```

---

# Features Implemented

## User Management

* Administrator Accounts
* Technician Accounts
* End User Accounts

---

## Asset Management

* Computer Inventory
* Printer Inventory
* Network Equipment
* Office Locations

---

## Help Desk

* Incident Ticket Creation
* Ticket Assignment
* Ticket Resolution
* Solution Documentation
* Ticket Lifecycle Management

Completed over **20 simulated Help Desk tickets** covering:

* Password Resets
* Printer Issues
* VPN Connectivity
* Outlook Problems
* Windows Performance
* Teams Authentication
* OneDrive Synchronization
* Software Installation
* Hardware Replacement

---

## Knowledge Base

Created documentation for common support procedures including:

* Windows Password Reset
* Printer Troubleshooting
* Outlook Repair
* VPN Troubleshooting
* Teams Sign-In
* Windows Updates
* OneDrive Sync
* Network Drive Mapping
* New Employee Setup
* Slow Computer Performance

---

# Screenshots

## Dashboard

![Dashboard](screenshots/dashboard.png)

## Computer Inventory

![Computers](screenshots/computers.png)

## Ticket Management

![Tickets](screenshots/ticket-list.png)

## Knowledge Base

![Knowledge Base](screenshots/knowledge-base.png)

---

# Installation

Detailed installation instructions are located in:

* docs/installation.md
* docs/apache-configuration.md
* docs/php-configuration.md
* docs/mariadb-setup.md

---

# Troubleshooting

Common issues encountered:

* Apache displaying PHP source code
* PHP module configuration
* GLPI login troubleshooting
* Knowledge Base publication
* DirectoryIndex configuration

Detailed troubleshooting is documented in:

docs/troubleshooting.md

---

# Lessons Learned

This project provided practical experience with:

* Linux server administration
* Apache configuration
* Database administration
* Enterprise Help Desk workflows
* Asset inventory management
* Technical documentation
* Structured troubleshooting

---

# Future Improvements

* Windows Server 2022 Integration
* Active Directory Authentication
* LDAP Integration
* Email Notifications
* Automatic Asset Discovery
* GLPI Agent Deployment
* Backup Automation
* SSL (HTTPS)

---

# Repository Structure

```
glpi-helpdesk-homelab/
│
├── README.md
├── LICENSE
├── .gitignore
│
├── docs/
│   ├── installation.md
│   ├── apache-configuration.md
│   ├── php-configuration.md
│   ├── mariadb-setup.md
│   ├── troubleshooting.md
│   ├── glpi-administration.md
│   └── lessons-learned.md
│
└── screenshots/
    ├── dashboard.png
    ├── users.png
    ├── computers.png
    ├── printers.png
    ├── network-devices.png
    ├── ticket-list.png
    ├── resolved-ticket.png
    └── knowledge-base.png

```

---

# Author

**George Baker**

Aspiring IT Support Specialist | Help Desk Technician | Systems Administrator

This project was created as part of my professional IT portfolio to demonstrate hands-on experience with enterprise IT support technologies.

