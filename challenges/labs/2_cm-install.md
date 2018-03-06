## <center> Challenge 2: Install Cloudera Manager 5.11.x (latest update)

* Create the Issue `Install CM`
* Assign yourself and label it `started`
* Install Cloudera Manager on the second node you listed in `0_setup.md`
* Copy the YUM command and output for installing Cloudera Manager in `challenges/labs/2_cm-install.md`
```
[centos@ip-172-31-30-59 ~]$ sudo yum -y install cloudera-manager-server cloudera-manager-server-db-2
Loaded plugins: fastestmirror, presto
Setting up Install Process
Loading mirror speeds from cached hostfile
 * base: ftp.heanet.ie
 * epel: ftp.heanet.ie
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
Resolving Dependencies
--> Running transaction check
---> Package cloudera-manager-server.x86_64 0:5.11.2-1.cm5112.p0.6.el6 will be installed
--> Processing Dependency: cloudera-manager-daemons = 5.11.2 for package: cloudera-manager-server-5.11.2-1.cm5112.p0.6.el6.x86_64
---> Package cloudera-manager-server-db-2.x86_64 0:5.11.2-1.cm5112.p0.6.el6 will be installed
--> Processing Dependency: postgresql-server >= 8.4 for package: cloudera-manager-server-db-2-5.11.2-1.cm5112.p0.6.el6.x86_64
--> Running transaction check
---> Package cloudera-manager-daemons.x86_64 0:5.11.2-1.cm5112.p0.6.el6 will be installed
---> Package postgresql-server.x86_64 0:8.4.20-8.el6_9 will be installed
--> Processing Dependency: postgresql(x86-64) = 8.4.20-8.el6_9 for package: postgresql-server-8.4.20-8.el6_9.x86_64
--> Running transaction check
---> Package postgresql.x86_64 0:8.4.20-8.el6_9 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

===============================================================================================================
 Package                            Arch         Version                          Repository              Size
===============================================================================================================
Installing:
 cloudera-manager-server            x86_64       5.11.2-1.cm5112.p0.6.el6         cloudera-manager       8.5 k
 cloudera-manager-server-db-2       x86_64       5.11.2-1.cm5112.p0.6.el6         cloudera-manager        10 k
Installing for dependencies:
 cloudera-manager-daemons           x86_64       5.11.2-1.cm5112.p0.6.el6         cloudera-manager       671 M
 postgresql                         x86_64       8.4.20-8.el6_9                   updates                2.6 M
 postgresql-server                  x86_64       8.4.20-8.el6_9                   updates                3.4 M

Transaction Summary
===============================================================================================================
Install       5 Package(s)

Total download size: 677 M
Installed size: 855 M
Downloading Packages:
Setting up and reading Presto delta metadata
Processing delta metadata
Package(s) data still to download: 677 M
(1/5): cloudera-manager-daemons-5.11.2-1.cm5112.p0.6.el6.x86_64.rpm                     | 671 MB     00:14
(2/5): cloudera-manager-server-5.11.2-1.cm5112.p0.6.el6.x86_64.rpm                      | 8.5 kB     00:00
(3/5): cloudera-manager-server-db-2-5.11.2-1.cm5112.p0.6.el6.x86_64.rpm                 |  10 kB     00:00
(4/5): postgresql-8.4.20-8.el6_9.x86_64.rpm                                             | 2.6 MB     00:00
(5/5): postgresql-server-8.4.20-8.el6_9.x86_64.rpm                                      | 3.4 MB     00:00
---------------------------------------------------------------------------------------------------------------
Total                                                                           30 MB/s | 677 MB     00:22
Running rpm_check_debug
Running Transaction Test
Transaction Test Succeeded
Running Transaction
  Installing : cloudera-manager-daemons-5.11.2-1.cm5112.p0.6.el6.x86_64                                    1/5
  Installing : cloudera-manager-server-5.11.2-1.cm5112.p0.6.el6.x86_64                                     2/5
  Installing : postgresql-8.4.20-8.el6_9.x86_64                                                            3/5
  Installing : postgresql-server-8.4.20-8.el6_9.x86_64                                                     4/5
  Installing : cloudera-manager-server-db-2-5.11.2-1.cm5112.p0.6.el6.x86_64                                5/5
  Verifying  : cloudera-manager-server-5.11.2-1.cm5112.p0.6.el6.x86_64                                     1/5
  Verifying  : postgresql-server-8.4.20-8.el6_9.x86_64                                                     2/5
  Verifying  : postgresql-8.4.20-8.el6_9.x86_64                                                            3/5
  Verifying  : cloudera-manager-daemons-5.11.2-1.cm5112.p0.6.el6.x86_64                                    4/5
  Verifying  : cloudera-manager-server-db-2-5.11.2-1.cm5112.p0.6.el6.x86_64                                5/5

Installed:
  cloudera-manager-server.x86_64 0:5.11.2-1.cm5112.p0.6.el6
  cloudera-manager-server-db-2.x86_64 0:5.11.2-1.cm5112.p0.6.el6

Dependency Installed:
  cloudera-manager-daemons.x86_64 0:5.11.2-1.cm5112.p0.6.el6         postgresql.x86_64 0:8.4.20-8.el6_9
  postgresql-server.x86_64 0:8.4.20-8.el6_9

Complete!

```
* Connect Cloudera Manager Server to its database
  * Use the `scm_prepare_database.sh` script 
  * Copy the full command invocation and its output to `2_properties.md`
  * Copy your `db.properties` content into the same file
* Start the Cloudera Manager server
* Put the following in `challenges/labs/2_cm_startup.md`:
  * The first line of your CM server log
  * Any line in the log containing the string "Started Jetty server"
* Copy the API command and output to list your CM deployment into `challenges/labs/2_cm-deployment.md`
* Push these changes to GitHub and label the Issue `review`
* Assign the issue to the instructors
