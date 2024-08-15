# Viewing Commit history

`git log`: It list the commits in reverse chronological order.
`git log --patch -2`: this show the difference between changes introduced in each commit in last 2 commits.
`git log -p -2`: It is same as above.
`git log --stat`: It shows stat of each commit means number of changes in file or repo etc.
`git log --pretty=oneline`: Logs commit in single line.
`git log --pretty=full`: Logs commit in comprehensivly.
`git log --pretty=fuller`: Logs commit more comprehensively.
`git log --pretty=short`: Logs commit in short form.
`git log --pretty=format:"%h - %an, %ar : %s"`: Log in given input format.
`git log --pretty=format:"%h %s" --graph`: It prints ASCII graph showing branches and merge history.
`git log --since=2.weeks`: It will show the commit for last 2 weeks.
`git log --until=2.weeks`: It will show the commit until 2 weeks from starting.
`git log -S function_name`: It will show the logs of particular function.
`git log --path/to/file`: It will show logs of particular file.
`git log --pretty="%h - %s" --author="Ayan Khan" --since="2024-4-10" --before="2024-04-10" --no-merges`

- no-merges shows the logs which are actually commits not a merging.

## Undoing things

`git commit --amend`: It can modify last commit.
`git checkout -- CONTRIBUTING.md`: Undo things to last commited stage.
`git reset HEAD CONTRIBUTING.md`: Undo things to last commited stage.
`git restore <file>`: restore image to last commit.

## Working with Remotes

`git remote`: Short name for each handle.
`git remote -v`: shows the URL

`git remote add <shortname> <URL>`: Adding repo to remote.
**shortname**: It is used for convenience so that we don't need to define it each time working with remote.

`git fetch <shortname>|<url>`: To fetch data from remote.
