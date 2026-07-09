# Apache Configuration

## Virtual Host

Document Root

```
/var/www/html
```

GLPI Location

```
/var/www/html/glpi
```

## Required Modules

Enable PHP:

```bash
sudo a2enmod php8.3
```

Restart Apache:

```bash
sudo systemctl restart apache2
```

## Common Verification Commands

```bash
sudo systemctl status apache2
```

```bash
apache2ctl -S
```

```bash
hostname -I
```

## Lessons Learned

* Apache was functioning correctly.
* GLPI was accessible through:

```
http://SERVER-IP/glpi/index.php
```

* Accessing `/glpi` initially returned PHP source code until configuration issues were resolved.
