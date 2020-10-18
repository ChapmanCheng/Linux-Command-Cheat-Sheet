# Linux cmds cheat sheet - shell scripting

## Configuration

- `/etc/nsswitch.conf`
- `/etc/hosts` - a self dns server
- `/etc/hostname` show computer(host) name

- ## [ping](https://ss64.com/bash/ping.html)

  send request to network host

- ## [curl](https://curl.haxx.se/docs/manual.html)

  ping a address, and much more

  ##### require download

- ## [ip address](https://ss64.com/bash/ip.html) or just `ip a`

  replace `$ ifconfig` command

- ## [tcpdump](https://ss64.com/bash/tcpdump.html)

  shows network leaning and coming into machine

- ## [wget](https://ss64.com/bash/wget.html)

  download files/packages/dependencies by `$ wget http://www.file.path/temp.zip`

- ## [nslookup](https://linux.die.net/man/1/nslookup)

  query internet name servers interactively (can get ip address)

  ```
  $ nslookup
  > google.com

  Server:		127.0.0.53
  Address:	127.0.0.53#53

  Non-authoritative answer:
  Name:	google.com
  Address: 172.217.24.206
  Name:	google.com
  Address: 2404:6800:4005:808::200e

  ```

  or run `$ nslookup google.com`

  > `Server` and `Address` are resolver to local machine DNS (Domain Name System) on modem
  > `Non-authoritative answer` is when local machine doesn't have that domain name, and went out to look for google.com

- ## [dig](https://linux.die.net/man/1/dig)

  another query internet servers, newer than `nslookup`  
  usage: `$ dig facebook.com`

- ## chronyd <span style="color: red;">Require install</span>

  Time synchronization service

  - config file: `/etc/chronyd.conf`
  - log fille: `/var/log/chrony`
  - service: `$ systemctl start/restant/enable chronyd`
  - command: `$chronyc`

  older version can use `ntp` (Network Time Protocal)

- ## [iptables]()

  administration tool for IPv4/IPv6 packet filtering and NAT

- ## [tracepath]()(ubuntu) and [traceroute]()
  map packets of data from source to destination. Can locate data loss that signify network node is down  
  usage: `$ tracepath google.com`
