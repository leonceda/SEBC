**What is ubertask optimization?

Whether to enable ubertask optimization, which runs "sufficiently small" jobs sequentially within a single JVM. "Small" is defined by the mapreduce.job.ubertask.maxmaps, mapreduce.job.ubertask.maxreduces, and mapreduce.job.ubertask.maxbytes settings.

**Where in CM is the Kerberos Security Realm value displayed?

In  CM Administrationtab > Settings > Kerberos category > Kerberos Security Realm

**Which CDH service(s) host a property for enabling Kerberos authentication?
 * YARN
 * HDFS
 * Zookeeper

**How do you upgrade the CM agents?

Using Cloudera upgrade wizard

**Give the tsquery statement used to chart Hue's CPU utilization?

select cpu_system_rate + cpu_user_rate where category=ROLE and serviceName=$SERVICENAME
  With SERVICENAME=hue 
 
**Name all the roles that make up the Hive service
 * Hive: HiveServer2
 * Hive: Hive Metastore Service
 * Hive: Gateway
 * Hive: WebHCat Server

**What steps must be completed before integrating Cloudera Manager with Kerberos?
 * Setup a KDC server
 * KDC renewable tickets enabled
 * Java security extention library installed in $JAVA_HOME/jre/lib/security on nodes
