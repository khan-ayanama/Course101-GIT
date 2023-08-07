# Git restore and switch

## GIT Switch

The git switch command is a newer alternative to the traditional git checkout command for switching branches in Git. It was introduced in Git version 2.23 as part of an effort to provide clearer and more intuitive commands for common actions. The git switch command is intended to be more user-friendly, especially for users who are new to Git or find the git checkout syntax a bit confusing.

* Here's how the git switch command works and how it differs from git checkout:

### Switching Branches

* The primary purpose of the git switch command is to switch between branches.

```git
    git switch branch_name
```

* Creating and Switching to a New Branch:
Just like with git checkout, you can create a new branch and switch to it using a single git switch command.

```git
    git switch -c new_branch_name
```

## Git Restore

The git restore command is used to restore or revert changes made to files in your working directory to a previous state. It's a versatile command that helps you manage the state of your files in various scenarios. Here are some common use cases for the git restore command:

### Discard Local Changes

You can use git restore to discard the changes you've made to a specific file, reverting it to the state of the last committed version.

```git
    git restore file_name
```

### Restore Specific Version

You can use git restore to restore a specific version of a file from a particular commit or branch.

```git
    git restore --source=commit_hash file_name
```

### Interactively Restore Changes

The --patch (or -p) option allows you to interactively select changes within a file that you want to restore.

```git
    git restore --patch file_name
```

### Restore Entire Working Directory

You can use git restore to restore all files in your working directory to their last committed state.

```git
    git restore .
```

### Restore Files in a Specific Directory

You can target a specific directory to restore its contents to the last committed version.

```git
    git restore directory_name
```

### Dry Run

To see what git restore would do without actually making any changes, you can use the --dry-run option.

```git
    git resotre --dry-run file_name
```
