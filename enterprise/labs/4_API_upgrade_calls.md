*Upgrade CM to latest version of C5.9

 * Report the latest available version of the API
```
[root@ip-172-31-8-154 ~]# curl -k -u 'leonceda:cloudera' http://172.31.5.113:7180/api/version
v14[root@ip-172-31-8-154 ~]#
```

 * Report the CM version
```
[root@ip-172-31-8-154 ~]# curl  -k -u 'leonceda:cloudera' http://172.31.5.113:7180/api/v14/cm/version
{
  "version" : "5.9.2",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170330-1814",
  "gitHash" : "822da28bff818f57fc1bfc3eafe3a550300ef1b0",
  "snapshot" : false
}
```

 * List all CM users
```
[root@ip-172-31-8-154 ~]# curl  -k -u 'leonceda:cloudera' http://172.31.5.113:7180/api/v14/users
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ]
  }, {
    "name" : "bdruser",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "leonceda",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_NAVIGATOR_ADMIN" ]
  } ]
}[root@ip-172-31-8-154 ~]#
```
 * 
```
[root@ip-172-31-8-154 ~]# curl  -k -u 'leonceda:cloudera' http://172.31.5.113:7180/api/v14/cm/scmDbInfo
{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}[root@ip-172-31-8-154 ~]#

``` 
