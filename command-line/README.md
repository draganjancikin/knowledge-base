# Command Line Basics

## Moving Around the Command Line

<https://drupalize.me/videos/moving-around-command-line?p=1149>

```bash
# to print working directory
$ pwd

# to listing things
$ ls

# to listing thing by page, hit the space bar to go on the netx page, and at the end hit q to exit from last page
$ ls | less

# to listing everything, and gave you more information
$ ls -al

# to changing directory
$ cd directory_name

# to back to up directory
$ cd ..

# to back to home directory
$ cd ~
# or
$ cd

# go to root directory
$ cd /

# go to one level up 
$ cd ../directory_name/

# go to apsolute path
$ cd /directory_name/sub_directory_name/sub_sub_directory_name/

# get manual of particular command
$ man command_name

# to clear command prompt
$ clear
```

Hint 1: Start typing and then hit Tab button and command prompt will be complete thing. If exist more then one thing with same letters hit Tab button again and will be apear all things with same letter.

Hint 2: Case sensitive is important.

## Copy, Move, Delete on Command Line

<https://drupalize.me/videos/copy-move-delete-command-line?p=1149>

### Make a new File and Directory

```bash
# make a new file
$ touch file_name

# make a new directory
$ mkdir dir_name
```

### Copy

```bash
# copy file to new one
$ cp dir_name/file_name another_dir_name

# copy directory dir_name to new one dir_name_of_new_dir
$ cp -r dir_name/ dir_name_of_new_dir
```

### Move

```bash
# move file from one directory to another
$ mv dir_name/file_name another_dir_name

# move file to directory level up
$ mv dir_name/file_name ../another_dir_name

# move all file that begin with some charachters
$ mv 0* dir_name

# rename file with mv command
$ mv file_name new_file_name
```

### Delete

```bash
# remove file
$ rm file_name

# remove directory
$ rm -r dir_name
```

## Dealing with Command Line Permissions

```bash
# After typing command
$ ls -al
```

```bash
# Get on screen something like this:
drwxr-xr-x 5 dragan dragan 4096 мар 21 14:51 .
drwxr-xr-x 9 dragan dragan 4096 мар 21 14:50 ..
drwxr-xr-x 2 dragan dragan 4096 мар 21 14:51 dir_1
drwxr-xr-x 2 dragan dragan 4096 мар 21 14:51 dir_2
drwxr-xr-x 2 dragan dragan 4096 мар 21 14:51 dir_3
-rw-r--r-- 1 dragan dragan    0 мар 21 14:51 file_1
-rw-r--r-- 1 dragan dragan    0 мар 21 14:51 file_2
-rw-r--r-- 1 dragan dragan    0 мар 21 14:51 file_3
```

The first charachter is type (d)
Next three charachter is permissons for user (rwx)
Next three charachter is permissons for group (r-x)
And last three charachter is permissons for everybody else (r-x)

"d" - directory
"r" - read
"w" - write
"x" - execute

### Change Permissions

```bash
# remove permissons
$ chmod [param_one]-[param_two] file_name

# add permissons
$ chmod [param_one]+[param_two] file_name

# set permissions
$chmod a=r file_name
```

Param one:

* u - user
* g - group
* o - other
* a - all

Param two is "r" or "w" or "x".

### Change Ownership

Super User Do - sudo

```bash
# change ownership on the file with sudo
$ sudo chown user_name file_name

# change user and group ownership
$ sudo chmod user_name:group_name file_name
```

## Using Zip and Tar on Command Line

```bash
# create zip file
$ zip name_of_zip_file.zip name_of_file_that_zipped

# unzip
$ unzip name_of_zip_file.zip

# create gzip file
$ gzip name_of_file_that_zipped

# gunzip, after gunzip gzip file is gone
$ gunzip name_of_gzip_file.gz

```

### Archieving with Tar

```bash
# tar
$ tar -cvf name_of_new_file.tar [list of file]

# untar
$ tar -xvf name_of_tar_file.tar

# archieving and compresion (use gzip)
$ tar -cvzf name_of_new_file.tgz [list of file]

# unzip
$tar -xvzf name_of_tgz_file.tgz
```

"c" - create
"v" - verbose
"f" - file
