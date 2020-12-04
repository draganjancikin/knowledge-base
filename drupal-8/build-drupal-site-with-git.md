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

## Step 1: Servers setup

Configure three servers for three enviroments:

* DEV
* STG
* PROD

## Step 2: Creating the Central Repository

Create a central repository from which all other environments will pull (GitHub, ...).
