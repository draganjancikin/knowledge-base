# COMPOSER

Composer is a (commandline) tool for dependency management in PHP. With composer declare the libraries / packages / tools
 your project depends on, and composer will manage (install, update) them.  
Composer install globaly but use localy per-projects.

Files:

* composer.json
* composer.lock

Index:

* [System Requirements](#system-requirements)
* [Installation on Ubuntu](#installation-on-ubuntu)
* [Commands](#commands)

## System Requirements

Composer requires PHP 5.3.2+ to run.

## Installation on Ubuntu

Globally:

First navigate to /bin/ folder, then

```bash
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === 'c31c1e292ad7be5f49291169c0ac8f683499edddcfd4e42232982d0fd193004208a58ff6f353fde0012d35fdd72bc394') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
```

## Commands

### require

Adds a new packages to the composer.json file in project (current) directory. If composer.json no exists one will be created.

```bash
composer require vendor_name/package_name
```

### self-update

To update Composer itself to the latest version

```bash
# If you have installed Composer for your entire system (global installation), you may have to run the command with root privileges
composer sudo -H composer self-update
# If you would like to instead update to a specific release specify it
composer sudo -H composer self-update 2.0.11
```
