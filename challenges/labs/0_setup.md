hallenge Setup

* Create the Issue `Challenges Setup`
* Make sure `mfernest` and `alexciobanu` are Collaborators
* Assign the Issue to yourself and label it `started`
* In the file `challenges/labs/0_setup.md`:
  * List the cloud provider you are using 
```
AWS
```
  * List your instances by IP address and DNS name (don't use `cat /etc/hosts` table for this)
```
ip-172-31-16-160.eu-west-1.compute.internal |
ip-172-31-16-160.eu-west-1.compute.internal has address 172.31.16.160

ip-172-31-18-25.eu-west-1.compute.internal | 
ip-172-31-18-25.eu-west-1.compute.internal has address 172.31.18.25

ip-172-31-22-249.eu-west-1.compute.internal | 
ip-172-31-22-249.eu-west-1.compute.internal has address 172.31.22.249

ip-172-31-17-134.eu-west-1.compute.internal | 
ip-172-31-17-134.eu-west-1.compute.internal has address 172.31.17.134

ip-172-31-26-93.eu-west-1.compute.internal | 
ip-172-31-26-93.eu-west-1.compute.internal has address 172.31.26.93

```

  * List the Linux release you are using 
```
[centos@ip-172-31-17-134 ~]$ cat /etc/redhat-release
CentOS release 6.9 (Final)

```

  * List the file system capacity for the first node 
```
[centos@ip-172-31-17-134 ~]$ df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       50G  2.8G   44G   6% /
tmpfs           7.8G     0  7.8G   0% /dev/shm
/dev/xvdb        99G   60M   99G   1% /data/00

```

  * List the command and output for `yum repolist enabled` 
```
ip-172-31-18-25.eu-west-1.compute.internal | 
Loaded plugins: fastestmirror, presto
Loading mirror speeds from cached hostfile
 * base: ftp.heanet.ie
 * epel: ftp.heanet.ie
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
repo id          repo name                                                status
base             CentOS-6 - Base                                           6,706
epel             Extra Packages for Enterprise Linux 6 - x86_64           12,467
extras           CentOS-6 - Extras                                            52
updates          CentOS-6 - Updates                                          950
repolist: 20,175

ip-172-31-22-249.eu-west-1.compute.internal | 
Loaded plugins: fastestmirror, presto
Loading mirror speeds from cached hostfile
 * base: ftp.heanet.ie
 * epel: ftp.heanet.ie
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
repo id          repo name                                                status
base             CentOS-6 - Base                                           6,706
epel             Extra Packages for Enterprise Linux 6 - x86_64           12,467
extras           CentOS-6 - Extras                                            52
updates          CentOS-6 - Updates                                          950
repolist: 20,175

ip-172-31-16-160.eu-west-1.compute.internal | 
Loaded plugins: fastestmirror, presto
Loading mirror speeds from cached hostfile
 * base: ftp.heanet.ie
 * epel: ftp.heanet.ie
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
repo id          repo name                                                status
base             CentOS-6 - Base                                           6,706
epel             Extra Packages for Enterprise Linux 6 - x86_64           12,467
extras           CentOS-6 - Extras                                            52
updates          CentOS-6 - Updates                                          950
repolist: 20,175

ip-172-31-17-134.eu-west-1.compute.internal | 
Loaded plugins: fastestmirror, presto
Loading mirror speeds from cached hostfile
 * base: ftp.heanet.ie
 * epel: mirrors.coreix.net
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
repo id          repo name                                                status
base             CentOS-6 - Base                                           6,706
epel             Extra Packages for Enterprise Linux 6 - x86_64           12,467
extras           CentOS-6 - Extras                                            52
updates          CentOS-6 - Updates                                          950
repolist: 20,175

ip-172-31-26-93.eu-west-1.compute.internal |
Loaded plugins: fastestmirror, presto
Loading mirror speeds from cached hostfile
 * base: ftp.heanet.ie
 * epel: mirrors.coreix.net
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
repo id          repo name                                                status
base             CentOS-6 - Base                                           6,706
epel             Extra Packages for Enterprise Linux 6 - x86_64           12,467
extras           CentOS-6 - Extras                                            52
updates          CentOS-6 - Updates                                          950
repolist: 20,175
```

* Add the following Linux accounts to all nodes
  * User `driscoll` with a UID of `2650`
  * User `bartfeld` with a UID of `3100`
  * Create the group `intl` and add `bartfeld` to it
  * Create the group `americas` and add `driscoll` to it
* List the `/etc/passwd` entries for `driscoll` and `bartfeld` 
  * Do not list the entire file
```

``@ip-172-31-26-93 ~]$ for i in $(cat hosts); do ssh -i .ssh/mysshkey.pem $i hostname -f && sudo cat /etc/passwd | egrep 'driscoll|bartfeld';done

ip-172-31-17-134.eu-west-1.compute.internal
driscoll:x:2650:2650::/home/driscoll:/bin/bash
bartfeld:x:3100:3100::/home/bartfeld:/bin/bash

ip-172-31-16-160.eu-west-1.compute.internal
driscoll:x:2650:2650::/home/driscoll:/bin/bash
bartfeld:x:3100:3100::/home/bartfeld:/bin/bash

ip-172-31-26-93.eu-west-1.compute.internal
driscoll:x:2650:2650::/home/driscoll:/bin/bash
bartfeld:x:3100:3100::/home/bartfeld:/bin/bash

ip-172-31-22-249.eu-west-1.compute.internal
driscoll:x:2650:2650::/home/driscoll:/bin/bash
bartfeld:x:3100:3100::/home/bartfeld:/bin/bash

ip-172-31-18-25.eu-west-1.compute.internal
driscoll:x:2650:2650::/home/driscoll:/bin/bash
bartfeld:x:3100:3100::/home/bartfeld:/bin/bash
```

* List the `/etc/group` entries for `intl` and `americas` 
  * Do not list the entire file
```
[centos@ip-172-31-26-93 ~]$ for i in $(cat hosts); do ssh -i .ssh/mysshkey.pem $i hostname -f && sudo cat /etc/group | egrep 'intl|americas';done
ip-172-31-17-134.eu-west-1.compute.internal
intl:x:3101:bartfeld
americas:x:3102:driscoll

ip-172-31-16-160.eu-west-1.compute.internal
intl:x:3101:bartfeld
americas:x:3102:driscoll

ip-172-31-26-93.eu-west-1.compute.internal
intl:x:3101:bartfeld
americas:x:3102:driscoll

ip-172-31-22-249.eu-west-1.compute.internal
intl:x:3101:bartfeld
americas:x:3102:driscoll

ip-172-31-18-25.eu-west-1.compute.internal
intl:x:3101:bartfeld
americas:x:3102:driscoll
```

* Push these updates to GitHub 
* Label your Issue `review` 
* Assign the Issue to the instructor

