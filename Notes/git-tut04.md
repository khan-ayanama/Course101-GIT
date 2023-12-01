# GIT Merge

Go to the target folder in which branch you want to commit and then merge the branch you want to merge.

* If there has been a changes in different files then there will be no problem while merging.
* If there has been a changes in same file in different files then conflicts should be resolve.

```git
    git merge merge_branch_name
```

## Resolve conflict while merging

When we want to merge the branches but the changes has been made in the same file in both the branches so we have to decide which changes we want to commit.

```git
    <!-- Abort merging -->
    git merge --abort
```
