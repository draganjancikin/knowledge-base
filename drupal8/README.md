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
composer init
composer install
composer require the_vendor_name/the_package_name:^X.x

composer update
composer update the_vendor_name/the_package_name --with-dependencies

composer outdated
composer remove
composer create-project
```

First uninstall nodules from Drupal, then remove from project.

## Install Drupal 8 with composer

Prerequisities: Install Composer globaly.

### Step 1: Create a new Drupal 8 project - a new composer project

```bash
composer create-project drupal/recommended-project:8.9.8 my_site_name_dir
```

will be create folder my_site_name_dir, and put inside all necessery Drupal 8 folders and files

After instal Drupal 8 recomended next steps:

* Install the site: <https://www.drupal.org/docs/8/install>
* Read the user guide: <https://www.drupal.org/docs/user_guide/en/index.html>
* Get support: <https://www.drupal.org/support>
* Get involved with the Drupal community:
      <https://www.drupal.org/getting-involved>
* Remove the plugin that prints this message:
      composer remove drupal/core-project-message
* Homepage: <https://www.drupal.org/project/drupal>
* Support:
  * docs: <https://www.drupal.org/docs/user_guide/en/index.html>
  * chat: <https://www.drupal.org/node/314178>

### Step 2

* Add modules and whatever other packages as dependencies
* Use composer to install (download) those packages to your project
* Update composer.lock file

## Recomended Modules

* Admin Toolbar (drupal/admin_toolbar)
      * submodul - Admin Toolbar Tools (admin_toolbar_tools)

* Drush (drupal/drush) +

* Pathauto (drupal/pathauto) +

* Token (token) +

* Simple Google Masp (simple_gmap) +

* AddToAny (addtoany)

* Scheduler (scheduler)

* Devel (devel) +
