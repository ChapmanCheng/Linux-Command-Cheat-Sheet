# Linux cmds cheat sheet - system utilities

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
