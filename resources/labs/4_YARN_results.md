 * Slowest run

+++++++++++++++++++++++++++++++++++++++
-               PERF RUN               -
+++++++++++++++++++++++++++++++++++++++
-Dmapreduce.job.maps=4
-Dmapreduce.map.memory.mb=1024
-Dmapreduce.map.java.opts.max.heap=819
-Dmapreduce.job.reduces=1
-Dmapreduce.reduce.java.opts.max.heap=819
TeraGen time: 1:18.91 real,7.28 user,0.90 sys
TeraSort time: 3:10.14 real,11.22 user,1.19 sys


 * Fast run

+++++++++++++++++++++++++++++++++++++++
-               PERF RUN               -
+++++++++++++++++++++++++++++++++++++++
-Dmapreduce.job.maps=4
-Dmapreduce.map.memory.mb=512
-Dmapreduce.map.java.opts.max.heap=409
-Dmapreduce.job.reduces=2
-Dmapreduce.reduce.java.opts.max.heap=409
TeraGen time: 1:15.65 real,7.07 user,0.84 sys
TeraSort time: 2:17.89 real,10.11 user,0.97 sys
