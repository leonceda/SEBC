hallenge 4 - HDFS Testing

* Create the Issue `Test HDFS`
* Assign yourself and label it `started`
* As user `hilary`, use `teragen` to generate a 65,536,000-record dataset
  * Write the output to 16 files 
  * Set the block size to 64 MB
  * Set the mapper container size to 768 MiB
  * Name the target directory `tgen`
  * Use the `time` command to capture job duration
* Put the following in `challenges/labs/4_teragen.md`
  * The full `teragen` command and output 
```
[root@ip-172-31-24-18 ~]# su - hilary
[hilary@ip-172-31-24-18 ~]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples-2.6.0-cdh5.11.2.jar teragen -Ddfs.blocksize=64m -Dmapreduce.job.maps=16 -Dmapreduce.map.memory.mb=748 65536000 tgen
18/03/09 10:11:50 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-25-228.eu-west-1.compute.internal/172.31.25.228:8032
18/03/09 10:11:51 INFO terasort.TeraGen: Generating 65536000 using 16
18/03/09 10:11:51 INFO mapreduce.JobSubmitter: number of splits:16
18/03/09 10:11:51 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1520586953143_0001
18/03/09 10:11:52 INFO impl.YarnClientImpl: Submitted application application_1520586953143_0001
18/03/09 10:11:52 INFO mapreduce.Job: The url to track the job: http://ip-172-31-25-228.eu-west-1.compute.internal:8088/proxy/application_1520586953143_0001/
18/03/09 10:11:52 INFO mapreduce.Job: Running job: job_1520586953143_0001
18/03/09 10:11:59 INFO mapreduce.Job: Job job_1520586953143_0001 running in uber mode : false
18/03/09 10:11:59 INFO mapreduce.Job:  map 0% reduce 0%
18/03/09 10:12:08 INFO mapreduce.Job:  map 6% reduce 0%
18/03/09 10:12:20 INFO mapreduce.Job:  map 29% reduce 0%
18/03/09 10:12:24 INFO mapreduce.Job:  map 33% reduce 0%
18/03/09 10:12:25 INFO mapreduce.Job:  map 34% reduce 0%
18/03/09 10:12:26 INFO mapreduce.Job:  map 42% reduce 0%
18/03/09 10:12:29 INFO mapreduce.Job:  map 43% reduce 0%
18/03/09 10:12:30 INFO mapreduce.Job:  map 46% reduce 0%
18/03/09 10:12:31 INFO mapreduce.Job:  map 50% reduce 0%
18/03/09 10:12:41 INFO mapreduce.Job:  map 56% reduce 0%
18/03/09 10:12:46 INFO mapreduce.Job:  map 61% reduce 0%
18/03/09 10:12:47 INFO mapreduce.Job:  map 66% reduce 0%
18/03/09 10:12:48 INFO mapreduce.Job:  map 69% reduce 0%
18/03/09 10:12:49 INFO mapreduce.Job:  map 76% reduce 0%
18/03/09 10:12:50 INFO mapreduce.Job:  map 80% reduce 0%
18/03/09 10:12:51 INFO mapreduce.Job:  map 81% reduce 0%
18/03/09 10:12:52 INFO mapreduce.Job:  map 83% reduce 0%
18/03/09 10:12:54 INFO mapreduce.Job:  map 84% reduce 0%
18/03/09 10:12:55 INFO mapreduce.Job:  map 94% reduce 0%
18/03/09 10:12:56 INFO mapreduce.Job:  map 96% reduce 0%
18/03/09 10:12:57 INFO mapreduce.Job:  map 98% reduce 0%
18/03/09 10:12:58 INFO mapreduce.Job:  map 100% reduce 0%
18/03/09 10:12:58 INFO mapreduce.Job: Job job_1520586953143_0001 completed successfully
18/03/09 10:12:59 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=2047494
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=1368
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=64
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=32
        Job Counters
                Launched map tasks=16
                Other local map tasks=16
                Total time spent by all maps in occupied slots (ms)=370970
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=370970
                Total vcore-milliseconds taken by all map tasks=370970
                Total megabyte-milliseconds taken by all map tasks=379873280
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Input split bytes=1368
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=2579
                CPU time spent (ms)=152110
                Physical memory (bytes) snapshot=5197750272
                Virtual memory (bytes) snapshot=40697237504
                Total committed heap usage (bytes)=4813488128
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=140750829423462787
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=6553600000

real    1m11.114s
user    0m7.788s
sys     0m0.458s

```
  * The result of the `time` command
```
real    1m11.114s
user    0m7.788s
sys     0m0.458s

```

  * The command and output of `hdfs dfs -ls /user/hilary/tgen`
```
[centos@ip-172-31-25-228 ~]$ sudo -u hdfs hdfs dfs -ls /user/hilary/tgen
Found 17 items
-rw-r--r--   3 hilary hilary          0 2018-03-09 10:12 /user/hilary/tgen/_SUCCESS
-rw-r--r--   3 hilary hilary  409600000 2018-03-09 10:12 /user/hilary/tgen/part-m-00000
-rw-r--r--   3 hilary hilary  409600000 2018-03-09 10:12 /user/hilary/tgen/part-m-00001
-rw-r--r--   3 hilary hilary  409600000 2018-03-09 10:12 /user/hilary/tgen/part-m-00002
-rw-r--r--   3 hilary hilary  409600000 2018-03-09 10:12 /user/hilary/tgen/part-m-00003
-rw-r--r--   3 hilary hilary  409600000 2018-03-09 10:12 /user/hilary/tgen/part-m-00004
-rw-r--r--   3 hilary hilary  409600000 2018-03-09 10:12 /user/hilary/tgen/part-m-00005
-rw-r--r--   3 hilary hilary  409600000 2018-03-09 10:12 /user/hilary/tgen/part-m-00006
-rw-r--r--   3 hilary hilary  409600000 2018-03-09 10:12 /user/hilary/tgen/part-m-00007
-rw-r--r--   3 hilary hilary  409600000 2018-03-09 10:12 /user/hilary/tgen/part-m-00008
-rw-r--r--   3 hilary hilary  409600000 2018-03-09 10:12 /user/hilary/tgen/part-m-00009
-rw-r--r--   3 hilary hilary  409600000 2018-03-09 10:12 /user/hilary/tgen/part-m-00010
-rw-r--r--   3 hilary hilary  409600000 2018-03-09 10:12 /user/hilary/tgen/part-m-00011
-rw-r--r--   3 hilary hilary  409600000 2018-03-09 10:12 /user/hilary/tgen/part-m-00012
-rw-r--r--   3 hilary hilary  409600000 2018-03-09 10:12 /user/hilary/tgen/part-m-00013
-rw-r--r--   3 hilary hilary  409600000 2018-03-09 10:12 /user/hilary/tgen/part-m-00014
-rw-r--r--   3 hilary hilary  409600000 2018-03-09 10:12 /user/hilary/tgen/part-m-00015
```

  * The command and output of `hadoop fsck -blocks /user/hilary`
```
[centos@ip-172-31-25-228 ~]$ sudo -u hdfs hdfs fsck -blocks /user/hilary
Connecting to namenode via http://ip-172-31-25-228.eu-west-1.compute.internal:50070
FSCK started by hdfs (auth:SIMPLE) from /172.31.25.228 for path /user/hilary at Fri Mar 09 10:16:41 UTC 2018
.................Status: HEALTHY
 Total size:    6553600000 B
 Total dirs:    3
 Total files:   17
 Total symlinks:                0
 Total blocks (validated):      112 (avg. block size 58514285 B)
 Minimally replicated blocks:   112 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Fri Mar 09 10:16:41 UTC 2018 in 5 milliseconds


The filesystem under path '/user/hilary' is HEALTHY

```

* Push this work to GitHub and label the Issue `review`
* Assign the issue to the instructors
