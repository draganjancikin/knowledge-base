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
