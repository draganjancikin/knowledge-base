# GIT - GITHUB

Basic commands
* [Delete a Local GIT branch](#delete-a-local-git-branch)
* [Delete a remote GIT branch](#delete-a-remote-git-branch)

## Delete a Local GIT branch

Delete local branch, only if you have already pushed and merged it with your remote branches.

```bash
$ git branch --delete branch_name
```

or

```bash
$ git branch -d branch_name
```

## Delete a remote GIT branch

```bash
$ git push origin --delete branch_name
```
