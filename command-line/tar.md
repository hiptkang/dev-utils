# tar examples

## Uncompress

### basic

```sh
# .tar
tar -xvf $NAME.tar

# untar in different directory
tar -xvf $NAME.tar -C $DEST_DIR

# .tar.gz or .tar.bz2 (same as .tar)
tar -xvf $NAME.tar.gz
```

### untar specific files in the archive file

```sh
# .tar (two files)
tar -xvf $NAME.tar $FILE_NAME $DIR_NAME

# .tar (wildcard)
tar -xvf $NAME.tar '*.cpp"

# .tar.gz
tar -zxvf $NAME.tar.gz $FILE_NAME $DIR_NAME

# .tar.bz2
tar -jxvf $NAME.tar.gz $FILE_NAME $DIR_NAME
```

## Compress

### basic

```sh
# .tar (directories)
tar -cvf $NAME.tar $DIR1 $DIR2

# .tar.gz (directories)
tar -zcvf $NAME.tar.gz $DIR1 $DIR2

# .tar.bz2 (directories)
tar -jcvf $NAME.tar.bz2 $DIR1 $DIR2
```

### verify

```sh
# .tar
tar tvfW $NAME.tar

# .tar.gz or .tar.bz2
# NO with one tar command
```

### add files

```sh
# .tar
tar -rvf $NAME.tar $FILEs $DIRs

# .tar.gz or .tar.bz2
# NO with one tar command
```


## Misc.

### tar options

- c – create a archive file.
- x – extract a archive file.
- k – keep old files.
- v – show the progress of archive file.
- f – filename of archive file.
- t – viewing content of archive file.
- j – filter archive through bzip2.
- z – filter archive through gzip.
- r – append or update files or directories to existing archive file.
- W – Verify a archive file.
- wildcards – Specify patterns in unix tar command.

```sh
# list content
tar -tvf $FILE
```
### gzip

```sh
# tar.gz to tar
gzip -d test.tar.gz
```

### bzip2

```sh
# tar.bz2 to tar
bzip2 -d test.tar.bz2
```

