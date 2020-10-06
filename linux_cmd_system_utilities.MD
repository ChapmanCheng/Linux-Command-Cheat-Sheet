# Linux cmds cheat sheet - system utilities

## Basic

- ## [whoami](https://www.ss64.com/bash/whoami.html)

  show your user name, i.e. root

- ## [hosthame](https://linux.die.net/man/1/hostname)

  show or set the system's host name

- ## [pwd](https://ss64.com/bash/pwd.html)

  Print Working Directory

- ## [date](https://www.ss64.com/bash/date.html)

  show date

- ## [uptime](https://www.ss64.com/bash/uptime.html)

  show 1. system time, 2. how long your computer is running, 3. number of users 4. load average

- ## [hostname](https://www.ss64.com/bash/hostname.html)

  show the computer's name

- ## [uname](https://www.ss64.com/bash/uname.html)

  print system information, use `$ uname --all` to show all infos

- ## [which](https://www.ss64.com/bash/which.html)

  show command's path `$ which pwd`

- ## [cal](https://www.ss64.com/bash/cal.html)

  show calendar, or show a given date `$ cal 6 1989`

- ## [bc](https://www.ss64.com/bash/bc.html)

  binary calculator

## Process and jobs

- ## [systemctl](https://www.ss64.com/bash/systemctl.html)
- ## [ps](https://www.ss64.com/bash/ps.html)
- ## [kill](https://www.ss64.com/bash/kill.html)
- ## [killall](https://www.ss64.com/bash/killall.html)
- ## [top](https://www.ss64.com/bash/top.html)
- ## [at](https://www.ss64.com/bash/at.html)

## Cronjobs

- ## [crontab](https://www.ss64.com/bash/crontab.html)

## System Monitoring

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
