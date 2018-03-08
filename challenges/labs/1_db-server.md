* Record the following in `challenges/labs/1_db-server.md`
  * The command and output for `hostname -f` on the database server host
```
[centos@ip-172-31-17-134 ~]$ hostname -f
ip-172-31-17-134.eu-west-1.compute.internal
```
  * The command and output for `mysql -u <user> -p<password> -e "status;"`
```
[centos@ip-172-31-17-134 ~]$ mysql -uroot -p -e "status";
Enter password:
--------------
mysql  Ver 14.14 Distrib 5.5.59, for Linux (x86_64) using readline 5.1

Connection id:          24
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
Uptime:                 2 min 49 sec

Threads: 1  Questions: 98  Slow queries: 0  Opens: 33  Flush tables: 1  Open tables: 26  Queries per second avg: 0.579
--------------

```
  * The command and output for `mysql -u <user> -p<password> -e "show databases;"`
```
[centos@ip-172-31-17-134 ~]$ mysql -uroot -p -e "show databases";
Enter password:
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
* Label the Issue `review` and assign it to the instructors

