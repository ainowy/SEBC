<p>

<b> teragen command </b>
[bavaria@ip-172-31-12-49 ~]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -D dfs.block.size=16777216 -D mapreduce.map.tasks=8 51200000 /user/bavaria/tgen512m
17/08/08 15:37:16 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-12-49.eu-west-1.compute.internal/172.31.12.49:8032
17/08/08 15:37:17 INFO terasort.TeraSort: Generating 51200000 using 2
17/08/08 15:37:17 INFO mapreduce.JobSubmitter: number of splits:2
17/08/08 15:37:17 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/08/08 15:37:17 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1502206036719_0002
17/08/08 15:37:17 INFO impl.YarnClientImpl: Submitted application application_1502206036719_0002
17/08/08 15:37:18 INFO mapreduce.Job: The url to track the job: http://ip-172-31-12-49.eu-west-1.compute.internal:8088/proxy/application_1502206036719_0002/
17/08/08 15:37:18 INFO mapreduce.Job: Running job: job_1502206036719_0002
17/08/08 15:37:26 INFO mapreduce.Job: Job job_1502206036719_0002 running in uber mode : false
17/08/08 15:37:26 INFO mapreduce.Job:  map 0% reduce 0%
17/08/08 15:37:39 INFO mapreduce.Job:  map 5% reduce 0%
17/08/08 15:37:40 INFO mapreduce.Job:  map 9% reduce 0%
17/08/08 15:37:42 INFO mapreduce.Job:  map 12% reduce 0%
17/08/08 15:37:43 INFO mapreduce.Job:  map 14% reduce 0%
17/08/08 15:37:45 INFO mapreduce.Job:  map 15% reduce 0%
17/08/08 15:37:46 INFO mapreduce.Job:  map 16% reduce 0%
17/08/08 15:37:48 INFO mapreduce.Job:  map 18% reduce 0%
17/08/08 15:37:49 INFO mapreduce.Job:  map 19% reduce 0%
17/08/08 15:37:51 INFO mapreduce.Job:  map 20% reduce 0%
17/08/08 15:37:52 INFO mapreduce.Job:  map 21% reduce 0%
17/08/08 15:37:54 INFO mapreduce.Job:  map 23% reduce 0%
17/08/08 15:37:55 INFO mapreduce.Job:  map 24% reduce 0%
17/08/08 15:37:57 INFO mapreduce.Job:  map 26% reduce 0%
17/08/08 15:37:58 INFO mapreduce.Job:  map 28% reduce 0%
17/08/08 15:38:00 INFO mapreduce.Job:  map 29% reduce 0%
17/08/08 15:38:01 INFO mapreduce.Job:  map 30% reduce 0%
17/08/08 15:38:03 INFO mapreduce.Job:  map 32% reduce 0%
17/08/08 15:38:04 INFO mapreduce.Job:  map 33% reduce 0%
17/08/08 15:38:06 INFO mapreduce.Job:  map 34% reduce 0%
17/08/08 15:38:07 INFO mapreduce.Job:  map 35% reduce 0%
17/08/08 15:38:09 INFO mapreduce.Job:  map 37% reduce 0%
17/08/08 15:38:10 INFO mapreduce.Job:  map 39% reduce 0%
17/08/08 15:38:12 INFO mapreduce.Job:  map 40% reduce 0%
17/08/08 15:38:13 INFO mapreduce.Job:  map 42% reduce 0%
17/08/08 15:38:15 INFO mapreduce.Job:  map 43% reduce 0%
17/08/08 15:38:16 INFO mapreduce.Job:  map 44% reduce 0%
17/08/08 15:38:18 INFO mapreduce.Job:  map 45% reduce 0%
17/08/08 15:38:19 INFO mapreduce.Job:  map 46% reduce 0%
17/08/08 15:38:21 INFO mapreduce.Job:  map 48% reduce 0%
17/08/08 15:38:22 INFO mapreduce.Job:  map 50% reduce 0%
17/08/08 15:38:24 INFO mapreduce.Job:  map 51% reduce 0%
17/08/08 15:38:25 INFO mapreduce.Job:  map 52% reduce 0%
17/08/08 15:38:27 INFO mapreduce.Job:  map 54% reduce 0%
17/08/08 15:38:28 INFO mapreduce.Job:  map 55% reduce 0%
17/08/08 15:38:30 INFO mapreduce.Job:  map 56% reduce 0%
17/08/08 15:38:31 INFO mapreduce.Job:  map 57% reduce 0%
17/08/08 15:38:33 INFO mapreduce.Job:  map 58% reduce 0%
17/08/08 15:38:34 INFO mapreduce.Job:  map 60% reduce 0%
17/08/08 15:38:36 INFO mapreduce.Job:  map 61% reduce 0%
17/08/08 15:38:37 INFO mapreduce.Job:  map 63% reduce 0%
17/08/08 15:38:39 INFO mapreduce.Job:  map 64% reduce 0%
17/08/08 15:38:40 INFO mapreduce.Job:  map 66% reduce 0%
17/08/08 15:38:43 INFO mapreduce.Job:  map 67% reduce 0%
17/08/08 15:38:44 INFO mapreduce.Job:  map 69% reduce 0%
17/08/08 15:38:46 INFO mapreduce.Job:  map 70% reduce 0%
17/08/08 15:38:47 INFO mapreduce.Job:  map 71% reduce 0%
17/08/08 15:38:49 INFO mapreduce.Job:  map 73% reduce 0%
17/08/08 15:38:50 INFO mapreduce.Job:  map 74% reduce 0%
17/08/08 15:38:52 INFO mapreduce.Job:  map 75% reduce 0%
17/08/08 15:38:53 INFO mapreduce.Job:  map 76% reduce 0%
17/08/08 15:38:55 INFO mapreduce.Job:  map 78% reduce 0%
17/08/08 15:38:56 INFO mapreduce.Job:  map 79% reduce 0%
17/08/08 15:38:58 INFO mapreduce.Job:  map 80% reduce 0%
17/08/08 15:38:59 INFO mapreduce.Job:  map 81% reduce 0%
17/08/08 15:39:01 INFO mapreduce.Job:  map 83% reduce 0%
17/08/08 15:39:02 INFO mapreduce.Job:  map 84% reduce 0%
17/08/08 15:39:04 INFO mapreduce.Job:  map 86% reduce 0%
17/08/08 15:39:05 INFO mapreduce.Job:  map 87% reduce 0%
17/08/08 15:39:07 INFO mapreduce.Job:  map 88% reduce 0%
17/08/08 15:39:08 INFO mapreduce.Job:  map 90% reduce 0%
17/08/08 15:39:10 INFO mapreduce.Job:  map 91% reduce 0%
17/08/08 15:39:11 INFO mapreduce.Job:  map 92% reduce 0%
17/08/08 15:39:13 INFO mapreduce.Job:  map 94% reduce 0%
17/08/08 15:39:14 INFO mapreduce.Job:  map 95% reduce 0%
17/08/08 15:39:16 INFO mapreduce.Job:  map 97% reduce 0%
17/08/08 15:39:17 INFO mapreduce.Job:  map 98% reduce 0%
17/08/08 15:39:20 INFO mapreduce.Job:  map 100% reduce 0%
17/08/08 15:39:20 INFO mapreduce.Job: Job job_1502206036719_0002 completed successfully
17/08/08 15:39:20 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=241240
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=170
                HDFS: Number of bytes written=5120000000
                HDFS: Number of read operations=8
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=4
        Job Counters
                Launched map tasks=2
                Other local map tasks=2
                Total time spent by all maps in occupied slots (ms)=218690
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=218690
                Total vcore-seconds taken by all map tasks=218690
                Total megabyte-seconds taken by all map tasks=223938560
        Map-Reduce Framework
                Map input records=51200000
                Map output records=51200000
                Input split bytes=170
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=554
                CPU time spent (ms)=85130
                Physical memory (bytes) snapshot=720715776
                Virtual memory (bytes) snapshot=5567647744
                Total committed heap usage (bytes)=311427072
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=109963291816450258
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=5120000000

real    2m7.804s
user    0m7.316s
sys     0m0.798s


<b>output hdfs dir</b>

[bavaria@ip-172-31-12-49 ~]$ hdfs dfs -ls /user/bavaria/tgen512m
Found 3 items
-rw-r--r--   3 bavaria supergroup          0 2017-08-08 15:39 /user/bavaria/tgen512m/_SUCCESS
-rw-r--r--   3 bavaria supergroup 2560000000 2017-08-08 15:39 /user/bavaria/tgen512m/part-m-00000
-rw-r--r--   3 bavaria supergroup 2560000000 2017-08-08 15:39 /user/bavaria/tgen512m/part-m-00001

<b>blocks linked</b>

[bavaria@ip-172-31-12-49 ~]$ hdfs fsck -blocks /user/bavaria/tgen512m
Connecting to namenode via http://ip-172-31-12-49.eu-west-1.compute.internal:50070
FSCK started by bavaria (auth:SIMPLE) from /172.31.12.49 for path /user/bavaria/tgen512m at Tue Aug 08 15:41:18 UTC 2017
...Status: HEALTHY
 Total size:    5120000000 B
 Total dirs:    1
 Total files:   3
 Total symlinks:                0
 Total blocks (validated):      306 (avg. block size 16732026 B)
 Minimally replicated blocks:   306 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Tue Aug 08 15:41:18 UTC 2017 in 20 milliseconds


The filesystem under path '/user/bavaria/tgen512m' is HEALTHY



</p>
