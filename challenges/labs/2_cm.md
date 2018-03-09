* List the command and output for `ls /etc/yum.repos.d` in `challenges/labs/2_cm.md`
```
$ ls /etc/yum.repos.d

ip-172-31-28-78.eu-west-1.compute.internal |
CentOS-Base.repo
CentOS-Debuginfo.repo
CentOS-fasttrack.repo
CentOS-Media.repo
CentOS-Vault.repo
epel.repo
epel-testing.repo
mysql-community.repo

ip-172-31-25-228.eu-west-1.compute.internal | 
CentOS-Base.repo
CentOS-Debuginfo.repo
CentOS-fasttrack.repo
CentOS-Media.repo
CentOS-Vault.repo
epel.repo
epel-testing.repo
mysql-community.repo

ip-172-31-24-17.eu-west-1.compute.internal | 
CentOS-Base.repo
CentOS-Debuginfo.repo
CentOS-fasttrack.repo
CentOS-Media.repo
CentOS-Vault.repo
epel.repo
epel-testing.repo
mysql-community.repo

ip-172-31-23-131.eu-west-1.compute.internal | 
CentOS-Base.repo
CentOS-Debuginfo.repo
CentOS-fasttrack.repo
CentOS-Media.repo
CentOS-Vault.repo
epel.repo
epel-testing.repo
mysql-community.repo

ip-172-31-24-18.eu-west-1.compute.internal |
CentOS-Base.repo
CentOS-Debuginfo.repo
CentOS-fasttrack.repo
CentOS-Media.repo
CentOS-Vault.repo
epel.repo
epel-testing.repo
mysql-community.repo

```

* Connect Cloudera Manager Server to its database
  * Use the `scm_prepare_database.sh` script to create the `db.properties` file 
    * List the full command and its output in `2_cm.md`
```
[centos@ip-172-31-24-18 ~]$ sudo /usr/share/cmf/schema/scm_prepare_database.sh -h ip-172-31-25-228.eu-west-1.compute.internal mysql scm scm scm
JAVA_HOME=/usr/java/jdk1.8.0_161
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.8.0_161/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
2018-03-09 08:45:51,359 [main] INFO  com.cloudera.enterprise.dbutil.DbCommandExecutor  - Successfully connected to database.
All done, your SCM database is configured correctly!
```
