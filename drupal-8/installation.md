# Drupal 8: Installation

Content index:

* [Install with Docksal on Ubuntu-Debian Linux](#install-with-docksal-on-ubuntu-debian-linux)
* [Setup an Existing Project on Local](#setup-an-existing-project-on-local)

## Install with Docksal on Ubuntu-Debian Linux

Prerequisites:

* Installed Docksal ( [Read more](../docksal/installation.md) )

```bash
# Quick start using a boilerplate
$ fin project create
```

After that:
* Typing project name
* Choose option for Drupal 8 (Composer version)
* Confirm: y - to proceed

## Setup an Existing Project on Local

Steps:

* Clone Project from Repository
* Command "fin up"
* Set up docksal to use composer 1.x <https://docs.docksal.io/tools/composer/#versions>
* After that: "fin composer install"
* copy .htaccess to web and settings.local.php to web/sites/default iz .docksal foldera
* fin db import /putanja-do-baze/naziv-fajla.sql
* fin drush cr
