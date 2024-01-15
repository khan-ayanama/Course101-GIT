# Introduction

## Version Control System

It is a system that keep the record of changes in files or directory so that it preserves history of the project so whenever you need to know what was the file actually look like at particular point of time.
There are bunch of softwares available to help and make it easy to handle files or projects.

## Local Version Control System

A system is used to manage file or it's history locally in your computer you can either calculate manually by creating different folder or there are softwares which can help for eg: RCS (Revision Control System)
RCS keeps history only of files by keeping track of modifications.

## Central Version Control System

It is a system where all the versioned files put on the central server and bunch of developer can access from it, and developers work on the files whichever they needed.
It has downside of corrupted data or low time of server.

## Distributed Version Control System

It is a system where developers clone the whole repository or file into their system and work on it, if server looses data or get corrupted repository can be copied from any developrs machine.

## GIT

Git stores the reference of snapshot of complete project rather than changes.

## Three States in GIT

### Modified (Working Area)

It means you have changed the file but have not commited to your database yet.

### Staged

It means that you marked a modified file in its current version to go into your next commit snapshot

### Commit

It means that data is safely stored in your local database.

## GIT Configuaration

Git configuration is for when you commit it identifies you.

### Git has multilevel of configurations

- Repository/Project Level (local)
- User Account (Global level)
- System Level (git installation)

The command to add the username and email address is

Git config commands:

```bash
    # It shows the settings and where they are comming from
    git config --list --show-origin

    # Adding username and email
    git config --global user.name "John Doe"
    git config --global user.email johndoe@example.com

    # Your editor
    $ git config --global core.editor emacs

    # Default branch name
    git config --global init.defaultBranch main

    # Getting HElP
    git help <verb>

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

## Initializing a repository

```git
    git init
```

## Status of files

Gives info about branch and the file position

```bash
    git status

    # Short status
    git status -s
```

## git add

To add file in staging area

```git
<!-- This will add particular file -->
    git add <filename>

    <!-- This will add all the files -->
    git add .
    git add -A
```

## .gitignore

```bash
# ignore all .a files
*.a

# but do track lib.a, even though you're ignoring .a files above
!lib.a

# only ignore the TODO file in the current directory, not subdir/TODO
/TODO

# ignore all files in any directory named build
build/

# ignore doc/notes.txt, but not doc/server/arch.txt
doc/*.txt

# ignore all .pdf files in the doc/ directory and any of its subdirectories
doc/**/*.pdf
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

3. Difference between (working || Staging) area && repo area

   ```git
       git diff head
   ```
