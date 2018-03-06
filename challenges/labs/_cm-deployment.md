* Copy the API command and output to list your CM deployment into `challenges/labs/2_cm-deployment.md`
```
[centos@ip-172-31-30-59 ~]$ curl -v -u 'admin:admin' http://ip-172-31-30-59.eu-west-1.compute.internal:7180/api/v16/cm/deployment
* About to connect() to ip-172-31-30-59.eu-west-1.compute.internal port 7180 (#0)
*   Trying 172.31.30.59... connected
* Connected to ip-172-31-30-59.eu-west-1.compute.internal (172.31.30.59) port 7180 (#0)
* Server auth using Basic with user 'admin'
> GET /api/v16/cm/deployment HTTP/1.1
> Authorization: Basic YWRtaW46YWRtaW4=
> User-Agent: curl/7.19.7 (x86_64-redhat-linux-gnu) libcurl/7.19.7 NSS/3.27.1 zlib/1.2.3 libidn/1.18 libssh2/1.4.2
> Host: ip-172-31-30-59.eu-west-1.compute.internal:7180
> Accept: */*
>
< HTTP/1.1 200 OK
< Expires: Thu, 01-Jan-1970 00:00:00 GMT
< Set-Cookie: CLOUDERA_MANAGER_SESSIONID=7nqr2kekt2lq3l8tvdi8jk48;Path=/;HttpOnly
< Content-Type: application/json
< Date: Tue, 06 Mar 2018 22:47:38 GMT
< Transfer-Encoding: chunked
< Server: Jetty(6.1.26.cloudera.4)
<
{
  "timestamp" : "2018-03-06T22:47:38.759Z",
  "clusters" : [ ],
  "hosts" : [ ],
  "users" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "fd88fa94530c6014a351151f7ef4bbb77cdff623bc1a89c3d624c9a3e6984c4d",
    "pwSalt" : -8906817278156687271,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.11.2",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170811-0014",
    "gitHash" : "3c3ea33a12076fb83a8f11c4452c52fac685d01b",
    "snapshot" : false
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/23/2012 2:30",
      "sensitive" : false
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD",
      "sensitive" : false
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,http://archive.cloudera.com/kudu/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/",
      "sensitive" : false
    } ]
  },
  "allHostsConfig" : {
    "items" : [ ]
  },
  "peers" : [ ],
  "hostTemplates" : {
    "items" : [ ]
  }
* Connection #0 to host ip-172-31-30-59.eu-west-1.compute.internal left intact
* Closing connection #0
```
* Push these changes to GitHub and label the Issue `review`
* Assign the issue to the instructors
