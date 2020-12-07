# Build drupal website workflow

1. [x] Create servers: LOCAL, DEV, PROD
2. [x] Create GitHub repository
3. [x] Install first copy of the website on DEV server
4. [x] Prepare LOCAL server and development
5. [x] Deployment to DEV
6. [x] Deployment to PROD

## 1. Create servers: LOCAL, DEV, PROD, and their respective databases

### LOCAL

* Address: <http://ed-drupal-website-local/>
* Database: ed_drupal_website_local
* Mysql username: DraganLocal
* Mysql password: Dragan73Local

### DEV

* Address: <http://ed-drupal-website-dev/>
* Database: ed_drupal_website_dev
* Mysql username: DraganDev
* Mysql password: Dragan73Dev

### PROD

* Address: <http://ed-drupal-website.bap.rs/>
* Database: rsba1022_ed_drupal_website
* Mysql username: rsba1022_DraganP
* Mysql password: Dragan73Prod

## 2. Create GitHub repository

* <https://github.com/draganjancikin/ed-drupal-website>

## 3. Install first copy of the website on DEV server

* Create project in empty folder with composer
* Add drush and install drupal
* Export configuration with drush
* Export database with drush
* Init git on DEV and link to GitHup repository
* Switch to develop branch
* Git add, commit and push code to GitHub

## 4. Prepare LOCAL server and development

* Restore db_backup.sql from DEV
* Git clone or pull
* add settings.php, change permission to 777, change settings.php, back permissions to 444
* Composer install
* Apply database updates : drush updb
* Import configuration (in case other developers made changes) : drush cim -y
* Clear caches : drush cr

* option steps
  * change permissions of web/sites/default to 755
  * make dir web/sites/default/files
  * change permissions of web/sites/default/files to 777

* Start work
* Finish work
* Export configuration : drush cex -y

* Git add, commit and push

## 5. Deployment to DEV

* Restore db_backup_local.sql from LOCAL
* git pull
* Composer install
* Apply database updates : drush updb
* Import configuration (in case other developers made changes) : drush cim -y
* Clear caches : drush cr
* Test to see what logged out users see

## 6. Deployment to PROD

* Only for first deployment restore db_backup_dev.sql from DEV
* Deploy the latest code
* Apply database updates: login as admin and go to /update.php
* Import configuration : /admin/config/development/configuration, review all changes make sense/are expected, then click `Import All`
* Check that all new expected functionality has now been deployed
* Clear caches : /admin/config/development/performance, then click `Clear All Caches`
* Test to see what logged out users see
