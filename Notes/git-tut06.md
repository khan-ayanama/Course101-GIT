# Notes - 06

## Detached Head in GIT

When commit is not in branch but at some hash than branch will be same but head will move to particular commit

### GIT Head

* When we are working we only checkout one branch at a time. This is also called as Head branch.  
* Git makes note of this branch and stores it in .git/Head
* Head as the reference for the path of the branch.  
* Head is nothing but the reference to the branch  
* Head not only reference a branch it also reference the commit sha1.  
* If the head points to a specific commit then it is called as detached head

## GIT Reset

* Term reset itself stands for undoing changes.
* Reset is often referred as confusing command.
* Reset does different thing in different contexts.
* It is used to move the branch.
* Reset moves the current branch and optionally copies the data from the repo to the working/staging areas.

### Reset has options

* --hard --> moves the files both to working are and staging area.
* --mixed --> moves the files only to stage area.(default option)
* --soft --> does not move the files.
