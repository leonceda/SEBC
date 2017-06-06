** Teragen output **

```
[root@ip-172-31-8-154 ~]# time sudo -u hdfs hadoop jar /opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/jars/hadoop-examples.jar teragen -Dmapred.map.tasks=4 -Ddfs.block.size=33554432 100000000 /user/hdfs/teragen-perf
17/06/06 15:18:06 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-6-121.eu-west-1.compute.internal/172.31.6.121:8032
17/06/06 15:18:07 INFO terasort.TeraSort: Generating 100000000 using 4
17/06/06 15:18:07 INFO mapreduce.JobSubmitter: number of splits:4
17/06/06 15:18:07 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/06/06 15:18:07 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/06/06 15:18:08 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1496756043472_0006
17/06/06 15:18:08 INFO impl.YarnClientImpl: Submitted application application_1496756043472_0006
17/06/06 15:18:08 INFO mapreduce.Job: The url to track the job: http://ip-172-31-6-121.eu-west-1.compute.internal:8088/proxy/application_1496756043472_0006/
17/06/06 15:18:08 INFO mapreduce.Job: Running job: job_1496756043472_0006
17/06/06 15:18:14 INFO mapreduce.Job: Job job_1496756043472_0006 running in uber mode : false
17/06/06 15:18:14 INFO mapreduce.Job:  map 0% reduce 0%
17/06/06 15:18:27 INFO mapreduce.Job:  map 2% reduce 0%
17/06/06 15:18:30 INFO mapreduce.Job:  map 3% reduce 0%
17/06/06 15:18:33 INFO mapreduce.Job:  map 4% reduce 0%
17/06/06 15:18:40 INFO mapreduce.Job:  map 5% reduce 0%
17/06/06 15:18:42 INFO mapreduce.Job:  map 6% reduce 0%
17/06/06 15:18:46 INFO mapreduce.Job:  map 7% reduce 0%
17/06/06 15:18:48 INFO mapreduce.Job:  map 8% reduce 0%
17/06/06 15:18:51 INFO mapreduce.Job:  map 9% reduce 0%
17/06/06 15:18:56 INFO mapreduce.Job:  map 10% reduce 0%
17/06/06 15:19:00 INFO mapreduce.Job:  map 11% reduce 0%
17/06/06 15:19:05 INFO mapreduce.Job:  map 12% reduce 0%
17/06/06 15:19:10 INFO mapreduce.Job:  map 13% reduce 0%
17/06/06 15:19:12 INFO mapreduce.Job:  map 14% reduce 0%
17/06/06 15:19:14 INFO mapreduce.Job:  map 15% reduce 0%
17/06/06 15:19:18 INFO mapreduce.Job:  map 16% reduce 0%
17/06/06 15:19:22 INFO mapreduce.Job:  map 17% reduce 0%
17/06/06 15:19:26 INFO mapreduce.Job:  map 18% reduce 0%
17/06/06 15:19:29 INFO mapreduce.Job:  map 19% reduce 0%
17/06/06 15:19:33 INFO mapreduce.Job:  map 20% reduce 0%
17/06/06 15:19:35 INFO mapreduce.Job:  map 21% reduce 0%
17/06/06 15:19:38 INFO mapreduce.Job:  map 22% reduce 0%
17/06/06 15:19:43 INFO mapreduce.Job:  map 23% reduce 0%
17/06/06 15:19:50 INFO mapreduce.Job:  map 24% reduce 0%
17/06/06 15:19:53 INFO mapreduce.Job:  map 25% reduce 0%
17/06/06 15:19:58 INFO mapreduce.Job:  map 26% reduce 0%
17/06/06 15:19:59 INFO mapreduce.Job:  map 27% reduce 0%
17/06/06 15:20:02 INFO mapreduce.Job:  map 28% reduce 0%
17/06/06 15:20:08 INFO mapreduce.Job:  map 29% reduce 0%
17/06/06 15:20:11 INFO mapreduce.Job:  map 30% reduce 0%
17/06/06 15:20:13 INFO mapreduce.Job:  map 31% reduce 0%
17/06/06 15:20:18 INFO mapreduce.Job:  map 32% reduce 0%
17/06/06 15:20:20 INFO mapreduce.Job:  map 33% reduce 0%
17/06/06 15:20:25 INFO mapreduce.Job:  map 34% reduce 0%
17/06/06 15:20:28 INFO mapreduce.Job:  map 35% reduce 0%
17/06/06 15:20:32 INFO mapreduce.Job:  map 36% reduce 0%
17/06/06 15:20:35 INFO mapreduce.Job:  map 37% reduce 0%
17/06/06 15:20:39 INFO mapreduce.Job:  map 38% reduce 0%
17/06/06 15:20:44 INFO mapreduce.Job:  map 39% reduce 0%
17/06/06 15:20:50 INFO mapreduce.Job:  map 40% reduce 0%
17/06/06 15:20:53 INFO mapreduce.Job:  map 41% reduce 0%
17/06/06 15:20:56 INFO mapreduce.Job:  map 42% reduce 0%
17/06/06 15:21:01 INFO mapreduce.Job:  map 43% reduce 0%
17/06/06 15:21:05 INFO mapreduce.Job:  map 44% reduce 0%
17/06/06 15:21:09 INFO mapreduce.Job:  map 45% reduce 0%
17/06/06 15:21:14 INFO mapreduce.Job:  map 46% reduce 0%
17/06/06 15:21:20 INFO mapreduce.Job:  map 47% reduce 0%
17/06/06 15:21:31 INFO mapreduce.Job:  map 48% reduce 0%
17/06/06 15:21:41 INFO mapreduce.Job:  map 50% reduce 0%
17/06/06 15:21:48 INFO mapreduce.Job:  map 51% reduce 0%
17/06/06 15:21:54 INFO mapreduce.Job:  map 52% reduce 0%
17/06/06 15:22:02 INFO mapreduce.Job:  map 53% reduce 0%
17/06/06 15:22:10 INFO mapreduce.Job:  map 54% reduce 0%
17/06/06 15:22:18 INFO mapreduce.Job:  map 55% reduce 0%
17/06/06 15:22:26 INFO mapreduce.Job:  map 56% reduce 0%
17/06/06 15:22:34 INFO mapreduce.Job:  map 57% reduce 0%
17/06/06 15:22:40 INFO mapreduce.Job:  map 58% reduce 0%
17/06/06 15:22:42 INFO mapreduce.Job:  map 59% reduce 0%
17/06/06 15:22:49 INFO mapreduce.Job:  map 60% reduce 0%
17/06/06 15:22:57 INFO mapreduce.Job:  map 61% reduce 0%
17/06/06 15:23:05 INFO mapreduce.Job:  map 62% reduce 0%

17/06/06 15:23:14 INFO mapreduce.Job:  map 63% reduce 0%
17/06/06 15:23:21 INFO mapreduce.Job:  map 64% reduce 0%
17/06/06 15:23:29 INFO mapreduce.Job:  map 65% reduce 0%
17/06/06 15:23:36 INFO mapreduce.Job:  map 66% reduce 0%
17/06/06 15:23:41 INFO mapreduce.Job:  map 67% reduce 0%
17/06/06 15:23:48 INFO mapreduce.Job:  map 68% reduce 0%
17/06/06 15:23:56 INFO mapreduce.Job:  map 69% reduce 0%
17/06/06 15:24:00 INFO mapreduce.Job:  map 70% reduce 0%
17/06/06 15:24:12 INFO mapreduce.Job:  map 71% reduce 0%
17/06/06 15:24:23 INFO mapreduce.Job:  map 72% reduce 0%
17/06/06 15:24:33 INFO mapreduce.Job:  map 73% reduce 0%
17/06/06 15:24:39 INFO mapreduce.Job:  map 74% reduce 0%
17/06/06 15:24:46 INFO mapreduce.Job:  map 75% reduce 0%
17/06/06 15:24:53 INFO mapreduce.Job:  map 76% reduce 0%
17/06/06 15:25:02 INFO mapreduce.Job:  map 77% reduce 0%
17/06/06 15:25:11 INFO mapreduce.Job:  map 78% reduce 0%
17/06/06 15:25:13 INFO mapreduce.Job:  map 79% reduce 0%
17/06/06 15:25:23 INFO mapreduce.Job:  map 80% reduce 0%
17/06/06 15:25:32 INFO mapreduce.Job:  map 81% reduce 0%
17/06/06 15:25:36 INFO mapreduce.Job:  map 82% reduce 0%
17/06/06 15:25:44 INFO mapreduce.Job:  map 83% reduce 0%
17/06/06 15:25:50 INFO mapreduce.Job:  map 84% reduce 0%
17/06/06 15:26:00 INFO mapreduce.Job:  map 85% reduce 0%
17/06/06 15:26:10 INFO mapreduce.Job:  map 86% reduce 0%
17/06/06 15:26:17 INFO mapreduce.Job:  map 87% reduce 0%
17/06/06 15:26:22 INFO mapreduce.Job:  map 88% reduce 0%
17/06/06 15:26:26 INFO mapreduce.Job:  map 89% reduce 0%
17/06/06 15:26:30 INFO mapreduce.Job:  map 90% reduce 0%
17/06/06 15:26:36 INFO mapreduce.Job:  map 91% reduce 0%
17/06/06 15:26:40 INFO mapreduce.Job:  map 92% reduce 0%
17/06/06 15:26:50 INFO mapreduce.Job:  map 93% reduce 0%
17/06/06 15:26:57 INFO mapreduce.Job:  map 94% reduce 0%
17/06/06 15:27:14 INFO mapreduce.Job:  map 95% reduce 0%
17/06/06 15:27:26 INFO mapreduce.Job:  map 96% reduce 0%
17/06/06 15:27:47 INFO mapreduce.Job:  map 97% reduce 0%
17/06/06 15:28:02 INFO mapreduce.Job:  map 98% reduce 0%
17/06/06 15:28:11 INFO mapreduce.Job:  map 99% reduce 0%
17/06/06 15:28:39 INFO mapreduce.Job:  map 100% reduce 0%
17/06/06 15:28:53 INFO mapreduce.Job: Job job_1496756043472_0006 completed successfully
17/06/06 15:28:53 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=488464
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=344
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=1849914
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=1849914
                Total vcore-seconds taken by all map tasks=1849914
                Total megabyte-seconds taken by all map tasks=1894311936
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Input split bytes=344
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=2650
                CPU time spent (ms)=206130
                Physical memory (bytes) snapshot=741326848
                Virtual memory (bytes) snapshot=6250749952
                Total committed heap usage (bytes)=849346560
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=214760662691937609
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=10000000000

real    10m50.108s
user    0m8.438s
sys     0m1.127s
```


** TeraSort output **

```
[root@ip-172-31-8-154 ~]# time sudo -u hdfs hadoop jar /opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/jars/hadoop-examples.jar terasort /user/hdfs/teragen-perf /user/hdfs/terasort-perf                          17/06/06 16:20:05 INFO terasort.TeraSort: starting
17/06/06 16:20:07 INFO input.FileInputFormat: Total input paths to process : 4
Spent 373ms computing base-splits.
Spent 6ms computing TeraScheduler splits.
Computing input splits took 380ms
Sampling 10 splits of 300
Making 8 from 100000 sampled records
Computing parititions took 1229ms
Spent 1612ms computing partitions.
17/06/06 16:20:08 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-6-121.eu-west-1.compute.internal/172.31.6.121:8032
17/06/06 16:20:09 INFO mapreduce.JobSubmitter: number of splits:300
17/06/06 16:20:10 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1496756043472_0007
17/06/06 16:20:10 INFO impl.YarnClientImpl: Submitted application application_1496756043472_0007
17/06/06 16:20:10 INFO mapreduce.Job: The url to track the job: http://ip-172-31-6-121.eu-west-1.compute.internal:8088/proxy/application_1496756043472_0007/
17/06/06 16:20:10 INFO mapreduce.Job: Running job: job_1496756043472_0007
17/06/06 16:20:17 INFO mapreduce.Job: Job job_1496756043472_0007 running in uber mode : false
17/06/06 16:20:17 INFO mapreduce.Job:  map 0% reduce 0%
17/06/06 16:20:26 INFO mapreduce.Job:  map 1% reduce 0%
17/06/06 16:20:31 INFO mapreduce.Job:  map 2% reduce 0%
17/06/06 16:20:35 INFO mapreduce.Job:  map 3% reduce 0%
17/06/06 16:20:37 INFO mapreduce.Job:  map 4% reduce 0%
17/06/06 16:20:44 INFO mapreduce.Job:  map 6% reduce 0%
17/06/06 16:20:52 INFO mapreduce.Job:  map 7% reduce 0%
17/06/06 16:20:56 INFO mapreduce.Job:  map 8% reduce 0%
17/06/06 16:20:57 INFO mapreduce.Job:  map 9% reduce 0%
17/06/06 16:21:05 INFO mapreduce.Job:  map 10% reduce 0%
17/06/06 16:21:08 INFO mapreduce.Job:  map 11% reduce 0%
17/06/06 16:21:09 INFO mapreduce.Job:  map 12% reduce 0%
17/06/06 16:21:16 INFO mapreduce.Job:  map 13% reduce 0%
17/06/06 16:21:20 INFO mapreduce.Job:  map 14% reduce 0%
17/06/06 16:21:23 INFO mapreduce.Job:  map 15% reduce 0%
17/06/06 16:21:28 INFO mapreduce.Job:  map 16% reduce 0%
17/06/06 16:21:32 INFO mapreduce.Job:  map 17% reduce 0%
17/06/06 16:21:33 INFO mapreduce.Job:  map 18% reduce 0%
17/06/06 16:21:41 INFO mapreduce.Job:  map 19% reduce 0%
17/06/06 16:21:44 INFO mapreduce.Job:  map 20% reduce 0%
17/06/06 16:21:48 INFO mapreduce.Job:  map 21% reduce 0%
17/06/06 16:21:50 INFO mapreduce.Job:  map 22% reduce 0%
17/06/06 16:21:56 INFO mapreduce.Job:  map 23% reduce 0%
17/06/06 16:21:57 INFO mapreduce.Job:  map 24% reduce 0%
17/06/06 16:22:04 INFO mapreduce.Job:  map 25% reduce 0%
17/06/06 16:22:08 INFO mapreduce.Job:  map 26% reduce 0%
17/06/06 16:22:12 INFO mapreduce.Job:  map 27% reduce 0%
17/06/06 16:22:17 INFO mapreduce.Job:  map 28% reduce 0%
17/06/06 16:22:20 INFO mapreduce.Job:  map 29% reduce 0%
17/06/06 16:22:21 INFO mapreduce.Job:  map 30% reduce 0%
17/06/06 16:22:28 INFO mapreduce.Job:  map 31% reduce 0%
17/06/06 16:22:32 INFO mapreduce.Job:  map 32% reduce 0%
17/06/06 16:22:35 INFO mapreduce.Job:  map 33% reduce 0%
17/06/06 16:22:43 INFO mapreduce.Job:  map 34% reduce 0%
17/06/06 16:22:44 INFO mapreduce.Job:  map 35% reduce 0%
17/06/06 16:22:45 INFO mapreduce.Job:  map 36% reduce 0%
17/06/06 16:22:53 INFO mapreduce.Job:  map 37% reduce 0%
17/06/06 16:22:55 INFO mapreduce.Job:  map 38% reduce 0%
17/06/06 16:23:00 INFO mapreduce.Job:  map 39% reduce 0%
17/06/06 16:23:05 INFO mapreduce.Job:  map 40% reduce 0%
17/06/06 16:23:09 INFO mapreduce.Job:  map 41% reduce 0%
17/06/06 16:23:12 INFO mapreduce.Job:  map 42% reduce 0%
17/06/06 16:23:18 INFO mapreduce.Job:  map 43% reduce 0%
17/06/06 16:23:20 INFO mapreduce.Job:  map 44% reduce 0%
17/06/06 16:23:26 INFO mapreduce.Job:  map 45% reduce 0%
17/06/06 16:23:30 INFO mapreduce.Job:  map 46% reduce 0%
17/06/06 16:23:32 INFO mapreduce.Job:  map 47% reduce 0%
17/06/06 16:23:37 INFO mapreduce.Job:  map 48% reduce 0%
17/06/06 16:23:41 INFO mapreduce.Job:  map 49% reduce 0%
17/06/06 16:23:42 INFO mapreduce.Job:  map 50% reduce 0%
17/06/06 16:23:50 INFO mapreduce.Job:  map 51% reduce 0%
17/06/06 16:23:51 INFO mapreduce.Job:  map 52% reduce 0%
17/06/06 16:23:57 INFO mapreduce.Job:  map 53% reduce 0%
17/06/06 16:23:58 INFO mapreduce.Job:  map 54% reduce 0%
17/06/06 16:24:06 INFO mapreduce.Job:  map 55% reduce 0%
17/06/06 16:24:07 INFO mapreduce.Job:  map 56% reduce 0%
17/06/06 16:24:14 INFO mapreduce.Job:  map 57% reduce 0%
17/06/06 16:24:15 INFO mapreduce.Job:  map 58% reduce 0%
17/06/06 16:24:21 INFO mapreduce.Job:  map 59% reduce 0%
17/06/06 16:24:24 INFO mapreduce.Job:  map 60% reduce 0%
17/06/06 16:24:28 INFO mapreduce.Job:  map 61% reduce 0%
17/06/06 16:24:31 INFO mapreduce.Job:  map 62% reduce 0%
17/06/06 16:24:36 INFO mapreduce.Job:  map 63% reduce 0%
17/06/06 16:24:39 INFO mapreduce.Job:  map 64% reduce 0%
17/06/06 16:24:43 INFO mapreduce.Job:  map 65% reduce 0%
17/06/06 16:24:47 INFO mapreduce.Job:  map 66% reduce 0%
17/06/06 16:24:51 INFO mapreduce.Job:  map 67% reduce 0%
17/06/06 16:24:55 INFO mapreduce.Job:  map 68% reduce 0%
17/06/06 16:24:58 INFO mapreduce.Job:  map 69% reduce 0%
17/06/06 16:25:02 INFO mapreduce.Job:  map 70% reduce 0%
17/06/06 16:25:07 INFO mapreduce.Job:  map 71% reduce 0%
17/06/06 16:25:11 INFO mapreduce.Job:  map 72% reduce 0%
17/06/06 16:25:12 INFO mapreduce.Job:  map 73% reduce 0%
17/06/06 16:25:19 INFO mapreduce.Job:  map 74% reduce 0%
17/06/06 16:25:21 INFO mapreduce.Job:  map 75% reduce 0%
17/06/06 16:25:26 INFO mapreduce.Job:  map 76% reduce 0%
17/06/06 16:25:29 INFO mapreduce.Job:  map 77% reduce 0%
17/06/06 16:25:33 INFO mapreduce.Job:  map 78% reduce 0%
17/06/06 16:25:38 INFO mapreduce.Job:  map 79% reduce 0%
17/06/06 16:25:40 INFO mapreduce.Job:  map 80% reduce 0%
17/06/06 16:25:45 INFO mapreduce.Job:  map 81% reduce 0%
17/06/06 16:25:49 INFO mapreduce.Job:  map 82% reduce 0%
17/06/06 16:25:55 INFO mapreduce.Job:  map 83% reduce 0%
17/06/06 16:25:59 INFO mapreduce.Job:  map 83% reduce 3%
17/06/06 16:26:00 INFO mapreduce.Job:  map 83% reduce 5%
17/06/06 16:26:01 INFO mapreduce.Job:  map 83% reduce 7%
17/06/06 16:26:02 INFO mapreduce.Job:  map 83% reduce 8%
17/06/06 16:26:04 INFO mapreduce.Job:  map 83% reduce 9%
17/06/06 16:26:05 INFO mapreduce.Job:  map 83% reduce 10%
17/06/06 16:26:06 INFO mapreduce.Job:  map 83% reduce 11%
17/06/06 16:26:07 INFO mapreduce.Job:  map 84% reduce 12%
17/06/06 16:26:12 INFO mapreduce.Job:  map 84% reduce 13%
17/06/06 16:26:17 INFO mapreduce.Job:  map 85% reduce 13%
17/06/06 16:26:21 INFO mapreduce.Job:  map 85% reduce 14%
17/06/06 16:26:25 INFO mapreduce.Job:  map 86% reduce 14%
17/06/06 16:26:31 INFO mapreduce.Job:  map 87% reduce 14%
17/06/06 16:26:38 INFO mapreduce.Job:  map 88% reduce 14%
17/06/06 16:26:42 INFO mapreduce.Job:  map 88% reduce 15%
17/06/06 16:26:48 INFO mapreduce.Job:  map 89% reduce 15%
17/06/06 16:26:56 INFO mapreduce.Job:  map 90% reduce 15%
17/06/06 16:27:06 INFO mapreduce.Job:  map 91% reduce 15%
17/06/06 16:27:15 INFO mapreduce.Job:  map 92% reduce 15%
17/06/06 16:27:20 INFO mapreduce.Job:  map 93% reduce 15%
17/06/06 16:27:28 INFO mapreduce.Job:  map 93% reduce 16%
17/06/06 16:27:29 INFO mapreduce.Job:  map 94% reduce 16%
17/06/06 16:27:38 INFO mapreduce.Job:  map 95% reduce 16%
17/06/06 16:27:45 INFO mapreduce.Job:  map 96% reduce 16%
17/06/06 16:27:53 INFO mapreduce.Job:  map 97% reduce 16%
17/06/06 16:28:03 INFO mapreduce.Job:  map 98% reduce 16%
17/06/06 16:28:11 INFO mapreduce.Job:  map 99% reduce 16%
17/06/06 16:28:15 INFO mapreduce.Job:  map 99% reduce 17%
17/06/06 16:28:17 INFO mapreduce.Job:  map 100% reduce 17%
17/06/06 16:28:23 INFO mapreduce.Job:  map 100% reduce 20%
17/06/06 16:28:24 INFO mapreduce.Job:  map 100% reduce 24%
17/06/06 16:28:25 INFO mapreduce.Job:  map 100% reduce 30%
17/06/06 16:28:26 INFO mapreduce.Job:  map 100% reduce 32%
17/06/06 16:28:27 INFO mapreduce.Job:  map 100% reduce 35%
17/06/06 16:28:28 INFO mapreduce.Job:  map 100% reduce 38%
17/06/06 16:28:29 INFO mapreduce.Job:  map 100% reduce 39%
17/06/06 16:28:30 INFO mapreduce.Job:  map 100% reduce 40%
17/06/06 16:28:31 INFO mapreduce.Job:  map 100% reduce 42%
17/06/06 16:28:33 INFO mapreduce.Job:  map 100% reduce 43%
17/06/06 16:28:34 INFO mapreduce.Job:  map 100% reduce 46%
17/06/06 16:28:35 INFO mapreduce.Job:  map 100% reduce 48%
17/06/06 16:28:36 INFO mapreduce.Job:  map 100% reduce 49%
17/06/06 16:28:37 INFO mapreduce.Job:  map 100% reduce 50%
17/06/06 16:28:38 INFO mapreduce.Job:  map 100% reduce 51%
17/06/06 16:28:39 INFO mapreduce.Job:  map 100% reduce 52%
17/06/06 16:28:40 INFO mapreduce.Job:  map 100% reduce 58%
17/06/06 16:28:41 INFO mapreduce.Job:  map 100% reduce 60%
17/06/06 16:28:42 INFO mapreduce.Job:  map 100% reduce 61%
17/06/06 16:28:43 INFO mapreduce.Job:  map 100% reduce 62%
17/06/06 16:28:45 INFO mapreduce.Job:  map 100% reduce 63%
17/06/06 16:28:46 INFO mapreduce.Job:  map 100% reduce 65%
17/06/06 16:28:47 INFO mapreduce.Job:  map 100% reduce 66%
17/06/06 16:28:49 INFO mapreduce.Job:  map 100% reduce 67%
17/06/06 16:28:50 INFO mapreduce.Job:  map 100% reduce 71%
17/06/06 16:28:53 INFO mapreduce.Job:  map 100% reduce 73%
17/06/06 16:28:54 INFO mapreduce.Job:  map 100% reduce 75%
17/06/06 16:28:57 INFO mapreduce.Job:  map 100% reduce 80%
17/06/06 16:29:00 INFO mapreduce.Job:  map 100% reduce 82%
17/06/06 16:29:02 INFO mapreduce.Job:  map 100% reduce 84%
17/06/06 16:29:03 INFO mapreduce.Job:  map 100% reduce 85%
17/06/06 16:29:06 INFO mapreduce.Job:  map 100% reduce 90%
17/06/06 16:29:08 INFO mapreduce.Job:  map 100% reduce 91%
17/06/06 16:29:09 INFO mapreduce.Job:  map 100% reduce 92%
17/06/06 16:29:12 INFO mapreduce.Job:  map 100% reduce 93%
17/06/06 16:29:14 INFO mapreduce.Job:  map 100% reduce 94%
17/06/06 16:29:16 INFO mapreduce.Job:  map 100% reduce 95%
17/06/06 16:29:17 INFO mapreduce.Job:  map 100% reduce 96%
17/06/06 16:29:24 INFO mapreduce.Job:  map 100% reduce 97%
17/06/06 16:29:25 INFO mapreduce.Job:  map 100% reduce 98%
17/06/06 16:29:27 INFO mapreduce.Job:  map 100% reduce 99%
17/06/06 16:29:30 INFO mapreduce.Job:  map 100% reduce 100%
17/06/06 16:29:34 INFO mapreduce.Job: Job job_1496756043472_0007 completed successfully
17/06/06 16:29:34 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=4478754527
                FILE: Number of bytes written=8892057448
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=10000046500
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=924
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=16
        Job Counters
                Launched map tasks=300
                Launched reduce tasks=8
                Data-local map tasks=300
                Total time spent by all maps in occupied slots (ms)=2428769
                Total time spent by all reduces in occupied slots (ms)=947145
                Total time spent by all map tasks (ms)=2428769
                Total time spent by all reduce tasks (ms)=947145
                Total vcore-seconds taken by all map tasks=2428769
                Total vcore-seconds taken by all reduce tasks=947145
                Total megabyte-seconds taken by all map tasks=2487059456
                Total megabyte-seconds taken by all reduce tasks=969876480
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Map output bytes=10200000000
                Map output materialized bytes=4375221247
                Input split bytes=46500
                Combine input records=0
                Combine output records=0
                Reduce input groups=100000000
                Reduce shuffle bytes=4375221247
                Reduce input records=100000000
                Reduce output records=100000000
                Spilled Records=200000000
                Shuffled Maps =2400
                Failed Shuffles=0
                Merged Map outputs=2400
                GC time elapsed (ms)=32521
                CPU time spent (ms)=1609150
                Physical memory (bytes) snapshot=145291112448
                Virtual memory (bytes) snapshot=482488455168
                Total committed heap usage (bytes)=175297789952
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=10000000000
        File Output Format Counters
                Bytes Written=10000000000
17/06/06 16:29:34 INFO terasort.TeraSort: done

real    9m30.709s
user    0m12.315s
sys     0m1.411s
```
