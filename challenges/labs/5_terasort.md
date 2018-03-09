* Run the `terasort` program as user `hilary` with the output target `/user/hilary/tsort`
  * Generate 24,000,000 records
  * Copy the command and full output to `challenges/labs/5_terasort.md`
```
[centos@ip-172-31-24-18 ~]$ klist
Ticket cache: FILE:/tmp/krb5cc_500
Default principal: hilary@LEONCEDA.PA

Valid starting     Expires            Service principal
03/09/18 10:33:01  03/10/18 10:33:01  krbtgt/LEONCEDA.PA@LEONCEDA.PA
        renew until 03/16/18 10:33:01

[centos@ip-172-31-24-18 ~]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort tgen tsort  24000000
18/03/09 10:44:04 INFO terasort.TeraSort: starting
18/03/09 10:44:05 INFO hdfs.DFSClient: Created token for hilary: HDFS_DELEGATION_TOKEN owner=hilary@LEONCEDA.PA, renewer=yarn, realUser=, issueDate=1520592245741, maxDate=1521197045741, sequenceNumber=2, masterKeyId=2 on 172.31.25.228:8020
18/03/09 10:44:05 INFO security.TokenCache: Got dt for hdfs://ip-172-31-25-228.eu-west-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.25.228:8020, Ident: (token for hilary: HDFS_DELEGATION_TOKEN owner=hilary@LEONCEDA.PA, renewer=yarn, realUser=, issueDate=1520592245741, maxDate=1521197045741, sequenceNumber=2, masterKeyId=2)
18/03/09 10:44:05 INFO input.FileInputFormat: Total input paths to process : 16
Spent 398ms computing base-splits.
Spent 4ms computing TeraScheduler splits.
Computing input splits took 402ms
Sampling 10 splits of 112
Making 6 from 100000 sampled records
Computing parititions took 656ms
Spent 1060ms computing partitions.
18/03/09 10:44:06 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-25-228.eu-west-1.compute.internal/172.31.25.228:8032
18/03/09 10:44:06 INFO mapreduce.JobSubmitter: number of splits:112
18/03/09 10:44:07 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1520591660488_0001
18/03/09 10:44:07 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.25.228:8020, Ident: (token for hilary: HDFS_DELEGATION_TOKEN owner=hilary@LEONCEDA.PA, renewer=yarn, realUser=, issueDate=1520592245741, maxDate=1521197045741, sequenceNumber=2, masterKeyId=2)
18/03/09 10:44:08 INFO impl.YarnClientImpl: Submitted application application_1520591660488_0001
18/03/09 10:44:08 INFO mapreduce.Job: The url to track the job: http://ip-172-31-25-228.eu-west-1.compute.internal:8088/proxy/application_1520591660488_0001/
18/03/09 10:44:08 INFO mapreduce.Job: Running job: job_1520591660488_0001
18/03/09 10:44:17 INFO mapreduce.Job: Job job_1520591660488_0001 running in uber mode : false
18/03/09 10:44:17 INFO mapreduce.Job:  map 0% reduce 0%
18/03/09 10:44:25 INFO mapreduce.Job:  map 2% reduce 0%
18/03/09 10:44:29 INFO mapreduce.Job:  map 3% reduce 0%
18/03/09 10:44:30 INFO mapreduce.Job:  map 4% reduce 0%
18/03/09 10:44:33 INFO mapreduce.Job:  map 6% reduce 0%
18/03/09 10:44:34 INFO mapreduce.Job:  map 8% reduce 0%
18/03/09 10:44:37 INFO mapreduce.Job:  map 10% reduce 0%
18/03/09 10:44:41 INFO mapreduce.Job:  map 11% reduce 0%
18/03/09 10:44:42 INFO mapreduce.Job:  map 12% reduce 0%
18/03/09 10:44:43 INFO mapreduce.Job:  map 13% reduce 0%
18/03/09 10:44:44 INFO mapreduce.Job:  map 14% reduce 0%
18/03/09 10:44:45 INFO mapreduce.Job:  map 16% reduce 0%
18/03/09 10:44:49 INFO mapreduce.Job:  map 18% reduce 0%
18/03/09 10:44:51 INFO mapreduce.Job:  map 19% reduce 0%
18/03/09 10:44:52 INFO mapreduce.Job:  map 20% reduce 0%
18/03/09 10:44:53 INFO mapreduce.Job:  map 22% reduce 0%
18/03/09 10:44:57 INFO mapreduce.Job:  map 24% reduce 0%
18/03/09 10:45:01 INFO mapreduce.Job:  map 27% reduce 0%
18/03/09 10:45:02 INFO mapreduce.Job:  map 29% reduce 0%
18/03/09 10:45:04 INFO mapreduce.Job:  map 30% reduce 0%
18/03/09 10:45:09 INFO mapreduce.Job:  map 32% reduce 0%
18/03/09 10:45:11 INFO mapreduce.Job:  map 34% reduce 0%
18/03/09 10:45:12 INFO mapreduce.Job:  map 37% reduce 0%
18/03/09 10:45:17 INFO mapreduce.Job:  map 38% reduce 0%
18/03/09 10:45:18 INFO mapreduce.Job:  map 39% reduce 0%
18/03/09 10:45:19 INFO mapreduce.Job:  map 40% reduce 0%
18/03/09 10:45:20 INFO mapreduce.Job:  map 42% reduce 0%
18/03/09 10:45:22 INFO mapreduce.Job:  map 43% reduce 0%
18/03/09 10:45:25 INFO mapreduce.Job:  map 45% reduce 0%
18/03/09 10:45:26 INFO mapreduce.Job:  map 46% reduce 0%
18/03/09 10:45:29 INFO mapreduce.Job:  map 47% reduce 0%
18/03/09 10:45:31 INFO mapreduce.Job:  map 49% reduce 0%
18/03/09 10:45:32 INFO mapreduce.Job:  map 50% reduce 0%
18/03/09 10:45:33 INFO mapreduce.Job:  map 52% reduce 0%
18/03/09 10:45:34 INFO mapreduce.Job:  map 53% reduce 0%
18/03/09 10:45:39 INFO mapreduce.Job:  map 55% reduce 0%
18/03/09 10:45:40 INFO mapreduce.Job:  map 57% reduce 0%
18/03/09 10:45:41 INFO mapreduce.Job:  map 58% reduce 0%
18/03/09 10:45:42 INFO mapreduce.Job:  map 59% reduce 0%
18/03/09 10:45:46 INFO mapreduce.Job:  map 60% reduce 0%
18/03/09 10:45:47 INFO mapreduce.Job:  map 61% reduce 0%
18/03/09 10:45:48 INFO mapreduce.Job:  map 63% reduce 0%
18/03/09 10:45:49 INFO mapreduce.Job:  map 65% reduce 0%
18/03/09 10:45:54 INFO mapreduce.Job:  map 67% reduce 0%
18/03/09 10:45:56 INFO mapreduce.Job:  map 69% reduce 0%
18/03/09 10:45:57 INFO mapreduce.Job:  map 70% reduce 0%
18/03/09 10:45:59 INFO mapreduce.Job:  map 71% reduce 0%
18/03/09 10:46:00 INFO mapreduce.Job:  map 72% reduce 0%
18/03/09 10:46:01 INFO mapreduce.Job:  map 73% reduce 0%
18/03/09 10:46:03 INFO mapreduce.Job:  map 75% reduce 0%
18/03/09 10:46:06 INFO mapreduce.Job:  map 76% reduce 0%
18/03/09 10:46:07 INFO mapreduce.Job:  map 77% reduce 0%
18/03/09 10:46:08 INFO mapreduce.Job:  map 79% reduce 0%
18/03/09 10:46:10 INFO mapreduce.Job:  map 80% reduce 0%
18/03/09 10:46:11 INFO mapreduce.Job:  map 81% reduce 0%
18/03/09 10:46:14 INFO mapreduce.Job:  map 82% reduce 0%
18/03/09 10:46:15 INFO mapreduce.Job:  map 84% reduce 0%
18/03/09 10:46:16 INFO mapreduce.Job:  map 85% reduce 0%
18/03/09 10:46:17 INFO mapreduce.Job:  map 86% reduce 0%
18/03/09 10:46:18 INFO mapreduce.Job:  map 88% reduce 0%
18/03/09 10:46:22 INFO mapreduce.Job:  map 89% reduce 0%
18/03/09 10:46:25 INFO mapreduce.Job:  map 90% reduce 0%
18/03/09 10:46:26 INFO mapreduce.Job:  map 91% reduce 0%
18/03/09 10:46:30 INFO mapreduce.Job:  map 92% reduce 0%
18/03/09 10:46:31 INFO mapreduce.Job:  map 93% reduce 10%
18/03/09 10:46:32 INFO mapreduce.Job:  map 94% reduce 10%
18/03/09 10:46:34 INFO mapreduce.Job:  map 94% reduce 15%
18/03/09 10:46:35 INFO mapreduce.Job:  map 95% reduce 15%
18/03/09 10:46:36 INFO mapreduce.Job:  map 96% reduce 21%
18/03/09 10:46:39 INFO mapreduce.Job:  map 97% reduce 21%
18/03/09 10:46:41 INFO mapreduce.Job:  map 98% reduce 21%
18/03/09 10:46:42 INFO mapreduce.Job:  map 99% reduce 21%
18/03/09 10:46:43 INFO mapreduce.Job:  map 100% reduce 22%
18/03/09 10:46:46 INFO mapreduce.Job:  map 100% reduce 28%
18/03/09 10:46:48 INFO mapreduce.Job:  map 100% reduce 34%
18/03/09 10:46:49 INFO mapreduce.Job:  map 100% reduce 48%
18/03/09 10:46:52 INFO mapreduce.Job:  map 100% reduce 50%
18/03/09 10:46:54 INFO mapreduce.Job:  map 100% reduce 52%
18/03/09 10:46:56 INFO mapreduce.Job:  map 100% reduce 57%
18/03/09 10:46:59 INFO mapreduce.Job:  map 100% reduce 82%
18/03/09 10:47:00 INFO mapreduce.Job:  map 100% reduce 86%
18/03/09 10:47:01 INFO mapreduce.Job:  map 100% reduce 89%
18/03/09 10:47:05 INFO mapreduce.Job:  map 100% reduce 94%
18/03/09 10:47:10 INFO mapreduce.Job:  map 100% reduce 97%
18/03/09 10:47:11 INFO mapreduce.Job:  map 100% reduce 100%
18/03/09 10:47:12 INFO mapreduce.Job: Job job_1520591660488_0001 completed successfully
18/03/09 10:47:12 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=2932412439
                FILE: Number of bytes written=5820798375
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=6553616800
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=354
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=12
        Job Counters
                Launched map tasks=112
                Launched reduce tasks=6
                Data-local map tasks=112
                Total time spent by all maps in occupied slots (ms)=791110
                Total time spent by all reduces in occupied slots (ms)=221201
                Total time spent by all map tasks (ms)=791110
                Total time spent by all reduce tasks (ms)=221201
                Total vcore-milliseconds taken by all map tasks=791110
                Total vcore-milliseconds taken by all reduce tasks=221201
                Total megabyte-milliseconds taken by all map tasks=810096640
                Total megabyte-milliseconds taken by all reduce tasks=226509824
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Map output bytes=6684672000
                Map output materialized bytes=2873023768
                Input split bytes=16800
                Combine input records=0
                Combine output records=0
                Reduce input groups=65536000
                Reduce shuffle bytes=2873023768
                Reduce input records=65536000
                Reduce output records=65536000
                Spilled Records=131072000
                Shuffled Maps =672
                Failed Shuffles=0
                Merged Map outputs=672
                GC time elapsed (ms)=17521
                CPU time spent (ms)=693710
                Physical memory (bytes) snapshot=60378931200
                Virtual memory (bytes) snapshot=327385305088
                Total committed heap usage (bytes)=62811799552
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=6553600000
        File Output Format Counters
                Bytes Written=6553600000
18/03/09 10:47:12 INFO terasort.TeraSort: done

real    3m8.851s
user    0m10.013s
sys     0m0.469s

```
* Run the Hadoop `pi` program as user `anupam`
  * Use the task parameters `50` and `100` 
  * Copy the command and full output to `challenges/labs/5_pi.md`
```

```
*  Copy the configuration files in `/var/kerberos/krb5kdc/` to your repo:
    * Add the prefix `5_` and the suffix `.md` to the original file name
    * Example: `5_kdc.conf.md`
* Push this work to GitHub and label the Issue `review`
* Assign the issue to the instructor

