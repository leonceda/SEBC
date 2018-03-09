## <center> Challenge 3 - Install CDH 5.11.x

* Create the Issue `Install CDH`
* Assign yourself and label it `started`
* Deploy Coreset services + Impala
  * Rename your cluster after your GitHub handle
* Create user directories in HDFS for `hilary` and `anupam`
* Add the following to `3_cm.md`:
    * The command and output for `hdfs dfs -ls /user`
```
[centos@ip-172-31-25-228 ~]$ sudo -u hdfs hdfs dfs -ls /user
Found 7 items
drwxr-xr-x   - anupam anupam          0 2018-03-09 09:21 /user/anupam
drwxr-xr-x   - hilary hilary          0 2018-03-09 09:20 /user/hilary
drwxrwxrwx   - mapred hadoop          0 2018-03-09 09:15 /user/history
drwxrwxr-t   - hive   hive            0 2018-03-09 09:16 /user/hive
drwxrwxr-x   - hue    hue             0 2018-03-09 09:17 /user/hue
drwxrwxr-x   - impala impala          0 2018-03-09 09:17 /user/impala
drwxrwxr-x   - oozie  oozie           0 2018-03-09 09:17 /user/oozie
```
    * The command and output from the CM API call `../api/v14/hosts` 
```
[centos@ip-172-31-24-18 ~]$ curl -v -u 'admin:*******' http://ip-172-31-24-18.eu-west-1.compute.internal:7180/api/v14/hosts
* About to connect() to ip-172-31-24-18.eu-west-1.compute.internal port 7180 (#0)
*   Trying 172.31.24.18... connected
* Connected to ip-172-31-24-18.eu-west-1.compute.internal (172.31.24.18) port 7180 (#0)
* Server auth using Basic with user 'admin'
> GET /api/v14/hosts HTTP/1.1
> Authorization: Basic YWRtaW46YWRtaW4=
> User-Agent: curl/7.19.7 (x86_64-redhat-linux-gnu) libcurl/7.19.7 NSS/3.27.1 zlib/1.2.3 libidn/1.18 libssh2/1.4.2
> Host: ip-172-31-24-18.eu-west-1.compute.internal:7180
> Accept: */*
>
< HTTP/1.1 200 OK
< Expires: Thu, 01-Jan-1970 00:00:00 GMT
< Set-Cookie: CLOUDERA_MANAGER_SESSIONID=uq3ycw52y59mkmq3wu6x1yb;Path=/;HttpOnly
< Content-Type: application/json
< Date: Fri, 09 Mar 2018 09:24:21 GMT
< Transfer-Encoding: chunked
< Server: Jetty(6.1.26.cloudera.4)
<
{
  "items" : [ {
    "hostId" : "55575243-9eb2-4108-aecf-b6662342fce1",
    "ipAddress" : "172.31.23.131",
    "hostname" : "ip-172-31-23-131.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-24-18.eu-west-1.compute.internal:7180/cmf/hostRedirect/55575243-9eb2-4108-aecf-b6662342fce1",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 16722612224
  }, {
    "hostId" : "c00895c8-7245-4dc2-8851-ffe5e285e433",
    "ipAddress" : "172.31.24.17",
    "hostname" : "ip-172-31-24-17.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-24-18.eu-west-1.compute.internal:7180/cmf/hostRedirect/c00895c8-7245-4dc2-8851-ffe5e285e433",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 16722612224
  }, {
    "hostId" : "6446d46f-8438-4959-8bda-ce10c8f72082",
    "ipAddress" : "172.31.24.18",
    "hostname" : "ip-172-31-24-18.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-24-18.eu-west-1.compute.internal:7180/cmf/hostRedirect/6446d46f-8438-4959-8bda-ce10c8f72082",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 16722612224
  }, {
    "hostId" : "514c9dca-5395-4af8-8ea7-2740c391d29e",
    "ipAddress" : "172.31.25.228",
    "hostname" : "ip-172-31-25-228.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-24-18.eu-west-1.compute.internal:7180/cmf/hostRedirect/514c9dca-5395-4af8-8ea7-2740c391d29e",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 16722612224
  }, {
    "hostId" : "6fb4f23b-feaf-43be-a813-45ecc9a2a259",
    "ipAddress" : "172.31.28.78",
    "hostname" : "ip-172-31-28-78.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-24-18.eu-west-1.compute.internal:7180/cmf/hostRedirect/6fb4f23b-feaf-43be-a813-45ecc9a2a259",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 16722313216
  } ]
* Connection #0 to host ip-172-31-24-18.eu-west-1.compute.internal left intact
* Closing connection #0
}
```
    * The command and output from the CM API call `../api/v8/clusters/<githubName>/services`
```
[centos@ip-172-31-24-18 ~]$ curl -v -u 'admin:*******' http://ip-172-31-24-18.eu-west-1.compute.internal:7180/api/v8/clusters/leonceda/services
* About to connect() to ip-172-31-24-18.eu-west-1.compute.internal port 7180 (#0)
*   Trying 172.31.24.18... connected
* Connected to ip-172-31-24-18.eu-west-1.compute.internal (172.31.24.18) port 7180 (#0)
* Server auth using Basic with user 'admin'
> GET /api/v8/clusters/leonceda/services HTTP/1.1
> Authorization: Basic YWRtaW46YWRtaW4=
> User-Agent: curl/7.19.7 (x86_64-redhat-linux-gnu) libcurl/7.19.7 NSS/3.27.1 zlib/1.2.3 libidn/1.18 libssh2/1.4.2
> Host: ip-172-31-24-18.eu-west-1.compute.internal:7180
> Accept: */*
>
< HTTP/1.1 200 OK
< Expires: Thu, 01-Jan-1970 00:00:00 GMT
< Set-Cookie: CLOUDERA_MANAGER_SESSIONID=ul60sf8hlb6x2dztcyna10qd;Path=/;HttpOnly
< Content-Type: application/json
< Date: Fri, 09 Mar 2018 09:26:09 GMT
< Transfer-Encoding: chunked
< Server: Jetty(6.1.26.cloudera.4)
<
{
  "items" : [ {
    "name" : "zookeeper",
    "type" : "ZOOKEEPER",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-24-18.eu-west-1.compute.internal:7180/cmf/serviceRedirect/zookeeper",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "ZOOKEEPER_CANARY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "ZOOKEEPER_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "ZooKeeper"
  }, {
    "name" : "oozie",
    "type" : "OOZIE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-24-18.eu-west-1.compute.internal:7180/cmf/serviceRedirect/oozie",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "OOZIE_OOZIE_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Oozie"
  }, {
    "name" : "hue",
    "type" : "HUE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-24-18.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hue",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HUE_HUE_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hue"
  }, {
    "name" : "hdfs",
    "type" : "HDFS",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-24-18.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hdfs",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HDFS_BLOCKS_WITH_CORRUPT_REPLICAS",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_CANARY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_DATA_NODES_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_FREE_SPACE_REMAINING",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_HA_NAMENODE_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_MISSING_BLOCKS",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_UNDER_REPLICATED_BLOCKS",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "HDFS"
  }, {
    "name" : "impala",
    "type" : "IMPALA",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-24-18.eu-west-1.compute.internal:7180/cmf/serviceRedirect/impala",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "IMPALA_ASSIGNMENT_LOCALITY",
      "summary" : "DISABLED"
    }, {
      "name" : "IMPALA_CATALOGSERVER_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "IMPALA_IMPALADS_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "IMPALA_STATESTORE_HEALTH",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Impala"
  }, {
    "name" : "yarn",
    "type" : "YARN",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-24-18.eu-west-1.compute.internal:7180/cmf/serviceRedirect/yarn",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "YARN_JOBHISTORY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_NODE_MANAGERS_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_RESOURCEMANAGERS_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_USAGE_AGGREGATION_HEALTH",
      "summary" : "DISABLED"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "YARN (MR2 Included)"
  }, {
    "name" : "hive",
    "type" : "HIVE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-24-18.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hive",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HIVE_HIVEMETASTORES_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "HIVE_HIVESERVER2S_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hive"
  } ]
* Connection #0 to host ip-172-31-24-18.eu-west-1.compute.internal left intact
* Closing connection #0
}
```
* Login to Hue and install the Hive sample data 
    * Copy a Hue screen that shows the Hive tables to `challenges/labs/3_hue_hive.png`
* Push this work to GitHub and label the Issue `review`
* Assign the issue to the instructor

