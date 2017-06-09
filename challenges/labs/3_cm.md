  * Command and output for hdfs dfs -ls /user
```
[root@ip-172-31-3-164 ~]# sudo -u hdfs hdfs dfs -ls /user
Found 6 items
drwxr-xr-x   - hdfs   supergroup          0 2017-06-09 10:35 /user/fullerton
drwxrwxrwx   - mapred hadoop              0 2017-06-09 10:24 /user/history
drwxrwxr-t   - hive   hive                0 2017-06-09 10:25 /user/hive
drwxrwxr-x   - hue    hue                 0 2017-06-09 10:26 /user/hue
drwxrwxr-x   - oozie  oozie               0 2017-06-09 10:26 /user/oozie
drwxr-xr-x   - hdfs   supergroup          0 2017-06-09 10:35 /user/raffles

```

 * The output from the CM API call ../api/v14/hosts
```
[root@ip-172-31-6-211 ~]# curl -u 'admin:admin' http://ip-172-31-6-211:7180/api/v14/hosts
{
  "items" : [ {
    "hostId" : "1e0dcbb2-b3ac-4b54-9868-6212635d4a06",
    "ipAddress" : "172.31.10.254",
    "hostname" : "ip-172-31-10-254.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-6-211.eu-west-1.compute.internal:7180/cmf/hostRedirect/1e0dcbb2-b3ac-4b54-9868-6212635d4a06",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "e0381a88-fac6-4bf5-afdb-642ee121cf7c",
    "ipAddress" : "172.31.12.37",
    "hostname" : "ip-172-31-12-37.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-6-211.eu-west-1.compute.internal:7180/cmf/hostRedirect/e0381a88-fac6-4bf5-afdb-642ee121cf7c",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "c43fda1f-7fb1-42d3-83da-bcf57db95f28",
    "ipAddress" : "172.31.3.164",
    "hostname" : "ip-172-31-3-164.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-6-211.eu-west-1.compute.internal:7180/cmf/hostRedirect/c43fda1f-7fb1-42d3-83da-bcf57db95f28",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "4d29662c-1c95-4e72-a41a-0b1d70443856",
    "ipAddress" : "172.31.5.142",
    "hostname" : "ip-172-31-5-142.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-6-211.eu-west-1.compute.internal:7180/cmf/hostRedirect/4d29662c-1c95-4e72-a41a-0b1d70443856",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "9485637d-2c92-49da-a90d-1b2d0ce6ac55",
    "ipAddress" : "172.31.6.211",
    "hostname" : "ip-172-31-6-211.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-6-211.eu-west-1.compute.internal:7180/cmf/hostRedirect/9485637d-2c92-49da-a90d-1b2d0ce6ac55",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  } ]

```
