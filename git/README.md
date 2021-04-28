# Git

Content index:

* [Introduction](#introduction)
* [Instalation](#instalation)
* [Settings](#settings)
* [Basic commands](#basic-commands)

## Introduction

Git is distributed: every developer has the full history of their code repository locally.

## Instalation

Instalation on Debian/Ubuntu:

```bash
$ apt-get install git
```

## Settings

Setting git username and email:

```bash
# Create system config for username and email
$ git config --system user.name "John Doe"
$ git config --system user.email "john.doe@gmail.com"

# Create global config for username and email
$ git config --global user.name "John Doe"
$ git config --global user.email "john.doe@gmail.com"

# Create project specific config for username and email. Execute commands under project's directory
$ git config user.name "John Doe"
$ git config user.email "john.doe@gmail.com"
```

Project overrides global and global overrides system config.

View config:

```bash
# show global credentials
$ git config --global --list
# List you settings and where they are coming from
$ git config --global --list --show-origin
```

## Basic Commands

* [Add file to stage](#add-file-to-stage)
* [Commit changes](#commit-changes)

### Add File to Stage

```bash
# Add file to stage.
$ git add file_name
# Add all files to stage
$ git add .
```

### Remove File from Stage

```bash
# Remove one file from stage.
$ git reset file_name 
```

### Commit Changes

```bash
# Commit.
$ git commit -m "Commit message"





# Rebase.
# Rebasing is the process of moving or combining a sequence of commits to a new base commit.
# From a content perspective, rebasing is changing the base of your branch from one commit to another making it appear as if you'd created your branch from a different commit. 
$ git rebase <base> # <base> is usually master branch 

# Delete upstream branch
$ git push origin --delete feature/login
```
