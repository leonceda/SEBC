tart the Cloudera Manager server
* Put the following in `challenges/labs/2_cm_startup.md`:

  * The first line of your CM server log
```
[centos@ip-172-31-30-59 ~]$ sudo head -1 /var/log/cloudera-scm-server/cloudera-scm-server.log
2018-03-06 22:40:59,279 INFO main:com.cloudera.server.cmf.Main: Starting SCM Server. JVM Args: [-Dlog4j.configuration=file:/etc/cloudera-scm-server/log4j.properties, -Dfile.encoding=UTF-8, -Dcmf.root.logger=INFO,LOGFILE, -Dcmf.log.dir=/var/log/cloudera-scm-server, -Dcmf.log.file=cloudera-scm-server.log, -Dcmf.jetty.threshhold=WARN, -Dcmf.schema.dir=/usr/share/cmf/schema, -Djava.awt.headless=true, -Djava.net.preferIPv4Stack=true, -Dpython.home=/usr/share/cmf/python, -XX:+UseConcMarkSweepGC, -XX:+UseParNewGC, -XX:+HeapDumpOnOutOfMemoryError, -Xmx2G, -XX:MaxPermSize=256m, -XX:+HeapDumpOnOutOfMemoryError, -XX:HeapDumpPath=/tmp, -XX:OnOutOfMemoryError=kill -9 %p], Args: [], Version: 5.11.2 (#6 built by jenkins on 20170811-0014 git: 3c3ea33a12076fb83a8f11c4452c52fac685d01b)

```
  * Any line in the log containing the string "Started Jetty server"
```
[centos@ip-172-31-30-59 ~]$ sudo grep -i "Started Jetty server" /var/log/cloudera-scm-server/cloudera-scm-server.log
2018-03-06 22:42:12,762 INFO WebServerImpl:com.cloudera.server.cmf.WebServerImpl: Started Jetty server.
```
