# Troubleshooting Guide

## Problem

Apache displayed PHP source code.

### Resolution

Verified:

* PHP installation
* Apache PHP module
* DirectoryIndex configuration
* Virtual Host configuration

---

## Problem

GLPI displayed "Incorrect username or password."

### Resolution

Used the default administrator account:

Username:

```
glpi
```

Password:

```
glpi
```

Changed the password after first login.

---

## Problem

Knowledge Base articles were not published.

### Resolution

Assigned publication targets and enabled article visibility for the Root entity.

---

## Problem

GLPI accessible through:

```
/glpi/index.php
```

but not:

```
/glpi
```

### Resolution

Verified Apache DirectoryIndex configuration and confirmed `index.php` loading correctly.
