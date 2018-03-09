* Run the Hadoop `pi` program as user `anupam`
  * Use the task parameters `50` and `100`
  * Copy the command and full output to `challenges/labs/5_pi.md`
```
[centos@ip-172-31-25-228 ~]$ klist
Ticket cache: FILE:/tmp/krb5cc_500
Default principal: anupam@LEONCEDA.PA

Valid starting     Expires            Service principal
03/09/18 10:36:08  03/10/18 10:36:08  krbtgt/LEONCEDA.PA@LEONCEDA.PA
        renew until 03/16/18 10:36:08
[centos@ip-172-31-25-228 ~]$
[centos@ip-172-31-25-228 ~]$
[centos@ip-172-31-25-228 ~]$ hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar pi 50 100
Number of Maps  = 50
Samples per Map = 100
Wrote input for Map #0
Wrote input for Map #1
Wrote input for Map #2
Wrote input for Map #3
Wrote input for Map #4
Wrote input for Map #5
Wrote input for Map #6
Wrote input for Map #7
Wrote input for Map #8
Wrote input for Map #9
Wrote input for Map #10
Wrote input for Map #11
Wrote input for Map #12
Wrote input for Map #13
Wrote input for Map #14
Wrote input for Map #15
Wrote input for Map #16
Wrote input for Map #17
Wrote input for Map #18
Wrote input for Map #19
Wrote input for Map #20
Wrote input for Map #21
Wrote input for Map #22
Wrote input for Map #23
Wrote input for Map #24
Wrote input for Map #25
Wrote input for Map #26
Wrote input for Map #27
Wrote input for Map #28
Wrote input for Map #29
Wrote input for Map #30
Wrote input for Map #31
Wrote input for Map #32
Wrote input for Map #33
Wrote input for Map #34
Wrote input for Map #35
Wrote input for Map #36
Wrote input for Map #37
Wrote input for Map #38
Wrote input for Map #39
Wrote input for Map #40
Wrote input for Map #41
Wrote input for Map #42
Wrote input for Map #43
Wrote input for Map #44
Wrote input for Map #45
Wrote input for Map #46
Wrote input for Map #47
Wrote input for Map #48
Wrote input for Map #49
Starting Job
18/03/09 10:53:13 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-25-228.eu-west-1.compute.internal/172.31.25.228:8032
18/03/09 10:53:13 INFO hdfs.DFSClient: Created token for anupam: HDFS_DELEGATION_TOKEN owner=anupam@LEONCEDA.PA, renewer=yarn, realUser=, issueDate=1520592793878, maxDate=1521197593878, sequenceNumber=3, masterKeyId=2 on 172.31.25.228:8020
18/03/09 10:53:13 INFO security.TokenCache: Got dt for hdfs://ip-172-31-25-228.eu-west-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.25.228:8020, Ident: (token for anupam: HDFS_DELEGATION_TOKEN owner=anupam@LEONCEDA.PA, renewer=yarn, realUser=, issueDate=1520592793878, maxDate=1521197593878, sequenceNumber=3, masterKeyId=2)
18/03/09 10:53:14 INFO input.FileInputFormat: Total input paths to process : 50
18/03/09 10:53:14 INFO mapreduce.JobSubmitter: number of splits:50
18/03/09 10:53:14 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1520591660488_0002
18/03/09 10:53:14 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.25.228:8020, Ident: (token for anupam: HDFS_DELEGATION_TOKEN owner=anupam@LEONCEDA.PA, renewer=yarn, realUser=, issueDate=1520592793878, maxDate=1521197593878, sequenceNumber=3, masterKeyId=2)
18/03/09 10:53:14 INFO impl.YarnClientImpl: Submitted application application_1520591660488_0002
18/03/09 10:53:14 INFO mapreduce.Job: The url to track the job: http://ip-172-31-25-228.eu-west-1.compute.internal:8088/proxy/application_1520591660488_0002/
18/03/09 10:53:14 INFO mapreduce.Job: Running job: job_1520591660488_0002
18/03/09 10:53:22 INFO mapreduce.Job: Job job_1520591660488_0002 running in uber mode : false
18/03/09 10:53:22 INFO mapreduce.Job:  map 0% reduce 0%
18/03/09 10:53:28 INFO mapreduce.Job:  map 2% reduce 0%
18/03/09 10:53:29 INFO mapreduce.Job:  map 4% reduce 0%
18/03/09 10:53:32 INFO mapreduce.Job:  map 8% reduce 0%
18/03/09 10:53:33 INFO mapreduce.Job:  map 10% reduce 0%
18/03/09 10:53:34 INFO mapreduce.Job:  map 18% reduce 0%
18/03/09 10:53:37 INFO mapreduce.Job:  map 22% reduce 0%
18/03/09 10:53:38 INFO mapreduce.Job:  map 24% reduce 0%
18/03/09 10:53:39 INFO mapreduce.Job:  map 26% reduce 0%
18/03/09 10:53:40 INFO mapreduce.Job:  map 32% reduce 0%
18/03/09 10:53:42 INFO mapreduce.Job:  map 36% reduce 0%
18/03/09 10:53:44 INFO mapreduce.Job:  map 40% reduce 0%
18/03/09 10:53:46 INFO mapreduce.Job:  map 46% reduce 0%
18/03/09 10:53:47 INFO mapreduce.Job:  map 50% reduce 0%
18/03/09 10:53:48 INFO mapreduce.Job:  map 52% reduce 0%
18/03/09 10:53:49 INFO mapreduce.Job:  map 54% reduce 0%
18/03/09 10:53:51 INFO mapreduce.Job:  map 56% reduce 0%
18/03/09 10:53:52 INFO mapreduce.Job:  map 64% reduce 0%
18/03/09 10:53:54 INFO mapreduce.Job:  map 68% reduce 0%
18/03/09 10:53:57 INFO mapreduce.Job:  map 74% reduce 0%
18/03/09 10:53:58 INFO mapreduce.Job:  map 76% reduce 0%
18/03/09 10:53:59 INFO mapreduce.Job:  map 82% reduce 0%
18/03/09 10:54:02 INFO mapreduce.Job:  map 88% reduce 0%
18/03/09 10:54:03 INFO mapreduce.Job:  map 90% reduce 0%
18/03/09 10:54:04 INFO mapreduce.Job:  map 92% reduce 0%
18/03/09 10:54:05 INFO mapreduce.Job:  map 96% reduce 0%
18/03/09 10:54:06 INFO mapreduce.Job:  map 98% reduce 0%
18/03/09 10:54:07 INFO mapreduce.Job:  map 100% reduce 0%
18/03/09 10:54:09 INFO mapreduce.Job:  map 100% reduce 100%
18/03/09 10:54:09 INFO mapreduce.Job: Job job_1520591660488_0002 completed successfully
18/03/09 10:54:09 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=256
                FILE: Number of bytes written=6602157
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=15040
                HDFS: Number of bytes written=215
                HDFS: Number of read operations=203
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=3
        Job Counters
                Launched map tasks=50
                Launched reduce tasks=1
                Data-local map tasks=50
                Total time spent by all maps in occupied slots (ms)=231291
                Total time spent by all reduces in occupied slots (ms)=4889
                Total time spent by all map tasks (ms)=231291
                Total time spent by all reduce tasks (ms)=4889
                Total vcore-milliseconds taken by all map tasks=231291
                Total vcore-milliseconds taken by all reduce tasks=4889
                Total megabyte-milliseconds taken by all map tasks=236841984
                Total megabyte-milliseconds taken by all reduce tasks=5006336
        Map-Reduce Framework
                Map input records=50
                Map output records=100
                Map output bytes=900
                Map output materialized bytes=1700
                Input split bytes=9140
                Combine input records=0
                Combine output records=0
                Reduce input groups=2
                Reduce shuffle bytes=1700
                Reduce input records=100
                Reduce output records=0
                Spilled Records=200
                Shuffled Maps =50
                Failed Shuffles=0
                Merged Map outputs=50
                GC time elapsed (ms)=5077
                CPU time spent (ms)=34590
                Physical memory (bytes) snapshot=23133503488
                Virtual memory (bytes) snapshot=141353992192
                Total committed heap usage (bytes)=24550309888
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=5900
        File Output Format Counters
                Bytes Written=97
Job Finished in 55.437 seconds
Estimated value of Pi is 3.14160000000000000000

```

