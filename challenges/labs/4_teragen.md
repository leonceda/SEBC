
```
[root@ip-172-31-6-211 ~]# time hadoop jar /opt/cloudera/parcels/CDH-5.10.1-1.cdh5.10.1.p0.10/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -Ddfs.blocksize=33554432 51200000 gen512m



17/06/09 10:48:16 INFO Configuration.deprecation: session.id is deprecated. Instead, use dfs.metrics.session-id
17/06/09 10:48:16 INFO jvm.JvmMetrics: Initializing JVM Metrics with processName=JobTracker, sessionId=
17/06/09 10:48:17 INFO terasort.TeraGen: Generating 51200000 using 1
17/06/09 10:48:17 INFO mapreduce.JobSubmitter: number of splits:1
17/06/09 10:48:17 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_local654678358_0001
17/06/09 10:48:17 INFO mapreduce.Job: The url to track the job: http://localhost:8080/
17/06/09 10:48:17 INFO mapreduce.Job: Running job: job_local654678358_0001
17/06/09 10:48:17 INFO mapred.LocalJobRunner: OutputCommitter set in config null
17/06/09 10:48:17 INFO output.FileOutputCommitter: File Output Committer Algorithm version is 1
17/06/09 10:48:17 INFO mapred.LocalJobRunner: OutputCommitter is org.apache.hadoop.mapreduce.lib.output.FileOutputCommitter
17/06/09 10:48:17 INFO mapred.LocalJobRunner: Waiting for map tasks
17/06/09 10:48:17 INFO mapred.LocalJobRunner: Starting task: attempt_local654678358_0001_m_000000_0
17/06/09 10:48:17 INFO output.FileOutputCommitter: File Output Committer Algorithm version is 1
17/06/09 10:48:17 INFO mapred.Task:  Using ResourceCalculatorProcessTree : [ ]
17/06/09 10:48:17 INFO mapred.MapTask: Processing split: org.apache.hadoop.examples.terasort.TeraGen$RangeInputFormat$RangeInputSplit@41dead19
17/06/09 10:48:18 INFO mapreduce.Job: Job job_local654678358_0001 running in uber mode : false
17/06/09 10:48:18 INFO mapreduce.Job:  map 0% reduce 0%
17/06/09 10:48:29 INFO mapred.LocalJobRunner: map > map
17/06/09 10:48:30 INFO mapreduce.Job:  map 18% reduce 0%
17/06/09 10:48:35 INFO mapred.LocalJobRunner: map > map
17/06/09 10:48:36 INFO mapreduce.Job:  map 26% reduce 0%
17/06/09 10:48:41 INFO mapred.LocalJobRunner: map > map
17/06/09 10:48:42 INFO mapreduce.Job:  map 36% reduce 0%
17/06/09 10:48:47 INFO mapred.LocalJobRunner: map > map
17/06/09 10:48:48 INFO mapreduce.Job:  map 45% reduce 0%
17/06/09 10:48:53 INFO mapred.LocalJobRunner: map > map
17/06/09 10:48:54 INFO mapreduce.Job:  map 53% reduce 0%
17/06/09 10:48:59 INFO mapred.LocalJobRunner: map > map
17/06/09 10:49:00 INFO mapreduce.Job:  map 63% reduce 0%
17/06/09 10:49:05 INFO mapred.LocalJobRunner: map > map
17/06/09 10:49:06 INFO mapreduce.Job:  map 72% reduce 0%
17/06/09 10:49:11 INFO mapred.LocalJobRunner: map > map
17/06/09 10:49:12 INFO mapreduce.Job:  map 81% reduce 0%
17/06/09 10:49:17 INFO mapred.LocalJobRunner: map > map
17/06/09 10:49:18 INFO mapreduce.Job:  map 90% reduce 0%
17/06/09 10:49:23 INFO mapred.LocalJobRunner: map > map
17/06/09 10:49:24 INFO mapreduce.Job:  map 99% reduce 0%
17/06/09 10:49:24 INFO mapred.LocalJobRunner: map > map
17/06/09 10:49:24 INFO mapred.Task: Task:attempt_local654678358_0001_m_000000_0 is done. And is in the process of committing
17/06/09 10:49:24 INFO mapred.LocalJobRunner: map > map
17/06/09 10:49:24 INFO mapred.Task: Task attempt_local654678358_0001_m_000000_0 is allowed to commit now
17/06/09 10:49:24 INFO output.FileOutputCommitter: Saved output of task 'attempt_local654678358_0001_m_000000_0' to file:/root/gen512m/_temporary/0/task_local654678358_0001_m_000000
17/06/09 10:49:24 INFO mapred.LocalJobRunner: map
17/06/09 10:49:24 INFO mapred.Task: Task 'attempt_local654678358_0001_m_000000_0' done.
17/06/09 10:49:24 INFO mapred.LocalJobRunner: Finishing task: attempt_local654678358_0001_m_000000_0
17/06/09 10:49:24 INFO mapred.LocalJobRunner: map task executor complete.
17/06/09 10:49:25 INFO mapreduce.Job:  map 100% reduce 0%
17/06/09 10:49:25 INFO mapreduce.Job: Job job_local654678358_0001 completed successfully
17/06/09 10:49:25 INFO mapreduce.Job: Counters: 16
        File System Counters
                FILE: Number of bytes read=276327
                FILE: Number of bytes written=5160560147
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
        Map-Reduce Framework
                Map input records=51200000
                Map output records=51200000
                Input split bytes=83
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=294
                Total committed heap usage (bytes)=195035136
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=109963291816450258
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=5160000008

real    1m11.134s
user    0m59.168s
sys     0m12.529s

```
