# DRUPAL 8

## Drupal and Composer

Composer did:

* get the (non-core) modules and themes on which your site depends
* get the libraries and any other packages on which your site depends, including whatever packages ^^those packages need, using right package version, keeping track of exactly which version of what is instaled
* update + remove packages
* track / maintain precise details about the Stuffs your project is made (composed!)

Composer can't:

* enable / disable modules on Drupal site
* manage site configuration
* content anything

Files:

* composer.json (contains list of project dependencies, instalation paths, ...)
* composer.lock (contains what packages and package versions are currently installed (downloaded on your project)

Version constraints:

* ~ ----- ~8.3 won't go to 8.4.0
* ^ ----- ^8.3 will go to 8.4.x, 8.5.x, etc to 8.9xxxx

Composer package files comes from packagist.org.  
For Drupal 8, official composer package service is: <https://packages.drupal.org/8>.

```bach
composer install
composer update
composer require the_vendor_name/the_package_name:^X.x
composer update
composer remove
```

First uninstall nodules from Drupal, then remove from project.

## Install Drupal 8 with composer

Prerequisities: Install Composer globaly.

Steps:

* Create a new Drupal 8 project - a new composer project

```bash
composer create-project drupal/recommended-project:8.9.8 my_site_name_dir
```

will be create folder my_site_name_dir, and put inside all necessery Drupal 8 folders and files

* Add modules and whatever other packages as dependencies
* Use composer to install (download) those packages to your project
* Update composer.lock file
