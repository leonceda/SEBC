hallenge Setup

* Create the Issue `Challenges Setup`
* Verify `mfernest` and `cfusi` are Collaborators
* If you re-taking the challenge, make sure your GitHub labels have been configured
* Assign the Issue to yourself and label it `started`
* In the file `challenges/labs/0_setup.md`:
  * List the cloud provider you are using (AWS, GCE, Azure, CloudCat, other)
```
AWS
```
  * List your instances by IP address and DNS name (don't use `/etc/hosts` for this)
```
ip-172-31-28-78.eu-west-1.compute.internal |
ip-172-31-28-78.eu-west-1.compute.internal has address 172.31.28.78

ip-172-31-24-17.eu-west-1.compute.internal |
ip-172-31-24-17.eu-west-1.compute.internal has address 172.31.24.17

ip-172-31-23-131.eu-west-1.compute.internal |
ip-172-31-23-131.eu-west-1.compute.internal has address 172.31.23.131

ip-172-31-24-18.eu-west-1.compute.internal |
ip-172-31-24-18.eu-west-1.compute.internal has address 172.31.24.18

ip-172-31-25-228.eu-west-1.compute.internal | 
ip-172-31-25-228.eu-west-1.compute.internal has address 172.31.25.228
```
  * List the Linux release you are using 
```
[centos@ip-172-31-25-228 ~]$ cat /etc/redhat-release
CentOS release 6.9 (Final)
```
  * List the file system capacity for the first node 
```
[centos@ip-172-31-25-228 ~]$ df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       50G  2.8G   44G   6% /
tmpfs           7.8G     0  7.8G   0% /dev/shm
/dev/xvdb        99G   60M   99G   1% /data/00
```
  * List the command and output for `yum repolist enabled` 
```
ip-172-31-28-78.eu-west-1.compute.internal | SUCCESS | rc=0 >>
Loaded plugins: fastestmirror, presto
Determining fastest mirrors
 * base: ftp.heanet.ie
 * epel: s3-mirror-eu-west-1.fedoraproject.org
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
repo id          repo name                                                status
base             CentOS-6 - Base                                           6,706
epel             Extra Packages for Enterprise Linux 6 - x86_64           12,467
extras           CentOS-6 - Extras                                            52
updates          CentOS-6 - Updates                                          950
repolist: 20,175

ip-172-31-24-17.eu-west-1.compute.internal | SUCCESS | rc=0 >>
Loaded plugins: fastestmirror, presto
Determining fastest mirrors
 * base: ftp.heanet.ie
 * epel: mirror.freethought-internet.co.uk
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
repo id          repo name                                                status
base             CentOS-6 - Base                                           6,706
epel             Extra Packages for Enterprise Linux 6 - x86_64           12,467
extras           CentOS-6 - Extras                                            52
updates          CentOS-6 - Updates                                          950
repolist: 20,175

ip-172-31-23-131.eu-west-1.compute.internal | SUCCESS | rc=0 >>
Loaded plugins: fastestmirror, presto
Determining fastest mirrors
 * base: ftp.heanet.ie
 * epel: mirror.freethought-internet.co.uk
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
repo id          repo name                                                status
base             CentOS-6 - Base                                           6,706
epel             Extra Packages for Enterprise Linux 6 - x86_64           12,467
extras           CentOS-6 - Extras                                            52
updates          CentOS-6 - Updates                                          950
repolist: 20,175

ip-172-31-24-18.eu-west-1.compute.internal | SUCCESS | rc=0 >>
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

ip-172-31-25-228.eu-west-1.compute.internal | SUCCESS | rc=0 >>
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
  * User `hilary` with a UID of `2800`
  * User `anupam` with a UID of `2900`
  * Create the group `analytics` and add `anupam` to it
  * Create the group `datasci` and add `hilary` to it
* List the `/etc/passwd` entries for `hilary` and `anupam` 
  * Do not list the entire file
```
$  egrep 'hilary|anupam' /etc/passwd
ip-172-31-28-78.eu-west-1.compute.internal | 
hilary:x:2800:2800::/home/hilary:/bin/bash
anupam:x:2900:2900::/home/anupam:/bin/bash

ip-172-31-24-18.eu-west-1.compute.internal |
hilary:x:2800:2800::/home/hilary:/bin/bash
anupam:x:2900:2900::/home/anupam:/bin/bash

ip-172-31-24-17.eu-west-1.compute.internal | 
hilary:x:2800:2800::/home/hilary:/bin/bash
anupam:x:2900:2900::/home/anupam:/bin/bash

ip-172-31-23-131.eu-west-1.compute.internal | 
hilary:x:2800:2800::/home/hilary:/bin/bash
anupam:x:2900:2900::/home/anupam:/bin/bash

ip-172-31-25-228.eu-west-1.compute.internal | 
hilary:x:2800:2800::/home/hilary:/bin/bash
anupam:x:2900:2900::/home/anupam:/bin/bash
```
* List the `/etc/group` entries for `analytics` and `datasci` 
  * Do not list the entire file
```
$ egrep 'analytics|datasci' /etc/group

ip-172-31-24-18.eu-west-1.compute.internal | 
analytics:x:2901:anupam
datasci:x:2902:hilary

ip-172-31-28-78.eu-west-1.compute.internal | 
analytics:x:3003:anupam
datasci:x:3004:hilary

ip-172-31-24-17.eu-west-1.compute.internal | 
analytics:x:3003:anupam
datasci:x:3004:hilary

ip-172-31-23-131.eu-west-1.compute.internal | 
analytics:x:3003:anupam
datasci:x:3004:hilary

ip-172-31-25-228.eu-west-1.compute.internal |
analytics:x:2901:anupam
datasci:x:2902:hilary
```
* Push these updates to GitHub 
* Label your Issue `review` 
* Assign the Issue to the instructor
