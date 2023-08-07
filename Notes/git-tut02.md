# Notes - 02

## How GIT stores the data

* Git stores data in the form of keys and values.
* Values is nothing but the contents of file.
* Git calculates the hashes with SHA1 algorithm.
* SHA-1 (Secure Hash Algorithm 1) is a cryptographic hash function that produces a fixed-size 160-bit (20-byte) hash value.
* SHA1 is  20 bytes in h exadecimal format.
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

```git
    <!-- To restore from staged area to working area -->
    git restore --staged file.txt

    <!-- To restore file content -->
    git restore file.txt
```
