# Docksal

## Instalation on Linux/Ubuntu

<https://docksal.io/installation#linux-supported>

Docksal zna da se sukobi sa Apache-em oko portova, tako da bi bilo dobro da stopiras apache2 pre nego se krene sa Docksal-om.

```bash
#
$ bash <(curl -fsSL https://get.docksal.io)
```

## Setup Existing Project on Local

Steps:

* Clone Project from Repository
* Command "fin up"
* Set up docksal to use composer 1.x <https://docs.docksal.io/tools/composer/#versions>
* After that: "fin composer install"
* copy .htaccess to web and settings.local.php to web/sites/default iz .docksal foldera
* fin db import /putanja-do-baze/naziv-fajla.sql
* fin drush cr

## Commands: fin

```bash
# start project
$ fin start
# stop project
$ fin stop
```

## Update Drupal Core and Modules

```bash
# check outdated 
$ fin composer outdated "drupal/*"

# update Drupal Core
$ fin composer require drupal/core-recommended:8.9.13 drupal/core:8.9.13 --update-with-all-dependencies

# update Drupal module
$ fin composer update drupal/modulename --with-dependencies
```

First Drupal core update:

* make a new branch
* update Drupal core
* clear cache
* check site

On link <http://psc.docksal/admin/reports/updates> is avaible updates. Need to enable Update Manager module.

Module update:

* make a new branch
* check Release Notes for important updates
* update module
* clear cache
* check site
* commit
* after all updates merge to dev if exist, if not merge to master
* deploy to dev
* backup db from dev
* db update on dev
* obeležiti testeru da istestira
