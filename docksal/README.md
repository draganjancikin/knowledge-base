# Docksal

## Content Index

* [Installation on Linux-Ubuntu](#installation-on-linux-ubuntu)
* [Setup an Existing Project on Local](#setup-an-existing-project-on-local)
* [Commands](#commands)
* [Update Drupal Core and Contrib Modules](#update-drupal-core-and-contrib-modules)
* [Delete Local and Remote Commits](#delete-local-and-remote-commits)

## Installation on Linux-Ubuntu

<https://docksal.io/installation#linux-supported>

Docksal zna da se sukobi sa Apache-em oko portova, tako da bi bilo dobro da stopiras apache2 pre nego se krene sa Docksal-om.

```bash
#
$ bash <(curl -fsSL https://get.docksal.io)
```

## Setup an Existing Project on Local

Steps:

* Clone Project from Repository
* Command "fin up"
* Set up docksal to use composer 1.x <https://docs.docksal.io/tools/composer/#versions>
* After that: "fin composer install"
* copy .htaccess to web and settings.local.php to web/sites/default iz .docksal foldera
* fin db import /putanja-do-baze/naziv-fajla.sql
* fin drush cr

## Commands

```bash
# start project
$ fin start
# stop project
$ fin stop
```

## Update Drupal Core and Contrib Modules

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

## Delete Local and Remote Commits

```bash
# delete local commits
$ git reset HEAD~number_of_commits_that_deleting

# reverting composer.lock on start state 
$ git checkout composer.lock

# push changes to repository
# "+" before master mean "force"
$ git push origin +master
```
