# Build drupal site with git

<https://www.drupal.org/docs/installing-drupal/building-a-drupal-site-with-git>

## Introduction

Development environment model:

* developers work on most code locally
* then push that code up through Development
* Staging and
* Production environments

Useful drupal modules:

* Chaos Tool Suite (ctools)
* Backup and Migrate (backup_migrate)

## Step 1: Servers setup - OK

Configure three servers for three enviroments:

* DEV
* STG
* PROD

## Step 2: Creating the Central Repository - OK

Create a central repository from which all other environments will pull (GitHub, ...).

## Step 3: Locally Install Drupal - OK

(On your local development enviroment)

## Step 4: Updating Remotes - OK

(On your local development environment)

```bash
 git init
 git add REAMDE.md
 git commit -m 'first commit'
 git branch -M main
 ...
```

## Step 5: Creating a working branch - develop branch

(On your local development environment)

```bash
 git checkout -b develop
```

## Step 6: Setting up the .gitignore file

Drupal 8 comes without a .gitignore but has an example.gitignore from which you can create a .gitignore.

If you wish to transfer configuration between sites using git, you probably need to change the location of the config directory (which is set in settings.php) to one which is tracked by git. By default, the config directory is in sites/default/files, and by default the .gitignore which you create from example.gitignore will exclude this directory path.

## Step 7: Customizing .gitignore

<https://www.drupal.org/docs/installing-drupal/building-a-drupal-site-with-git#gitignore-custom>

## Step 8: Pushing Code to the Central Repository and Completing Initial Deployment

On your local development environment

```bash
 git push origin fooproject
```

On your remote server

```bash
 # get (clone) project from github
 git clone project_name@fooproject.com/home/users/fooproject/fooproject.git folder_name
 # install dependencies
 composer install
 # instal site with drush
 drush site:install --site-name= ...
```

In Drupal 8 the site should be installed only once (rather than repeating the install for dev, staging and production sites), and the different versions of the site should be created with databases set up using a dump of the database from the first copy of the site. This is because each install creates a distinct site with a site UUID, which would prevent import of configuration between the dev, staging and production versions of the site (subject to #1613424: [META] Allow a site to be installed from existing configuration being solved). After copying a site's database, it will be necessary to clear the caches (which can be done from Manage > Configuration > Performance, or using drush from command line).

Because the install is only run on the first copy of the site, it will also be necessary to open settings.php on each version of the site, and manually adjust the database settings in it to use the relevant copy of the database for each version of the site. Naming the databases similarly to the code directories, such as fooproject_dev, fooproject_stg, fooproject_prod, can help avoid confusion .

If you have set up a default .gitignore which excludes the sites/*/default folder before copying the code to each version of the site using git, settings.php and the config directory (assuming it is still in the default location) will not have been copied when copying the code with git. In that case, so you would need to manually copy settings.php to each version of the site, and you would need to either manually copy the config directory or rebuild it, in order to get the copies of the site working. For troubleshooting after copying a site see <https://www.drupal.org/documentation/rebuild>.

## Step 9: Adding Contributed Modules and Themes

Simply download and install modules and themes to your site and add them to your main development branch.

```bash
 git add ...
 git commit -m “message”
 git push
```

Then, on your remote server while inside the dev directory:

```bach
 git pull ...
```
