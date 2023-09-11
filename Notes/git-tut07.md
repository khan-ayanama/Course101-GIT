# GIT Stash

* Sometimes you want to switch the branches, but you are working on an incomplete part of your current project.
* You don't want to make a commit a half done work. Git stashing allows you to do so.
* The stash's meaning is "store somethng safely in hidden place". The sense is Git is also the same for stash, Git temporarily saves your data safely without commiting.

```git
    <!-- stash the modified fiels and creates new stash -->
    git stash

    <!-- If you want to give the name for particular stash -->
    git stash save <name>

    <!-- see the stash list -->
    git stash list

    <!-- To retrieve the recent stashed data into the branch we use & remove from stash -->
    git stash pop

    <!--To include message with stash  -->
    git stash save "message"

    <!-- When you want to maintain stash as well as pop -->
    git stash apply <stashId>
```

## Handle multiple stashes

```git
    <!-- To drop a stash without bringing it in working area -->
    git stash drop --> removes latest stash
    git stash drop <id>

    <!-- To check the stashed data befor pulling -->
    git stash show -p

    <!-- To delete all stash -->
    git stash clear

    <!-- Another branch for stash -->
    git stash branch new_branch stash@{id}
```
