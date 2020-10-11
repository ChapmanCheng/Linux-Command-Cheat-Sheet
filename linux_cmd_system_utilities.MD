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

  System Control

  - start/stop service
    - `$ systemctl start service-name`
    - `$ systemctl stop service-name`
    - `$ systemctl restart service-name`
  - start/stop service at boot-time
    - `$ systemctl enable service-name`
    - `$ systemctl disable service-name`
  - show service current status `$ systemctl status service-name`

- ## Display Process

  - ## [ps](https://www.ss64.com/bash/ps.html)

    list running process

    - dunno the functions `$ ps -ef`

  - ## [top](https://www.ss64.com/bash/top.html)

    display process and computer status

  - ## [df](https://www.ss64.com/bash/df.html)

    show disk usage `$ df -h` with human readable memory size

  - ## [dmseg](https://www.ss64.com/bash/dmseg.html)

    show system error messages

  - ## iostat <span style="color: red;"> \* not support on 20.04 </span>
    show input and ouput stats  
    to refresh the stat every one second `$iostat 1`
  - ## netstat <span style="color: red;"> \* not support on 20.04 </span>
    show network information `$ netstat -rnv`
  - ## free
    show ram memroy
  - ## read cpu info - `cat /proc/cpuinfo`
  - ## read memory info - `cat /proc/meminfo`

- ## Kill Process

  - ## [kill](https://www.ss64.com/bash/kill.html)

    kill a process `$ kill 1234` with a given PID (process ID)

    ##### (similar to `$ systemctl stop service`)

  - ## [killall](https://www.ss64.com/bash/killall.html)

    kill all process under the same service `$ killall firefox`

  - ## [pkill](https://www.ss64.com/bash/pkill.html)

    kill process by name `pkill top`

- ## Background and Foreground and Priority

  - ## [jobs](https://www.ss64.com/bash/jobs.html)

    show current jobs in terminal session

  - ## [fg](https://www.ss64.com/bash/fg.html)

    push _job_ to **Foreground** `$ fg PID` or `$ fg`

  - ## [bg](https://www.ss64.com/bash/bg.html)

    move _job_ to **Background** `$ bg PID` or `$ bg`

  - ## [nice](https://www.ss64.com/bash/nice.html)

    process priority `$nice -n 5 PROCESS`
    or just get a better computer

- ## [nohup](https://www.ss64.com/bash/nohup.html)

  don't stop process even after terminal closed `$ nohup COMMAND &`

## Cronjobs

- ## [crontab](https://www.ss64.com/bash/crontab.html)
  edit a cronjob `$ crontab -e ` to enter a vi editor  
  list all cronjob `$ crontab -l`
  ##### get instruction from [crontab guru](https://crontab.guru/) or any other sites
- ## do hourly / daily / weekly / monthly cronjobs

  go to `/etc/cron.daily || cron.hourly || cron.weekly || cron.monthly`, add scripts to create conjob

  ##### daily/weekly/monthly store in `/etc/anacrontab`

  ##### hourly store in `/etc/cron.d/anacron`

## System Maintenence

- ## shutdown
  use `$ shutdown now` for immediate shutdown
- ## init [1..6]
  run `$ man init` for more info
- ## reboot
  alias to `$ shutdown -r`
- ## halt
  alias to `$ shutdown -H`
- ## [hostnamectl](https://www.ss64.com/bash/hostnamectl.html)
  set a new hostname to computer `$ hostnamectl set-hostname NEWNAME`  
  or edit in `/etc/hostname`
- ## Recover root password
  [check video](https://udemy.com/course/complete-linux-training-course-to-get-your-dream-it-job/learn/lecture/9848206)
- ## [sosreport](https://access.redhat.com/solutions/3592) <span style="color: red;">Redhat only</span>

## System Information

you can find system information in `$ cat /etc/os-release` or `$ cat /etc/redhat-release` etc.

- ## [uname](https://www.ss64/bash/uname.html)

  print system information  
  print all with `$ uname -a`

- ## [dmidecode](https://www.ss64/bash/dmidecode.html)

  prints super detail information w/ bios `$ sudo dmidecode`

- ## [arch](https://www.ss64/bash/arch.html)
  show system architecture

## Environment variables

- ## to view all env `$ printenv` or `$ env`
- ## to view one env `$ echo $SHELL`
- ## set a env variable in this session `$ export MY_VAR=foobar`
- ## set user variable permanantly in `~/.bashrc` file
- ## set global variable permanantly in `/etc/profile` or `/etc/bashrc` file

## Other

- ## `clear` - clears your screen
- ## `exit` - exit shell/terminal session
- ## [script](https://www.ss64.com/bash/script.html)
  record a log of your inputs in the terminal session `$ script FILENAME.log`  
  to exit, use `$ exit` to get out of the concurrent job

## Log Monitoring

- Log Directory Location `$ cd /var/log`
- `/var/log/boot.log` show bootup log files
- chronyd (replacement of NTP services)
- `/var/log/message` show <span style="color: red;"> !!! all hardware/software/application/prcoess infos <span>
- `/var/log/cron` show executed cronjogs
- `/var/log/dmesg` show error message, same as `$ dmesg`
- `/var/log/maillog` show send/receive mails logs, good for troubleshooting
- `/var/log/secure` show users logged in, failed logged in, and from where
- `/var/log/httpd` show apache logs

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
