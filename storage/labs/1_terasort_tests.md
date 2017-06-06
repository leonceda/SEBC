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

