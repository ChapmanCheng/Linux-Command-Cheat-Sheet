# Linux cmds cheat sheet - shell scripting

## She-bang

`#!/bin/bash`

## Comments

`# This is a comment`

## Some commands use in shell scripts

- ## [sleep](https://www.ss64.com/bash/sleep.html)

  put machine to idle for specified seconds `$ sleep 10`

- ## [expr](https://www.ss64.com/bash/expr.html)

  evaluate expression, can be use for calculation

  - express boolean
    - `$ expr ARG1 | ARG2`
    - `$ expr ARG1 & ARG2`
    - `$ expr ARG1 > ARG2` or `$ expr ARG1 < ARG2`
    - `$ expr ARG1 >= ARG2` or `$ expr ARG1 <= ARG2`
    - `$ expr ARG1 = ARG2`
    - `$ expr ARG1 != ARG2`
  - express math
    - `$ expr ARG1 + ARG2`
    - `$ expr ARG1 - ARG2`
    - `$ expr ARG1 * ARG2`
    - `$ expr ARG1 / ARG2`
    - `$ expr ARG1 % ARG2`
  - either regex
    - `$ expr STRING : REGXP`
    - `$ expr match STRING REGXP`
    - `$ expr substr STRING REGXP`
    - `$ expr index STRING REGXP`
  - other
    - length of string `$ expr length STRING`

## Shell Scripts Syntax

- ## case statement (switch statment)

  ```
  case $choices in
  a) date ;;
  b) ls ;;
  c) who ;;
  d) uptime ;;
  *) echo Invalid choice - Bye ;;
  esac
  ```

- ## for loop

  ```
  for COLOR in red green blue
  do
    echo $COLOR
  done
  ```

- ## if else

  ```
  if [ #bool ]
  then
    ---
  elif [ #bool ]
    ---
  else
    ---
  fi
  ```

  ### File test Operators

  | operators | meaning                                                                              |
  | --------- | ------------------------------------------------------------------------------------ |
  | -e        | file exists                                                                          |
  | -a        | file exists                                                                          |
  | -f        | file is a regular file (not a directory or device file)                              |
  | -s        | file is not zero size                                                                |
  | -d        | file is a directory                                                                  |
  | -b        | file is a block device                                                               |
  | -c        | file is a character device                                                           |
  | -p        | file is a pipe                                                                       |
  | -h        | file is a symbolic link                                                              |
  | -L        | file is a symbolic link                                                              |
  | -S        | file is a socket                                                                     |
  | -t        | file (descriptor) is associated with a terminal device                               |
  | -r        | file has read permission (for the user running the test)                             |
  | -w        | file has write permission (for the user running the test)                            |
  | -x        | file has execute permission (for the user running the test)                          |
  | -g        | set-group-id (sgid) flag set on file or directory                                    |
  | -u        | set-user-id (suid) flag set on file                                                  |
  | -k        | sticky bit set                                                                       |
  | -O        | you are owner of file                                                                |
  | -G        | group-id of file same as yours                                                       |
  | -N        | file modified since it was last read                                                 |
  | f1 -nt f2 | file f1 is newer than f2                                                             |
  | f1 -ot f2 | file f1 is older than f2                                                             |
  | f1 -ef f2 | files f1 andf2 are hard links to the same file                                       |
  | !         | \"not\" -- reverses the sense of the tests above (returns true if condition absent). |

  ### Integers Operators

  | operators | meaning                                                     |
  | --------- | ----------------------------------------------------------- |
  | -eq       | is equal to                                                 |
  | -ne       | is not equal to                                             |
  | -gt       | is greater than                                             |
  | -ge       | is greater or euqal to                                      |
  | -lt       | is less than                                                |
  | -le       | is less than or equal to                                    |
  | <         | is less than ( **within double parentheses**)               |
  | <=        | is less than or equal to ( **within double parentheses**)   |
  | >         | is greater than ( **within double parentheses**)            |
  | >=        | is greater than or equal to ( **within double parenthese**) |

  ### String Operators

  | operators | meaning                                               |
  | --------- | ----------------------------------------------------- |
  | =         | is equal to                                           |
  | ==        | is equal to (**behaves differently**)                 |
  | !=        | is not equal to                                       |
  | <         | is less than, in ASCII alphabetical order             |
  | >         | is less than or equal to, in ASCII alphabetical order |
  | -z        | is null or zero length                                |
  | -n        | is not null                                           |

- ## Alias

  set alias `$ alias ph="pwd; hostname"`  
  unset alias `$ unalias ph`

  to create permanent alias, set in these files

  - user alias  
    `/home/user/.bashrc`
  - global alias  
    `/etc/bashrc/`
