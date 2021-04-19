# Git

Content index:

* [Configuration](#configuration)
* [Commands](#commands)

## Configuration

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

## Commands

```bash
# Add file to stage.
$ git add file_name

# Commit.
$ git commit -m "Commit message"

# Rebase.
# Rebasing is the process of moving or combining a sequence of commits to a new base commit.
# From a content perspective, rebasing is changing the base of your branch from one commit to another making it appear as if you'd created your branch from a different commit. 
$ git rebase <base> # <base> is usually master branch 

# Delete upstream branch
$ git push origin --delete feature/login
```
