# Git revert

The git revert command is used to create a new commit that undoes the changes introduced by a specific commit or a range of commits. It's a way to reverse the effects of a commit without actually removing it from the history. This is a safer way of undoing changes compared to tools like git reset, which can alter history and potentially cause issues when collaborating with others.

## Revert a Single Commit

To revert the changes introduced by a single commit, use the following syntax:

```git
    git revert <commit_hash>
```

This will create a new commit that undoes the changes introduced by the specified commit.

## Revert a Range of Commits

To revert a range of commits (inclusive), you can provide a commit range in the following format:

```git
    git revert <oldest_commit_hash>..<newest_commit_hash>
```

## Revert a Merge Commit

When reverting a merge commit, you'll need to specify the -m option followed by the parent number (1-based index) of the mainline parent in the merge commit. This tells Git which parent's changes to undo.

```git
    git revert -m <parent_number> <merge_commit_hash>
```

## Commit Message

When you run git revert, Git will prompt you to edit the commit message for the new revert commit. By default, the message will include information about the commit(s) being reverted.

## Conflict Resolution

* If the commit you're trying to revert and your current state have conflicting changes, Git will prompt you to resolve the conflicts before creating the revert commit.

* Using git revert is a safer way to undo changes because it creates a new commit that undoes the specified changes while preserving the history. Other team members who might have based their work on the original changes won't be adversely affected.

* Remember that the git revert command can be used to selectively undo specific changes from a commit, so it doesn't remove the entire commit from history. Always ensure you understand the consequences of using this command and the changes it will make to your repository.
