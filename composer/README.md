# COMPOSER

Composer is a (commandline) tool for dependency management in PHP. With composer declare the libraries / packages / tools
 your project depends on, and composer will manage (install, update) them.  
Composer install globaly but use localy per-projects.

Files:

* composer.json
* composer.lock

## System Requirements

Composer requires PHP 5.3.2+ to run.

## Installation on Linux/Ubuntu

Globally:

First navigate to /bin/ folder, then

```bash
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === 'c31c1e292ad7be5f49291169c0ac8f683499edddcfd4e42232982d0fd193004208a58ff6f353fde0012d35fdd72bc394') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
```
