
  * Repolist
[root@ip-172-31-10-254 ~]# ll /etc/yum.repos.d/
total 28
-rw-r--r--. 1 root root 1926 Nov 27  2013 CentOS-Base.repo
-rw-r--r--. 1 root root  638 Nov 27  2013 CentOS-Debuginfo.repo
-rw-r--r--. 1 root root  630 Nov 27  2013 CentOS-Media.repo
-rw-r--r--. 1 root root 3664 Nov 27  2013 CentOS-Vault.repo
-rw-r--r--. 1 root root  208 Jun  9 09:04 cloudera-manager.repo
-rw-r--r--. 1 root root 1836 Jun  9 08:35 mysql-community.repo
-rw-r--r--. 1 root root 1885 Apr 27 09:04 mysql-community-source.repo

  * Databases setup

```
[root@ip-172-31-6-211 ~]# /usr/share/cmf/schema/scm_prepare_database.s                                                                                                     h mysql -h ip-172-31-10-254.eu-west-1.compute.internal -uroot -p --scm                                                                                                     -host ip-172-31-6-211.eu-west-1.compute.internal hive hive hive
Enter database password:
JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/jav                                                                                                     a/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/                                                                                                     usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommand                                                                                                     Executor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
2017-06-09 09:25:23,574 [main] INFO  com.cloudera.enterprise.dbutil.Db                                                                                                     CommandExecutor  - Successfully connected to database.
All done, your SCM database is configured correctly!
[root@ip-172-31-6-211 ~]#
[root@ip-172-31-6-211 ~]# /usr/share/cmf/schema/scm_prepare_database.s                                                                                                     h mysql -h ip-172-31-10-254.eu-west-1.compute.internal -uroot -p --scm                                                                                                     -host ip-172-31-6-211.eu-west-1.compute.internal rman rman rman
Enter database password:
JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/jav                                                                                                     a/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/                                                                                                     usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommand                                                                                                     Executor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
2017-06-09 09:25:39,965 [main] INFO  com.cloudera.enterprise.dbutil.Db                                                                                                     CommandExecutor  - Successfully connected to database.
All done, your SCM database is configured correctly!
[root@ip-172-31-6-211 ~]#
[root@ip-172-31-6-211 ~]#
[root@ip-172-31-6-211 ~]# /usr/share/cmf/schema/scm_prepare_database.sh mysql -h ip-172-31-10-254.eu-west-1.compute.internal -uroot -p --scm-host                           ip-172-31-6-211.eu-west-1.compute.internal oozie oozie oozie
Enter database password:
JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/s                          hare/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
2017-06-09 09:26:26,856 [main] INFO  com.cloudera.enterprise.dbutil.DbCommandExecutor  - Successfully connected to database.
All done, your SCM database is configured correctly!
[root@ip-172-31-6-211 ~]#
[root@ip-172-31-6-211 ~]#
[root@ip-172-31-6-211 ~]# /usr/share/cmf/schema/scm_prepare_database.sh mysql -h ip-172-31-10-254.eu-west-1.compute.internal -uroot -p --scm-host ip-172-31-6-211.eu-west-1.compute.internal hue hue hue
Enter database password:
JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
2017-06-09 09:27:28,127 [main] INFO  com.cloudera.enterprise.dbutil.DbCommandExecutor  - Successfully connected to database.
All done, your SCM database is configured correctly!
[root@ip-172-31-6-211 ~]#
[root@ip-172-31-6-211 ~]#
[root@ip-172-31-6-211 ~]#
[root@ip-172-31-6-211 ~]# /usr/share/cmf/schema/scm_prepare_database.sh mysql -h ip-172-31-10-254.eu-west-1.compute.internal -uroot -p --scm-host ip-172-31-6-211.eu-west-1.compute.internal sentry sentry sentry
Enter database password:
JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
2017-06-09 09:27:41,840 [main] INFO  com.cloudera.enterprise.dbutil.DbCommandExecutor  - Successfully connected to database.
All done, your SCM database is configured correctly!

```

