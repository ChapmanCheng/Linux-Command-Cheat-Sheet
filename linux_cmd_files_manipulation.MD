# Linux cmds cheat sheet

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

## Combine and split

- ## [cat](https://www.ss64.com/bash/cat.html)
  concatenate `$ cat file1 file2 file3 > bundle`
- ## [split](https://www.ss64.com/bash/split.html)
  split file by 10 lines each `$ split -l 10 parentFile childFile`
