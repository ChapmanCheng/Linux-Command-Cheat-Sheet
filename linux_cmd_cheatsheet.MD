# Linux cmds cheat sheet

## File permissions

- ## [chmod](https://ss64.com/bash/chmod.html)

  change file read, write, execute for User, Group, Others

- ## [chown](https://ss64.com/bash/chown.html) (**_root only_**)

  change file ownership

- ## [chgrp](https://ss64.com/bash/chgrp.html) (**_root only_**)

  change file group ownership

## Access Control List (ACL)

permission mechanism for file system

- ## setfacl
- ## getfacl

## SSH (Secure shell)

- ## [ssh](https://www.ss64.com/bash/ssh.html)
  i.e. `ssh root@192.107.0.1`
- ## [ssh-keygen](https://www.ss64.com/bash/ssh-keygen.html)
  generate new key pairs in _~/.ssh/_
- ## [ssh-add](https://www.ss64.com/bash/ssh-add.html)
  add private keys to current computer after ssh-keygen
- ## [scp](https://www.ss64.com/bash/scp.html)
  secure shell _copy_

## Show Files

- ## [cat](https://www.ss64.com/bash/cat.html)
- ## [head](https://www.ss64.com/bash/head.html)
  to show 5 lines `head -5` or `head -n 5`
- ## [tail](https://www.ss64.com/bash/tail.html)
  to show 5 lines `tail -5` or `tail -n 5`

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

## Zip and compression

- ## [tar](https://www.ss64.com/bash/tar.html)
- ## [gzip](https://www.ss64.com/bash/gzip.html)
- ## [gzip](https://www.ss64.com/bash/gzip.html)

## Others

- ## [whoami](https://www.ss64.com/bash/whoami.html)
  show user name, i.e. root
- ## [hosthame](https://linux.die.net/man/1/hostname)
  show or set the system's host name
- ## [pwd](https://ss64.com/bash/pwd.html)
  Print Working Directory
