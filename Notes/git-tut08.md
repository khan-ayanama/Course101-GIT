# Git checkout

* Moves from on branch to another
* Creates new branch if not existed and moves head to that branch.
* Not only branch it also shifts to particular commit has if you observe.

* If you move to a particular commit has using hash

```git
    git checkout <commit_has>
    <!-- Now you're in DETACHED HEAD -->
```

* Gith Checkout also supports another syntax

```git
    <!-- When you want to move the commit one step back without knowing the hash -->
    git checkout Head~1

    <!-- If you want to move back where you were previous -->
    git checkout -
```

* Git checkout also used to discard changes in the file.
* You can revert the changes of the particular file using.

```git
    git checkout Head <filename>
    git checkout --<filename>
```
