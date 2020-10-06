# Linux cmds cheat sheet - permissions and users

## File Permissions

- ## [chmod](https://ss64.com/bash/chmod.html)

  change file read, write, execute for User, Group, Others

- ## [chown](https://ss64.com/bash/chown.html) (**_root only_**)

  change file ownership

- ## [chgrp](https://ss64.com/bash/chgrp.html) (**_root only_**)

  change file group ownership

## Admin on users

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

- ## [who](https://ss64.com/bash/who.html) and [w](https://ss64.com/bash/w.html)

  show who is logged in `$ who`  
  `w` shows what they are doing too

- ## [last](https://ss64.com/bash/last.html)

  show list of last logged in users

- ## [finger](https://ss64.com/bash/finger.html)

  need to install...

- ## [id](https://ss64.com/bash/id.html)

  show your user's id and group id `$ id`  
  or show another user's id and grp id `$ id anotherUser`

## root and others

- ## [su](https://ss64.com/bash/su.html) and [sudo](https://ss64.com/bash/sudo.html)

  switch user `$ su - username` or switch to root `$ su -`
  and super user do `$ sudo apt update`

- ## [whoami](https://www.ss64.com/bash/whoami.html)

  show your user name, i.e. root

- ## [hosthame](https://linux.die.net/man/1/hostname)

  show or set the system's host name

- ## [pwd](https://ss64.com/bash/pwd.html)

  Print Working Directory

## Communications between users

- ## [users](https://www.ss64.com/bash/users.html)

  shows list of logged in users

- ## [wall](https://www.ss64.com/bash/wall.html)

  send message to other users `$ wall` then enter your message

- ## [write](https://www.ss64.com/bash/write.html)

  write a message to specific userr `$ write username` then write message

## Access Control List (ACL)

permission mechanism for file system

- ## setfacl
- ## getfacl
