# GIT - Intro

* Git is a Version Control System (VCS)
* VCS is software designed to record changes made to the file or folder over time.
* It also record images, research paper etc.

## Type of VCS

### Local Version Control System

It primarily focuses on tracking changes and providing version history within a single machine.

### Centralized Version control System

The central server acts as a single source of truth, where all changes are stored and accessed by team members.

### Distributed Version Control System

It allows multiple developers to work on the same project without needing a central server or a single point of control. Instead, each developer has their own complete copy of the project, including its entire history of changes.

## Three States in GIT

### Modified (Working Area)

It means you have changed the file but have not  commited to your database yet.

### Staged

It means that you marked a modified file in its current version to go into your next commit snapshot

### Commit

It means thatt data is safely stored in your local database.

## GIT Configuaration

### Git has multilevel of configurations

* Repository/Project Level (local)
* User Account (Global level)
* System Level (git installation)

The command to add the username and email address is  

```cmd
    git cofig
```

### Git Configuration commands

1. Initialize git repository

    ```git
        git init
    ```

2. To see hidden files and folder

    ```git
        ls -a
    ```

3. To configure email locally

    ```git
        git config --local user.email newmail@gmail.com
    ```

4. To unset the field

    ```git
        git config --unset user.email
    ```

5. To remove section

    ```git
        git config --local --remove-section user
    ```

## git help

```git
    git help
    git help -a | git help --all
    git help init
    git help all
```

## git status

Gives info about branch and the file position

## git add

To add file in staging area

```git
<!-- This will add particular file -->
    git add <filename>

    <!-- This will add all the files -->
    git add .
    git add -A
```

## git commit

To commit file

```git
    git commit
    git commit -m "message"
```

## git log

It shows all the commits

```git
    git log
    git log --oneline
```

## git diff

It gives the difference between the changes made in file

1. Difference between working area and staging area

    ```git
        git diff
    ```

2. Difference between staging area and repo area

    ```git
        git diff --staged
    ```

3. Difference between working area and repo area

    ```git
        git diff head
    ```
