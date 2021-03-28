# GIT - GITHUB

Content index:

* [Git](#git)
  * [Instalation](#instalation)
  * [Setting](#setting)
  * [Basic commands](#basic-commands)
  * [Working with Branches](#working-with-branches)

## Git

### Instalation

Instalation on Debian/Ubuntu:

```bash
$ apt-get install git
```

### Setting

```bash
# Setting user name
$ git config --global user.name "John Doe"
# Setting email
$ git config --global user.email johndoe@example.com
# show global credentials
$ git config --global --list
# List you settings and where they are coming from
$ git config --global --list --show-origin
```

### Git Basics

Git is distributed: every developer has the full history of their code repository locally.

### How Git works

Here is a basic overview of how Git works:

1. Create a "repository" (project) with a git hosting tool (like Bitbucket)
2. Copy (or clone) the repository to your local machine
3. Add a file to your local repo and "commit" (save) the changes
4. "Push" your changes to your master branch
5. Make a change to your file with a git hosting tool and commit
6. "Pull" the changes to your local machine
7. Create a "branch" (version), make a change, commit the change
8. Open a "pull request" (propose changes to the master branch)
9. "Merge" your branch to the master branch

## Basic commands

* [Show and Set Git Username and Email](#show-and-set-git-username-and-email)
* [List existing branches](#list-existing-branches)
* [Switch between branches](#switch-between-branches)
* [Delete a Local GIT branch](#delete-a-local-git-branch)
* [Delete a remote GIT branch](#delete-a-remote-git-branch)
* [Delete a commit](#delete-a-commit)
* [Push Commits to a Remote GIT branch](#push-commits-to-a-remote-git-branch)

### List existing branches

```bash
# list all branches (local and remote)
git branch -a
# list local braches
git branch --list
```

### Switch between branches

```bash
# switch to master
git checkout master
# switch to branch branch_name
git checkout branch_name
```

### Delete a Local GIT branch

Delete local branch, only if you have already pushed and merged it with your remote branches.

```bash
git branch --delete branch_name
```

or

```bash
git branch -d branch_name
```

### Delete a remote GIT branch

```bash
git push origin --delete branch_name
```

### Delete a Commit

```bash
# 
$ git reset HEAD~number_of_commits
```

### Push Commits to a Remote GIT branch

```bash
#
git push -u origin master
#
git push -u "url_to_your_repository" master
```

## Working with Branches

<https://thenewstack.io/dont-mess-with-the-master-working-with-branches-in-git-and-github/>

Do not mess with the master. If you make changes to the master branch of a group project, very quickly there will be merge conflicts, weeping, rending of garments, and plagues of locusts.  

The master branch is deployable. It is your production code.

Open project, version on your compouter, and cd into the directoru.

* Step 1: Take inventory - list exist branches

```bash
git branch -a

```

* Step 2: Create a new branch and switch to it

We create a new version of the project, a branch, to make changes in locally on our computer — while the original version of the project, the master, remains safely on GitHub.  

We give the new branch a descriptive name.  

```bash
git checkout -b branchNameHere
```

* Step 3: Make changes in working branch

* Step 4: Stage and commit changes to working branch

```bash
# add changes to stage
git add name_of_changed_file
# check status
git status
# commit changes
git commit -m "Description of changes we made"
```

* Step 5: Merge working branch changes

Merge or move code, often from development to production.  
We need to be in master(main) branch.  

```bash
# first move to main branch
git checkput main
# then merge workiong branch
git merge working_branch_name --no-ff
# then push changet to GitHub
git push
# after the branch merged, delete branch
git branch -d working_branch_name
```

And that’s it!

* We successfully created a working branch separate from master.
* Made changes to it.
* Staged and committed those changes.
* Then merged them back into master on our local working environment.
* Then, finally, pushed everything up to GitHub so that all versions of our project are the same, everywhere!

-------------------------------------------------------------------------------

```bash
git checkout -b development
git push origin development
```

Very good tuto:
<https://www.thegeekstuff.com/2019/03/git-create-dev-branch-and-merge/>
