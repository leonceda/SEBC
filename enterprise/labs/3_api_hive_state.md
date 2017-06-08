*Managing Hive services using CM API

```
[root@ip-172-31-5-113 ~]#  curl -k -u 'leonceda:cloudera' http://172.31.5.113:7180/api/version
v13[root@ip-172-31-5-113 ~]#
```

```
[root@ip-172-31-5-113 ~]# curl -k -u 'leonceda:cloudera' http://172.31.5.113:7180/api/v13/clusters/cluster/services/hive/
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-5-113.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://ip-172-31-5-113.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hive/instances",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  } ],
  "configStalenessStatus" : "FRESH",
  "clientConfigStalenessStatus" : "FRESH",
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive",
  "entityStatus" : "GOOD_HEALTH"
}[root@ip-172-31-5-113 ~]#
```
