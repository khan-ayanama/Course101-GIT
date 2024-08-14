# Git Basics

There are two ways of initializing git repository.

- Clone an existing repository
- You can turn local directory to git repository

## Initializing local direcoty

```bash
    git init
```

## Tracked vs Untracked files

Tracked files are the one which were present in the last snapshot or modified, unmodified staged files.

Untracked means git will see files which are present but not present at the time of last snapshot, until you add it it won't add it in your repository.

## Trackig new files

```git
    <!-- Adding files -->
    git add file_name

    <!-- Status for short -->
    git status -s
```

## Short Status

`git status -s || git status --short` for short form of status of repo

When you run short status command you get some type of letter code:-
`M`: Modified files
`MM`: The presence of two M characters signifies staged and unstaged modifications.
`A`: File added to staging area.
`??`: File is not tracked.

## Ignoring files

- Blank lines or line starting with # are ignored
- Added files will be checked recursively
- To avoid recursion use forward slash(/)

```txt
    # Ignoring file ending with .o or .a
    *.[oa]

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

## git Diff

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

## Commiting files

- When you don't pass message from terminal and commit file open in your editor

```bash
    git commit
```

- When you want to see detailed changes in files in commit message

```bash
    git commit -v
```

- When you pass message from terminal

```bash
    git commit -m "commit message"
```

- When you want to commit but without staging
  NOTE: It will not commit newly created file but the files which are already tracked.

```bash
    git commit -a -m "commit message without staging"
```

## Removing files

`Remove from Working Directory:`
Delete the file manually from your working directory. For example, if you want to remove 'file-03.txt', you can use the following command:

```bash
rm file-03.txt
```

`Use git rm to Stage the Deletion:`
Once you've deleted the file, you need to stage the deletion in Git using the git rm command:

```bash
git rm file-03.txt
```

This command stages the file for removal, both from your working directory and the next commit.

`Commit the Changes:`
After staging the deletion, you need to commit the changes:

```bash
git commit -m "Remove file-03.txt"
```

- If you want to remove a file from the repository but keep it in your working directory, you can use the --cached option with git rm:

```bash
git rm --cached file-03.txt
```

This will remove the file from the staging area (index) but keep it in your working directory.

## Moving files

`Use git mv to Rename/Move:`
To move a file or rename it, use the git mv command. For example, if you want to move 'file-03.txt' to a new directory called 'new_directory', you would do:

```bash
git mv file-03.txt new_directory/
```

If you're renaming the file, you can do:

```bash
git mv old_filename.txt new_filename.txt
```
