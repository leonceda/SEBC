## <center> Challenge 2: Install Cloudera Manager 5.11.x (latest update)

* Create the Issue `Install CM`
* Assign yourself and label it `started`
* Install Cloudera Manager on the second node you listed in `0_setup.md`
* Copy the YUM command and output for installing Cloudera Manager in `challenges/labs/2_cm-install.md`
```
[centos@ip-172-31-26-93 ~]$ yum -y install cloudera-manager-server
Loaded plugins: fastestmirror, presto
You need to be root to perform this command.
[centos@ip-172-31-26-93 ~]$
[centos@ip-172-31-26-93 ~]$ sudo yum -y install cloudera-manager-server
Loaded plugins: fastestmirror, presto
Setting up Install Process
Loading mirror speeds from cached hostfile
 * base: ftp.heanet.ie
 * epel: mirrors.coreix.net
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
cloudera-manager                                                                 |  951 B     00:00
cloudera-manager/primary                                                         | 4.3 kB     00:00
cloudera-manager                                                                                    7/7
Resolving Dependencies
--> Running transaction check
---> Package cloudera-manager-server.x86_64 0:5.11.2-1.cm5112.p0.6.el6 will be installed
--> Processing Dependency: cloudera-manager-daemons = 5.11.2 for package: cloudera-manager-server-5.11.2-1.cm5112.p0.6.el6.x86_64
--> Running transaction check
---> Package cloudera-manager-daemons.x86_64 0:5.11.2-1.cm5112.p0.6.el6 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

========================================================================================================
 Package                       Arch        Version                          Repository             Size
========================================================================================================
Installing:
 cloudera-manager-server       x86_64      5.11.2-1.cm5112.p0.6.el6         cloudera-manager      8.5 k
Installing for dependencies:
 cloudera-manager-daemons      x86_64      5.11.2-1.cm5112.p0.6.el6         cloudera-manager      671 M

Transaction Summary
========================================================================================================
Install       2 Package(s)

Total download size: 671 M
Installed size: 826 M
Downloading Packages:
Setting up and reading Presto delta metadata
Processing delta metadata
Package(s) data still to download: 671 M
(1/2): cloudera-manager-daemons-5.11.2-1.cm5112.p0.6.el6.x86_64.rpm              | 671 MB     00:28
(2/2): cloudera-manager-server-5.11.2-1.cm5112.p0.6.el6.x86_64.rpm               | 8.5 kB     00:00
--------------------------------------------------------------------------------------------------------
Total                                                                    23 MB/s | 671 MB     00:28
Running rpm_check_debug
Running Transaction Test
Transaction Test Succeeded
Running Transaction
Warning: RPMDB altered outside of yum.
  Installing : cloudera-manager-daemons-5.11.2-1.cm5112.p0.6.el6.x86_64                             1/2
  Installing : cloudera-manager-server-5.11.2-1.cm5112.p0.6.el6.x86_64                              2/2
  Verifying  : cloudera-manager-server-5.11.2-1.cm5112.p0.6.el6.x86_64                              1/2
  Verifying  : cloudera-manager-daemons-5.11.2-1.cm5112.p0.6.el6.x86_64                             2/2

Installed:
  cloudera-manager-server.x86_64 0:5.11.2-1.cm5112.p0.6.el6

Dependency Installed:
  cloudera-manager-daemons.x86_64 0:5.11.2-1.cm5112.p0.6.el6

Complete!
```
