# Linux cmds cheat sheet

## File permissions

- ## [chmod](https://ss64.com/bash/chmod.html)

  change file read, write, execute for User, Group, Others

- ## [chown](https://ss64.com/bash/chown.html) (**_root only_**)

  change file ownership

- ## [chgrp](https://ss64.com/bash/chgrp.html) (**_root only_**)

  change file group ownership

- ## [useradd](https://ss64.com/bash/useradd.html) (**_root only_**)

  add new user

- ## [usermod](https://ss64.com/bash/usermod.html) (**_root only_**)

  modify a user

- ## [userdel](https://ss64.com/bash/userdel.html) (**_root only_**)

  delete a user

- ## [groupadd](https://ss64.com/bash/groupadd.html) (**_root only_**)

  add new group

- ## [groupdel](https://ss64.com/bash/groupdel.html) (**_root only_**)

  delete a group

- ## [su](https://ss64.com/bash/su.html) and [sudo](https://ss64.com/bash/sudo.html)

  switch user `$ su - anotherUser`
  and super user do `$ sudo apt update`

- ## [id](https://ss64.com/bash/id.html)

## Access Control List (ACL)

permission mechanism for file system

- ## setfacl
- ## getfacl

## Filters

- ## [cut](https://www.ss64.com/bash/cut.html)
  - cut with delimiter **_:_** and field **_6_** `$ cut -d: -f 6 file`
  - cut only 1st character `$ cut -c1 file`
  - cut first five characters `$ cut -c1-5 file`
- ## [awk](https://www.ss64.com/bash/awk.html)

  data extraction base on fields  
  the second argument is actually a function

  - extract column 1 of file `$ awk '{print $1}' file`
  - extract last column of file `$ awk '{print $NF}' file`
  - search for word "Jerry" `$ awk '/Jerry/ {print}' file` (use grep instead, seriously...)
  - extract by delimiter (or called field seperator) **_:_** `$ awk -F: '{print $1}' file`
  - replace word (syntax is a mess)
  - filter by string length of 15 `$ awk 'length($0) > 15' file`

- ## [grep](https://www.ss64.com/bash/grep.html)

  - normal usage `$ grep "searchterm" file`  
    or `$ grep searchterm file`
  - find and **_count_** `$ grep -c "searchterm" file`
  - case insensitive `$ grep -i "searchterm" file`
  - show line number `$ grep -n "searchterm" file`
  - except searchterm (invert match) `$ grep -v "searchterm" file`

- ## [egrep](https://www.ss64.com/bash/egrep.html)

  ##### usage same as grep

  - search for two searchterms `$ egrep "searchterm1|searchterm2" file`

- ## [sort](https://www.ss64.com/bash/sort.html)

  - sort by alphabetical order `$ sort file`
  - reverse sort `$ sort -r file`
  - sort by field number two `$ sort -k2 file`

- ## [uniq](https://www.ss64.com/bash/uniq.html) \* need to use with sort

  - normal usage `$ sort file | uniq`
  - count repeated `$ sort file | uniq -c`
  - only show repeated lines `$ sort file | uniq -d`

- ## [wc](https://www.ss64.com/bash/wc.html)
  word count
  - check all `$ wc file`
  - line count `$ wc -l file`
  - word count `$ wc -w file`
  - byte count `$ wc -b file`

## Combine and split

- ## [cat](https://www.ss64.com/bash/cat.html)
  concatenate `$ cat file1 file2 file3 > bundle`
- ## [split](https://www.ss64.com/bash/split.html)
  split file by 10 lines each `$ split -l 10 parentFile childFile`

## Zip and compression

- ## [tar](https://www.ss64.com/bash/tar.html)
  just put multiple files in one container/folder
  - put everything here in _file.tar_ `$ tar cvf file.tar .`  
    cvf is --create --label --file
  - extract everything `$ tar xvf file.tar`
- ## [gzip](https://www.ss64.com/bash/gzip.html)
  zip files, or preferably, zip a tar
  - zip file `$ gzip file.tar`
  - unzip file `$ gunzip file.tar` or `$ gzip -d file.tar`
- ## [bzip](https://www.ss64.com/bash/bzip.html)
  use gzip instead

## Others

- ## [whoami](https://www.ss64.com/bash/whoami.html)
  show user name, i.e. root
- ## [hosthame](https://linux.die.net/man/1/hostname)
  show or set the system's host name
- ## [pwd](https://ss64.com/bash/pwd.html)
  Print Working Directory
- ## [sed](https://ss64.com/bash/sed.html)
  Stream editor ( **_check `$ info sed` for other usage_** )
  - substitute `$ sed 's/original/replacement/g' file`  
    `/g` = global flag
    delete empty lines `$ sed '/^.$/d' file` (might not work)
  - use --in-place (or -i) flag to save the file `$ sed -i 's/original/replacement/g' file`
  - can also be written as
    - delete by line numbers: `$ sed '20d' file` and `$ sed '20,25d' file`
    - delete by regex `$ sed '/^foobar/d' file`
