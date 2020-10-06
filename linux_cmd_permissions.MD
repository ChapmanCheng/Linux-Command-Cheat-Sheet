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

## Access Control List (ACL)

permission mechanism for file system

- ## setfacl
- ## getfacl
