# Linux commands cheatsheet - ssh

## SSH (Secure shell)

### for detailed docs of the cli interface, checkout the [official documents](https://www.ssh.com/ssh/command/)

- ## [ssh](https://www.ss64.com/bash/ssh.html)

  use **username@hostname** or **username@ip_address**
  `$ ssh chap@192.107.0.1`  
  execute a command on remote server
  `$ ssh chap@192.107.0.1 ls /etc/httpd/`

  > others: [command line options](https://www.ssh.com/ssh/command/#ssh-command-line-options)

- ## [ssh-keygen](https://www.ss64.com/bash/ssh-keygen.html)

  generate new key pairs in _~/.ssh/_

  - use rsa algorithms `$ ssh-keygen -t rsa`
  - use bit rate 4096 (recommanded) `$ssh-keygen -b 4096`
  - lastest algo is ecdsa w/ **521** bits

  > others:
  > [command line options](https://www.ssh.com/ssh/keygen/#command-and-option-summary),
  > [keys and algorithms](https://www.ssh.com/ssh/keygen/#choosing-an-algorithm-and-key-size)

- ## [ssh-copy-id](https://www.ssh.com/ssh/copy-id)

  install public key to the server as authorized key  
   `$ ssh-copy-id -i ~/.ssh/id_rsa user@host`  
   or just `cat` the public key's content into `root@server $ ~/.ssh/authorized_keys`

  > others: [command line options](https://www.ssh.com/ssh/copy-id#command-line-options)

- ## [ssh-add](https://www.ss64.com/bash/ssh-add.html)

  ssh-add is a command for adding SSH private keys into the  
  **SSH** authentication **agent** for implementing single sign-on with SSH.

  - simple add key cmc `$ ssh-add ~/.ssh/id_rsa`
  - if has pass phrase, will ask for past phrase

  > others: [command line options](https://www.ssh.com/ssh/add#ssh-add-command-line-options)  
  > **BEWARE**: ssh-add is will be lost after session or shutdown

- ## [scp](https://www.ss64.com/bash/scp.html)

  secure shell _cp (copy command)_

  - copy to `$ scp file host:path`
  - copy from `$scp host:file`  
    e.g. `\$ scp ~/Document/text.conf 192.160.0.101:/etc/conf/text.conf`
  - copy dir recursively `$ scp -r dir host:path`

- ## sftp

  just use **_scp_**

- ## put public key in remote servers

  append your keys in `$cat id_rsa.pub >> ~/.ssh/authorized_keys`

- ## remote files permissions

  `~/.ssh/` is set as _drwx------_ (700)  
  `~/.ssh/*` everything else is set as _-rw-------_ (600)

- ## edit ssh configs

  go to ` /etc/ssh/sshd_config`, see official documents for additioanl settings
