**Setup:**
  * 5 nodes of CentOS-6.5-GA-03.3-f4325b48-37b0-405a-9847-236c64622e3e-ami-6be4dc02.2 (ami-42718735), region _us-west-2a_
  * Linux Release
```
[root@ip-172-31-10-254 ~]# cat /etc/redhat-release
CentOS release 6.5 (Final)
```
  * Disks on machines
```
[root@ip-172-31-10-254 ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde       7.9G  749M  6.8G  10% /
tmpfs           7.4G     0  7.4G   0% /dev/shm
/dev/xvdg        99G  188M   94G   1% /opt/cloudera
/dev/xvdf        20G  172M   19G   1% /var/log/app

```

  * Yum repo list output
```
[root@ip-172-31-10-254 ~]# yum repolist enabled
Loaded plugins: fastestmirror, presto
Loading mirror speeds from cached hostfile
 * base: ftp.heanet.ie
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
repo id                   repo name                            status
base                      CentOS-6 - Base                      6,706
extras                    CentOS-6 - Extras                       45
updates                   CentOS-6 - Updates                     354
repolist: 7,105
```

  * Adding Linux Users and Groups
```
[root@ip-172-31-10-254 ~]# useradd raffles -u 2000
[root@ip-172-31-10-254 ~]# useradd fullerton -u 2000
useradd: UID 2000 is not unique
[root@ip-172-31-10-254 ~]# useradd fullerton -u 3000
[root@ip-172-31-10-254 ~]# groupadd hotels
[root@ip-172-31-10-254 ~]# groupadd shops
[root@ip-172-31-10-254 ~]#  usermod -a -G hotels fullerton
[root@ip-172-31-10-254 ~]#  usermod -a -G shops raffles
```
  * List Users
```
[root@ip-172-31-10-254 ~]# egrep "statler|waldorf" /etc/passwd
[root@ip-172-31-10-254 ~]# egrep "raffles|fullerton" /etc/passwd
raffles:x:2000:2000::/home/raffles:/bin/bash
fullerton:x:3000:3000::/home/fullerton:/bin/bash
[root@ip-172-31-10-254 ~]# egrep "hotels|shops" /etc/group
hotels:x:3001:fullerton
shops:x:3002:raffles

```
