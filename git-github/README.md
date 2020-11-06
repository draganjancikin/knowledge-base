# GIT - GITHUB

## Basic commands:
* [List existing branches](#list-existing-branches)
* [Switch between branches](#switch-between-branches)
* [Delete a Local GIT branch](#delete-a-local-git-branch)
* [Delete a remote GIT branch](#delete-a-remote-git-branch)

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

## Working with Branches (Git - GitHub)

Do not mess with the master. If you make changes to the master branch of a group project, very quickly there will be merge conflicts, weeping, rending of garments, and plagues of locusts. It’s that serious.  

<mark>The master branch is deployable. It is your production code</mark>

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
