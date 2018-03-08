* Create the Issue `Install Database` 
* Assign the Issue to yourself and label it `started`
* Install the server on the first node you listed in `0_setup.md`
  * Use a YUM repository to install the package
  * Copy the YUM install command and output to `challenges/labs/1_database-server-install.md`

```
[centos@ip-172-31-17-134 SEBC]$ sudo yum -y install mysql-community-server
Loaded plugins: fastestmirror, presto
Setting up Install Process
Loading mirror speeds from cached hostfile
 * base: ftp.heanet.ie
 * epel: mirrors.coreix.net
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
mysql55-community                                                                                                                                                                           | 2.5 kB     00:00
Resolving Dependencies
--> Running transaction check
---> Package mysql-community-server.x86_64 0:5.5.59-2.el6 will be installed
--> Processing Dependency: mysql-community-common(x86-64) = 5.5.59-2.el6 for package: mysql-community-server-5.5.59-2.el6.x86_64
--> Processing Dependency: mysql-community-client(x86-64) >= 5.5.8 for package: mysql-community-server-5.5.59-2.el6.x86_64
--> Running transaction check
---> Package mysql-community-client.x86_64 0:5.5.59-2.el6 will be installed
--> Processing Dependency: mysql-community-libs(x86-64) >= 5.5.8 for package: mysql-community-client-5.5.59-2.el6.x86_64
---> Package mysql-community-common.x86_64 0:5.5.59-2.el6 will be installed
--> Running transaction check
---> Package mysql-community-libs.x86_64 0:5.5.59-2.el6 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

===================================================================================================================================================================================================================
 Package                                                   Arch                                      Version                                            Repository                                            Size
===================================================================================================================================================================================================================
Installing:
 mysql-community-server                                    x86_64                                    5.5.59-2.el6                                       mysql55-community                                     38 M
Installing for dependencies:
 mysql-community-client                                    x86_64                                    5.5.59-2.el6                                       mysql55-community                                     14 M
 mysql-community-common                                    x86_64                                    5.5.59-2.el6                                       mysql55-community                                    277 k
 mysql-community-libs                                      x86_64                                    5.5.59-2.el6                                       mysql55-community                                    1.7 M

Transaction Summary
===================================================================================================================================================================================================================
Install       4 Package(s)

Total download size: 54 M
Installed size: 239 M
Downloading Packages:
Setting up and reading Presto delta metadata
Processing delta metadata
Package(s) data still to download: 54 M
(1/4): mysql-community-client-5.5.59-2.el6.x86_64.rpm                                                                                                                                       |  14 MB     00:00
(2/4): mysql-community-common-5.5.59-2.el6.x86_64.rpm                                                                                                                                       | 277 kB     00:00
(3/4): mysql-community-libs-5.5.59-2.el6.x86_64.rpm                                                                                                                                         | 1.7 MB     00:00
(4/4): mysql-community-server-5.5.59-2.el6.x86_64.rpm                                                                                                                                       |  38 MB     00:00
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Total                                                                                                                                                                               53 MB/s |  54 MB     00:01
Running rpm_check_debug
Running Transaction Test
Transaction Test Succeeded
Running Transaction
  Installing : mysql-community-common-5.5.59-2.el6.x86_64                                                                                                                                                      1/4
  Installing : mysql-community-libs-5.5.59-2.el6.x86_64                                                                                                                                                        2/4
  Installing : mysql-community-client-5.5.59-2.el6.x86_64                                                                                                                                                      3/4
  Installing : mysql-community-server-5.5.59-2.el6.x86_64                                                                                                                                                      4/4
  Verifying  : mysql-community-libs-5.5.59-2.el6.x86_64                                                                                                                                                        1/4
  Verifying  : mysql-community-common-5.5.59-2.el6.x86_64                                                                                                                                                      2/4
  Verifying  : mysql-community-client-5.5.59-2.el6.x86_64                                                                                                                                                      3/4
  Verifying  : mysql-community-server-5.5.59-2.el6.x86_64                                                                                                                                                      4/4

Installed:
  mysql-community-server.x86_64 0:5.5.59-2.el6

Dependency Installed:
  mysql-community-client.x86_64 0:5.5.59-2.el6                          mysql-community-common.x86_64 0:5.5.59-2.el6                          mysql-community-libs.x86_64 0:5.5.59-2.el6

Complete!
```
