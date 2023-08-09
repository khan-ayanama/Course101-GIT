# Notes

Github is online repository for git repo

## Git Cloning

Git will retreive all fies of repo and initialize new repo with full hisoty of project.

```git
    git clone <url>
```

## Github with SSH

We can connect to github using two methods

1. Using HTTPS
2. Using SSH

## Create Repo in Github

```git
    <!-- Check whether repo connected with remote repo -->
    git remote
    git remote -v

    <!-- Adding remote -->
    <!-- origin is short form of url you can write anything -->
    git remote add origin <url>
```

We have master as the default branch just like origin is default url, If needed we can change

### Renaming the Remotes

```git
    <!-- Renaming remote -->
    git remote rename <old_name> <new_name>

    <!-- Removing remote -->
    git remote remove <name>
```

## Push the local branch & commits to the Github repo

If you want to push the commit of one branch to the other branch from local to remote.

```git
    git push origin new_branch:master

    <!-- To check all the remote branch -->
    git branch -r
```

### -u option

* THe -u option allow us to set the upstream of the branch we are pushing.
* You can think of this as link between local branch to branch in github.
* It sets the default remote repo for local
