# Git

Content index:

* [Commands](#commands)

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
