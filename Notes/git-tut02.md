# Notes - 02

## How GIT stores the data

* Git stores data in the form of keys and values.
* Values is nothing but the contents of file.
* Git calculates the hashes with SHA1 algorithm.
* SHA-1 (Secure Hash Algorithm 1) is a cryptographic hash function that produces a fixed-size 160-bit (20-byte) hash value.
* SHA1 is  20 bytes in hexadecimal format.
* Not only content the files, directories and so on commits has their own SHA-1
* Every object has its own SHA1

## Decode hash code

```git
    git cat-file <hash> -p
```

## Rename files

```git
    mv old_filename.txt new_filename.txt
```

## Restore file

* To only unstage a certain file and thereby undo a previous git add, you need to provide the --staged flag:

```git
    git restore --staged index.html
```

* You can of course also remove multiple files at once from the Staging Area:

```git
    git restore --staged *.css
```

* If you want to discard uncommitted local changes in a file, simply omit the --staged flag. Keep in mind, however, that you cannot undo this!

```git
    git restore index.html
```

Another interesting use case is to restore a specific historic revision of a file:

```git
    git restore --source 7173808e index.html
    git restore --source master~2 index.html
```

The first example will restore the file as it was in commit #7173808e, while the second one will restore it as it was "two commits before the current tip of the master branch".

```git
    <!-- To restore from staged area to working area -->
    git restore --staged file.txt

    <!-- To restore file content -->
    git restore file.txt
```
