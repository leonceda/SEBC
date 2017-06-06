# SnapShot lab output

```
[root@ip-172-31-8-154 ~]# sudo -u hdfs hdfs dfs -ls precious
Found 1 items
-rw-r--r--   3 hdfs supergroup     449822 2017-06-06 17:11 precious/SEBC-master.zip
```
```
[root@ip-172-31-8-154 ~]# sudo -u hdfs hdfs dfsadmin -allowSnapshot /user/hdfs/precious
Allowing snaphot on /user/hdfs/precious succeeded
```
```
[root@ip-172-31-8-154 ~]# sudo -u hdfs hdfs dfs -createSnapshot /user/hdfs/precious sebc-hdfs-test
Created snapshot /user/hdfs/precious/.snapshot/sebc-hdfs-test
```
```
[root@ip-172-31-8-154 ~]# sudo -u hdfs hdfs dfs -rm -r -skipTrash precious
rm: The directory /user/hdfs/precious cannot be deleted since /user/hdfs/precious is snapshottable and already has snapshots
```
```
[root@ip-172-31-8-154 ~]# sudo -u hdfs hdfs dfs -rm -r -skipTrash precious/SEBC-master.zip
Deleted precious/SEBC-master.zip
```
```
[root@ip-172-31-8-154 ~]#
[root@ip-172-31-8-154 ~]# sudo -u hdfs hdfs dfs -ls precious/.snapshot/sebc-hdfs-test
Found 1 items
-rw-r--r--   3 hdfs supergroup     449822 2017-06-06 17:11 precious/.snapshot/sebc-hdfs-test/SEBC-master.zip
[root@ip-172-31-8-154 ~]#
[root@ip-172-31-8-154 ~]# sudo -u hdfs hdfs dfs -cp precious/.snapshot/sebc-hdfs-test/SEBC-master.zip precious/
[root@ip-172-31-8-154 ~]# sudo -u hdfs hdfs dfs -ls precious
Found 1 items
-rw-r--r--   3 hdfs supergroup     449822 2017-06-06 17:55 precious/SEBC-master.zip
```
