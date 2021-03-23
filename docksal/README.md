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

* Clone Project form Repository
* Command  "fin up"
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
