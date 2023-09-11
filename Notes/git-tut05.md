# GIT Rebase

* Rebase is often used as an alternative to merging.
* Rebasing a branch updates one branch with another by applying the commits of one brach on top of the commits of  another branch.
* Git Rebase is used to clean up our local commit history
* Rebase is an advance command which is used rarely
* Rebase doens't preserve history

## Do not use Rebase when

The branch is public it is shared to all the developers, most of the teams prefer merger over rebase.

## Common places where we use rebases

* Cleaning up your commits before sharing your branch.
* Pulling changes from another branch without merge

```git
    git rebase branch_name
```

## Interactive Reabsing, Rewriting history by changing and squashing multiple commit message

Merging different commit into single commit

```git
    <!--Run this in the branch you want to rebase into master -->

    git rebase -i master
    git rebase --interactive master
```

## GIt Ammend

When you want to add the changes in previous commit instead of new commit

```git
    git commit --ammend
```

## GIT Cherry Pick

Cherry Pick is used if you want to apply particular commit from one branch into another branch.  
Cherry pick is mainly used if you don't want to merge the whole branch and you want some of the commit.

* It will duplicate the commit

```git
    git cherry-pick <hash>
```
