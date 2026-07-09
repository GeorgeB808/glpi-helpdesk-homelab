# PHP Configuration

## Installed Version

PHP 8.3

## Verification

```bash
php -v
```

## Installed Modules

* php-mysql
* php-intl
* php-mbstring
* php-xml
* php-curl
* php-gd
* php-imap
* php-bz2
* php-zip
* php-ldap

## Testing PHP

Created:

```
/var/www/html/info.php
```

Containing:

```php
<?php phpinfo(); ?>
```

Verified PHP processing through the browser.

## Lessons Learned

A common troubleshooting issue involved Apache displaying raw PHP code instead of executing PHP. Verifying the PHP module and Apache configuration resolved the issue.
