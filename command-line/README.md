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