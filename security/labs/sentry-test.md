```
[root@ip-172-31-6-121 ~]# kinit leonceda
Password for leonceda@LEONCEDA.SG:
```

```
[root@ip-172-31-6-121 ~]# beeline
Beeline version 1.1.0-cdh5.8.3 by Apache Hive
beeline> !connect jdbc:hive2://ip-172-31-6-121.eu-west-1.compute.internal:10000/default;principal=hive/ip-172-31-6-121.eu-west-1.compute.internal@LEONCEDA.SG
scan complete in 18ms
Connecting to jdbc:hive2://ip-172-31-6-121.eu-west-1.compute.internal:10000/default;principal=hive/ip-172-31-6-121.eu-west-1.compute.internal@LEONCEDA.SG
Enter username for jdbc:hive2://ip-172-31-6-121.eu-west-1.compute.internal:10000/default;principal=hive/ip-172-31-6-121.eu-west-1.compute.internal@LEONCEDA.SG: leonceda
Enter password for jdbc:hive2://ip-172-31-6-121.eu-west-1.compute.internal:10000/default;principal=hive/ip-172-31-6-121.eu-west-1.compute.internal@LEONCEDA.SG: ********
Connected to: Apache Hive (version 1.1.0-cdh5.8.3)
Driver: Hive JDBC (version 1.1.0-cdh5.8.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ

```

```
0: jdbc:hive2://ip-172-31-6-121.eu-west-1.com> show tables;
INFO  : Compiling command(queryId=hive_20170608222424_3cc055c7-f015-4249-bf9c-ed4da25e7e51): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170608222424_3cc055c7-f015-4249-bf9c-ed4da25e7e51); Time taken: 0.321 seconds
INFO  : Executing command(queryId=hive_20170608222424_3cc055c7-f015-4249-bf9c-ed4da25e7e51): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170608222424_3cc055c7-f015-4249-bf9c-ed4da25e7e51); Time taken: 0.822 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (1.501 seconds)

```

```
0: jdbc:hive2://ip-172-31-6-121.eu-west-1.com> CREATE ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20170608222525_38df79db-25f7-410c-b481-4ccbfea056b5): CREATE ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170608222525_38df79db-25f7-410c-b481-4ccbfea056b5); Time taken: 0.383 seconds
INFO  : Executing command(queryId=hive_20170608222525_38df79db-25f7-410c-b481-4ccbfea056b5): CREATE ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170608222525_38df79db-25f7-410c-b481-4ccbfea056b5); Time taken: 0.159 seconds
INFO  : OK
No rows affected (0.575 seconds)
0: jdbc:hive2://ip-172-31-6-121.eu-west-1.com> GRANT ALL ON SERVER server1 TO ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20170608222525_e729980a-ad2f-4f2d-9ddb-2bc69be79ce7): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170608222525_e729980a-ad2f-4f2d-9ddb-2bc69be79ce7); Time taken: 0.374 seconds
INFO  : Executing command(queryId=hive_20170608222525_e729980a-ad2f-4f2d-9ddb-2bc69be79ce7): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170608222525_e729980a-ad2f-4f2d-9ddb-2bc69be79ce7); Time taken: 0.286 seconds
INFO  : OK
No rows affected (0.724 seconds)
0: jdbc:hive2://ip-172-31-6-121.eu-west-1.com> GRANT ROLE sentry_admin TO GROUP leonceda;
INFO  : Compiling command(queryId=hive_20170608222525_6bea0a22-4849-4439-8220-380c4f02e404): GRANT ROLE sentry_admin TO GROUP leonceda
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170608222525_6bea0a22-4849-4439-8220-380c4f02e404); Time taken: 0.316 seconds
INFO  : Executing command(queryId=hive_20170608222525_6bea0a22-4849-4439-8220-380c4f02e404): GRANT ROLE sentry_admin TO GROUP leonceda
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170608222525_6bea0a22-4849-4439-8220-380c4f02e404); Time taken: 0.227 seconds
INFO  : OK
No rows affected (0.602 seconds)
0: jdbc:hive2://ip-172-31-6-121.eu-west-1.com> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20170608222525_c5424177-27fa-492a-a7e6-f30f599445a6): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170608222525_c5424177-27fa-492a-a7e6-f30f599445a6); Time taken: 0.346 seconds
INFO  : Executing command(queryId=hive_20170608222525_c5424177-27fa-492a-a7e6-f30f599445a6): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170608222525_c5424177-27fa-492a-a7e6-f30f599445a6); Time taken: 0.673 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (1.438 seconds)

```

```
0: jdbc:hive2://ip-172-31-6-121.eu-west-1.com> CREATE ROLE reads;
INFO  : Compiling command(queryId=hive_20170608222626_7a69798e-a257-40b0-800a-10d1278302be): CREATE ROLE reads
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170608222626_7a69798e-a257-40b0-800a-10d1278302be); Time taken: 0.385 seconds
INFO  : Executing command(queryId=hive_20170608222626_7a69798e-a257-40b0-800a-10d1278302be): CREATE ROLE reads
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170608222626_7a69798e-a257-40b0-800a-10d1278302be); Time taken: 0.062 seconds
INFO  : OK
No rows affected (0.506 seconds)
0: jdbc:hive2://ip-172-31-6-121.eu-west-1.com> CREATE ROLE write;
INFO  : Compiling command(queryId=hive_20170608222626_4479f7ce-f2c7-4ce9-ba3e-0ac10f3a65f6): CREATE ROLE write
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170608222626_4479f7ce-f2c7-4ce9-ba3e-0ac10f3a65f6); Time taken: 0.219 seconds
INFO  : Executing command(queryId=hive_20170608222626_4479f7ce-f2c7-4ce9-ba3e-0ac10f3a65f6): CREATE ROLE write
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170608222626_4479f7ce-f2c7-4ce9-ba3e-0ac10f3a65f6); Time taken: 0.049 seconds
INFO  : OK
No rows affected (0.301 seconds)
0: jdbc:hive2://ip-172-31-6-121.eu-west-1.com> GRANT SELECT ON DATABASE default TO ROLE reads;
INFO  : Compiling command(queryId=hive_20170608222626_4b869b50-28eb-4687-86ab-ca2879978f72): GRANT SELECT ON DATABASE default TO ROLE reads
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170608222626_4b869b50-28eb-4687-86ab-ca2879978f72); Time taken: 0.271 seconds
INFO  : Executing command(queryId=hive_20170608222626_4b869b50-28eb-4687-86ab-ca2879978f72): GRANT SELECT ON DATABASE default TO ROLE reads
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170608222626_4b869b50-28eb-4687-86ab-ca2879978f72); Time taken: 0.1 seconds
INFO  : OK
No rows affected (0.41 seconds)
0: jdbc:hive2://ip-172-31-6-121.eu-west-1.com> GRANT ROLE reads TO GROUP selector;
INFO  : Compiling command(queryId=hive_20170608222727_9865a275-2d75-450a-b7a7-d62c50a75ed5): GRANT ROLE reads TO GROUP selector
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170608222727_9865a275-2d75-450a-b7a7-d62c50a75ed5); Time taken: 0.545 seconds
INFO  : Executing command(queryId=hive_20170608222727_9865a275-2d75-450a-b7a7-d62c50a75ed5): GRANT ROLE reads TO GROUP selector
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170608222727_9865a275-2d75-450a-b7a7-d62c50a75ed5); Time taken: 0.068 seconds
INFO  : OK
No rows affected (0.644 seconds)

```

```
0: jdbc:hive2://ip-172-31-6-121.eu-west-1.com> REVOKE ALL ON DATABASE default FROM ROLE writes;
INFO  : Compiling command(queryId=hive_20170608223131_08331260-5e95-402a-baf7-d550ec8183e1): REVOKE ALL ON DATABASE default FROM ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170608223131_08331260-5e95-402a-baf7-d550ec8183e1); Time taken: 0.201 seconds
INFO  : Executing command(queryId=hive_20170608223131_08331260-5e95-402a-baf7-d550ec8183e1): REVOKE ALL ON DATABASE default FROM ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170608223131_08331260-5e95-402a-baf7-d550ec8183e1); Time taken: 0.094 seconds
INFO  : OK
No rows affected (0.342 seconds)
0: jdbc:hive2://ip-172-31-6-121.eu-west-1.com> GRANT SELECT ON default.sample_07 TO ROLE writes;
INFO  : Compiling command(queryId=hive_20170608223232_9be1de6a-75e9-4639-a22d-8f518749e129): GRANT SELECT ON default.sample_07 TO ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170608223232_9be1de6a-75e9-4639-a22d-8f518749e129); Time taken: 0.216 seconds
INFO  : Executing command(queryId=hive_20170608223232_9be1de6a-75e9-4639-a22d-8f518749e129): GRANT SELECT ON default.sample_07 TO ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170608223232_9be1de6a-75e9-4639-a22d-8f518749e129); Time taken: 0.12 seconds
INFO  : OK
No rows affected (0.37 seconds)
0: jdbc:hive2://ip-172-31-6-121.eu-west-1.com> GRANT ROLE writes TO GROUP inserters;
INFO  : Compiling command(queryId=hive_20170608223232_66ebc45f-f5bc-4fbf-918b-2bb63ed3cb65): GRANT ROLE writes TO GROUP inserters
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170608223232_66ebc45f-f5bc-4fbf-918b-2bb63ed3cb65); Time taken: 0.241 seconds
INFO  : Executing command(queryId=hive_20170608223232_66ebc45f-f5bc-4fbf-918b-2bb63ed3cb65): GRANT ROLE writes TO GROUP inserters
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170608223232_66ebc45f-f5bc-4fbf-918b-2bb63ed3cb65); Time taken: 0.06 seconds
INFO  : OK
No rows affected (0.343 seconds)

```

```
[root@ip-172-31-6-121 ~]# kinit george
Password for george@LEONCEDA.SG:
[root@ip-172-31-6-121 ~]# beeline
Beeline version 1.1.0-cdh5.8.3 by Apache Hive
beeline> !connect jdbc:hive2://ip-172-31-6-121.eu-west-1.compute.internal:10000/default;principal=hive/ip-172-31-6-121.eu-west-1.compute.internal@LEONCEDA.SG
scan complete in 14ms
Connecting to jdbc:hive2://ip-172-31-6-121.eu-west-1.compute.internal:10000/default;principal=hive/ip-172-31-6-121.eu-west-1.compute.internal@LEONCEDA.SG
Enter username for jdbc:hive2://ip-172-31-6-121.eu-west-1.compute.internal:10000/default;principal=hive/ip-172-31-6-121.eu-west-1.compute.internal@LEONCEDA.SG: george
Enter password for jdbc:hive2://ip-172-31-6-121.eu-west-1.compute.internal:10000/default;principal=hive/ip-172-31-6-121.eu-west-1.compute.internal@LEONCEDA.SG: ******
Connected to: Apache Hive (version 1.1.0-cdh5.8.3)
Driver: Hive JDBC (version 1.1.0-cdh5.8.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-172-31-6-121.eu-west-1.com> show tables;
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (1.297 seconds)
INFO  : Compiling command(queryId=hive_20170608223535_b2da0700-ee82-4724-8538-16e4f0b6f820): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170608223535_b2da0700-ee82-4724-8538-16e4f0b6f820); Time taken: 0.288 seconds
INFO  : Executing command(queryId=hive_20170608223535_b2da0700-ee82-4724-8538-16e4f0b6f820): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170608223535_b2da0700-ee82-4724-8538-16e4f0b6f820); Time taken: 0.61 seconds
INFO  : OK

```

```
[root@ip-172-31-6-121 ~]#
[root@ip-172-31-6-121 ~]# kinit ferdinand
Password for ferdinand@LEONCEDA.SG:
[root@ip-172-31-6-121 ~]# beeline
Beeline version 1.1.0-cdh5.8.3 by Apache Hive
beeline> !connect jdbc:hive2://ip-172-31-6-121.eu-west-1.compute.internal:10000/default;principal=hive/ip-172-31-6-121.eu-west-1.compute.internal@LEONCEDA.SG
scan complete in 11ms
Connecting to jdbc:hive2://ip-172-31-6-121.eu-west-1.compute.internal:10000/default;principal=hive/ip-172-31-6-121.eu-west-1.compute.internal@LEONCEDA.SG
Enter username for jdbc:hive2://ip-172-31-6-121.eu-west-1.compute.internal:10000/default;principal=hive/ip-172-31-6-121.eu-west-1.compute.internal@LEONCEDA.SG: leonceda
Enter password for jdbc:hive2://ip-172-31-6-121.eu-west-1.compute.internal:10000/default;principal=hive/ip-172-31-6-121.eu-west-1.compute.internal@LEONCEDA.SG: ********
Connected to: Apache Hive (version 1.1.0-cdh5.8.3)
Driver: Hive JDBC (version 1.1.0-cdh5.8.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-172-31-6-121.eu-west-1.com> show tables;
INFO  : Compiling command(queryId=hive_20170608223737_44ac94f5-b4e2-4d14-ac10-cab7d84c0dee): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170608223737_44ac94f5-b4e2-4d14-ac10-cab7d84c0dee); Time taken: 0.376 seconds
INFO  : Executing command(queryId=hive_20170608223737_44ac94f5-b4e2-4d14-ac10-cab7d84c0dee): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170608223737_44ac94f5-b4e2-4d14-ac10-cab7d84c0dee); Time taken: 1.163 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (2.003 seconds)
0: jdbc:hive2://ip-172-31-6-121.eu-west-1.com>

```
