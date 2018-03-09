## <center> Challenge 1: Install a Database server

* Create the Issue `Install MySQL` if you are using RHEL/Centos 6.x
  * Or name it `Install MariaDB` if you are using RHEL/CentOS 7.x
* Assign the Issue to yourself and label it `started`
* Install MySQL 5.5 or MariaDB 5.5 server on the first node listed in `0_setup.md`
  * Use a YUM repository to install the package
  * Copy the repo configuration you used to `challenges/labs/1_my-database-server.repo.md`
* On all cluster nodes
  * Install the database client package and JDBC connector jar on all nodes
* Start the database service and create these databases
  * `scm`
  * `rman`
  * `hive`
  * `oozie`
  * `hue`
* Record the following in `challenges/labs/1_db-server.md`
  * A command and output that shows the hostname of your database server 
```
[centos@ip-172-31-25-228 ~]$ hostname -f
ip-172-31-25-228.eu-west-1.compute.internal
```
  * A command and output that reports the database server version
```
[centos@ip-172-31-25-228 ~]$ mysql -uroot -e "status"
--------------
mysql  Ver 14.14 Distrib 5.5.59, for Linux (x86_64) using readline 5.1

Connection id:          18
Current database:
Current user:           root@localhost
SSL:                    Not in use
Current pager:          stdout
Using outfile:          ''
Using delimiter:        ;
Server version:         5.5.59 MySQL Community Server (GPL)
Protocol version:       10
Connection:             Localhost via UNIX socket
Server characterset:    latin1
Db     characterset:    latin1
Client characterset:    utf8
Conn.  characterset:    utf8
UNIX socket:            /var/lib/mysql/mysql.sock
Uptime:                 2 min 53 sec

Threads: 1  Questions: 74  Slow queries: 0  Opens: 33  Flush tables: 1  Open tables: 26  Queries per second avg: 0.427
--------------
```
  * A command and output that lists all the databases in the server
```
[centos@ip-172-31-25-228 ~]$ mysql -uroot -e "show databases"
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| test               |
+--------------------+
```
* Push this work to GitHub
* Label the Issue `review` and assign it to the instructor
