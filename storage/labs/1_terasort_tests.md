<h1><b> Terasort </b></h1>
<pre>

[root@ip-172-31-39-40 ~]# time hadoop jar /opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort tera_gen10G /user/ainowy/terasort512m
17/06/07 11:05:42 INFO terasort.TeraSort: starting
17/06/07 11:05:43 INFO input.FileInputFormat: Total input paths to process : 4
Spent 211ms computing base-splits.
Spent 7ms computing TeraScheduler splits.
Computing input splits took 220ms
Sampling 10 splits of 320
Making 6 from 100000 sampled records
Computing parititions took 689ms
Spent 913ms computing partitions.
17/06/07 11:05:44 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-39-40.eu-west-1.compute.internal/172.31.39.40:8032
17/06/07 11:05:45 INFO mapreduce.JobSubmitter: number of splits:320
17/06/07 11:05:45 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1496824411518_0005
17/06/07 11:05:45 INFO impl.YarnClientImpl: Submitted application application_1496824411518_0005
17/06/07 11:05:45 INFO mapreduce.Job: The url to track the job: http://ip-172-31-39-40.eu-west-1.compute.internal:8088/proxy/application_1496824411518_0005/
17/06/07 11:05:45 INFO mapreduce.Job: Running job: job_1496824411518_0005
17/06/07 11:05:51 INFO mapreduce.Job: Job job_1496824411518_0005 running in uber mode : false
17/06/07 11:05:51 INFO mapreduce.Job:  map 0% reduce 0%
17/06/07 11:05:59 INFO mapreduce.Job:  map 1% reduce 0%
17/06/07 11:06:02 INFO mapreduce.Job:  map 3% reduce 0%
17/06/07 11:06:12 INFO mapreduce.Job:  map 4% reduce 0%
17/06/07 11:06:13 INFO mapreduce.Job:  map 5% reduce 0%
17/06/07 11:06:15 INFO mapreduce.Job:  map 6% reduce 0%
17/06/07 11:06:22 INFO mapreduce.Job:  map 8% reduce 0%
17/06/07 11:06:28 INFO mapreduce.Job:  map 9% reduce 0%
17/06/07 11:06:32 INFO mapreduce.Job:  map 10% reduce 0%
17/06/07 11:06:33 INFO mapreduce.Job:  map 11% reduce 0%
17/06/07 11:06:42 INFO mapreduce.Job:  map 13% reduce 0%
17/06/07 11:06:43 INFO mapreduce.Job:  map 14% reduce 0%
17/06/07 11:06:52 INFO mapreduce.Job:  map 16% reduce 0%
17/06/07 11:06:56 INFO mapreduce.Job:  map 17% reduce 0%
17/06/07 11:07:02 INFO mapreduce.Job:  map 19% reduce 0%
17/06/07 11:07:09 INFO mapreduce.Job:  map 20% reduce 0%
17/06/07 11:07:12 INFO mapreduce.Job:  map 22% reduce 0%
17/06/07 11:07:22 INFO mapreduce.Job:  map 24% reduce 0%
17/06/07 11:07:24 INFO mapreduce.Job:  map 25% reduce 0%
17/06/07 11:07:30 INFO mapreduce.Job:  map 26% reduce 0%
17/06/07 11:07:31 INFO mapreduce.Job:  map 27% reduce 0%
17/06/07 11:07:32 INFO mapreduce.Job:  map 28% reduce 0%
17/06/07 11:07:40 INFO mapreduce.Job:  map 29% reduce 0%
17/06/07 11:07:42 INFO mapreduce.Job:  map 30% reduce 0%
17/06/07 11:07:45 INFO mapreduce.Job:  map 31% reduce 0%
17/06/07 11:07:49 INFO mapreduce.Job:  map 32% reduce 0%
17/06/07 11:07:52 INFO mapreduce.Job:  map 33% reduce 0%
17/06/07 11:07:58 INFO mapreduce.Job:  map 34% reduce 0%
17/06/07 11:07:59 INFO mapreduce.Job:  map 35% reduce 0%
17/06/07 11:08:02 INFO mapreduce.Job:  map 36% reduce 0%
17/06/07 11:08:06 INFO mapreduce.Job:  map 37% reduce 0%
17/06/07 11:08:12 INFO mapreduce.Job:  map 38% reduce 0%
17/06/07 11:08:13 INFO mapreduce.Job:  map 39% reduce 0%
17/06/07 11:08:18 INFO mapreduce.Job:  map 40% reduce 0%
17/06/07 11:08:22 INFO mapreduce.Job:  map 41% reduce 0%
17/06/07 11:08:24 INFO mapreduce.Job:  map 42% reduce 0%
17/06/07 11:08:26 INFO mapreduce.Job:  map 43% reduce 0%
17/06/07 11:08:32 INFO mapreduce.Job:  map 44% reduce 0%
17/06/07 11:08:34 INFO mapreduce.Job:  map 45% reduce 0%
17/06/07 11:08:40 INFO mapreduce.Job:  map 46% reduce 0%
17/06/07 11:08:42 INFO mapreduce.Job:  map 47% reduce 0%
17/06/07 11:08:44 INFO mapreduce.Job:  map 48% reduce 0%
17/06/07 11:08:52 INFO mapreduce.Job:  map 49% reduce 0%
17/06/07 11:08:53 INFO mapreduce.Job:  map 50% reduce 0%
17/06/07 11:08:54 INFO mapreduce.Job:  map 51% reduce 0%
17/06/07 11:09:02 INFO mapreduce.Job:  map 52% reduce 0%
17/06/07 11:09:03 INFO mapreduce.Job:  map 53% reduce 0%
17/06/07 11:09:08 INFO mapreduce.Job:  map 54% reduce 0%
17/06/07 11:09:12 INFO mapreduce.Job:  map 56% reduce 0%
17/06/07 11:09:16 INFO mapreduce.Job:  map 57% reduce 0%
17/06/07 11:09:22 INFO mapreduce.Job:  map 59% reduce 0%
17/06/07 11:09:29 INFO mapreduce.Job:  map 60% reduce 0%
17/06/07 11:09:32 INFO mapreduce.Job:  map 61% reduce 0%
17/06/07 11:09:33 INFO mapreduce.Job:  map 62% reduce 0%
17/06/07 11:09:39 INFO mapreduce.Job:  map 63% reduce 0%
17/06/07 11:09:43 INFO mapreduce.Job:  map 64% reduce 0%
17/06/07 11:09:45 INFO mapreduce.Job:  map 65% reduce 0%
17/06/07 11:09:49 INFO mapreduce.Job:  map 66% reduce 0%
17/06/07 11:09:53 INFO mapreduce.Job:  map 67% reduce 0%
17/06/07 11:09:57 INFO mapreduce.Job:  map 68% reduce 0%
17/06/07 11:09:59 INFO mapreduce.Job:  map 69% reduce 0%
17/06/07 11:10:03 INFO mapreduce.Job:  map 70% reduce 0%
17/06/07 11:10:06 INFO mapreduce.Job:  map 71% reduce 0%
17/06/07 11:10:11 INFO mapreduce.Job:  map 72% reduce 0%
17/06/07 11:10:13 INFO mapreduce.Job:  map 73% reduce 0%
17/06/07 11:10:17 INFO mapreduce.Job:  map 74% reduce 0%
17/06/07 11:10:23 INFO mapreduce.Job:  map 75% reduce 0%
17/06/07 11:10:24 INFO mapreduce.Job:  map 76% reduce 0%
17/06/07 11:10:26 INFO mapreduce.Job:  map 77% reduce 0%
17/06/07 11:10:33 INFO mapreduce.Job:  map 78% reduce 0%
17/06/07 11:10:34 INFO mapreduce.Job:  map 79% reduce 0%
17/06/07 11:10:39 INFO mapreduce.Job:  map 80% reduce 0%
17/06/07 11:10:43 INFO mapreduce.Job:  map 82% reduce 0%
17/06/07 11:10:50 INFO mapreduce.Job:  map 83% reduce 0%
17/06/07 11:10:55 INFO mapreduce.Job:  map 83% reduce 3%
17/06/07 11:10:56 INFO mapreduce.Job:  map 83% reduce 6%
17/06/07 11:10:57 INFO mapreduce.Job:  map 83% reduce 8%
17/06/07 11:10:58 INFO mapreduce.Job:  map 83% reduce 9%
17/06/07 11:10:59 INFO mapreduce.Job:  map 83% reduce 12%
17/06/07 11:11:00 INFO mapreduce.Job:  map 84% reduce 13%
17/06/07 11:11:03 INFO mapreduce.Job:  map 84% reduce 14%
17/06/07 11:11:04 INFO mapreduce.Job:  map 84% reduce 15%
17/06/07 11:11:05 INFO mapreduce.Job:  map 84% reduce 18%
17/06/07 11:11:07 INFO mapreduce.Job:  map 85% reduce 19%
17/06/07 11:11:09 INFO mapreduce.Job:  map 85% reduce 20%
17/06/07 11:11:10 INFO mapreduce.Job:  map 85% reduce 21%
17/06/07 11:11:11 INFO mapreduce.Job:  map 85% reduce 24%
17/06/07 11:11:14 INFO mapreduce.Job:  map 86% reduce 24%
17/06/07 11:11:21 INFO mapreduce.Job:  map 87% reduce 24%
17/06/07 11:11:26 INFO mapreduce.Job:  map 88% reduce 24%
17/06/07 11:11:34 INFO mapreduce.Job:  map 89% reduce 24%
17/06/07 11:11:35 INFO mapreduce.Job:  map 89% reduce 25%
17/06/07 11:11:42 INFO mapreduce.Job:  map 90% reduce 25%
17/06/07 11:11:48 INFO mapreduce.Job:  map 91% reduce 25%
17/06/07 11:11:55 INFO mapreduce.Job:  map 92% reduce 25%
17/06/07 11:11:57 INFO mapreduce.Job:  map 92% reduce 26%
17/06/07 11:12:00 INFO mapreduce.Job:  map 93% reduce 26%
17/06/07 11:12:09 INFO mapreduce.Job:  map 94% reduce 26%
17/06/07 11:12:16 INFO mapreduce.Job:  map 95% reduce 26%
17/06/07 11:12:23 INFO mapreduce.Job:  map 96% reduce 26%
17/06/07 11:12:26 INFO mapreduce.Job:  map 96% reduce 27%
17/06/07 11:12:30 INFO mapreduce.Job:  map 97% reduce 27%
17/06/07 11:12:36 INFO mapreduce.Job:  map 98% reduce 27%
17/06/07 11:12:44 INFO mapreduce.Job:  map 99% reduce 27%
17/06/07 11:12:48 INFO mapreduce.Job:  map 99% reduce 28%
17/06/07 11:12:51 INFO mapreduce.Job:  map 100% reduce 28%
17/06/07 11:12:56 INFO mapreduce.Job:  map 100% reduce 42%
17/06/07 11:12:57 INFO mapreduce.Job:  map 100% reduce 53%
17/06/07 11:12:58 INFO mapreduce.Job:  map 100% reduce 58%
17/06/07 11:13:00 INFO mapreduce.Job:  map 100% reduce 59%
17/06/07 11:13:01 INFO mapreduce.Job:  map 100% reduce 60%
17/06/07 11:13:02 INFO mapreduce.Job:  map 100% reduce 61%
17/06/07 11:13:03 INFO mapreduce.Job:  map 100% reduce 62%
17/06/07 11:13:04 INFO mapreduce.Job:  map 100% reduce 63%
17/06/07 11:13:06 INFO mapreduce.Job:  map 100% reduce 65%
17/06/07 11:13:08 INFO mapreduce.Job:  map 100% reduce 66%
17/06/07 11:13:09 INFO mapreduce.Job:  map 100% reduce 68%
17/06/07 11:13:11 INFO mapreduce.Job:  map 100% reduce 69%
17/06/07 11:13:12 INFO mapreduce.Job:  map 100% reduce 71%
17/06/07 11:13:13 INFO mapreduce.Job:  map 100% reduce 72%
17/06/07 11:13:15 INFO mapreduce.Job:  map 100% reduce 74%
17/06/07 11:13:17 INFO mapreduce.Job:  map 100% reduce 80%
17/06/07 11:13:19 INFO mapreduce.Job:  map 100% reduce 82%
17/06/07 11:13:22 INFO mapreduce.Job:  map 100% reduce 85%
17/06/07 11:13:25 INFO mapreduce.Job:  map 100% reduce 86%
17/06/07 11:13:28 INFO mapreduce.Job:  map 100% reduce 87%
17/06/07 11:13:29 INFO mapreduce.Job:  map 100% reduce 88%
17/06/07 11:13:31 INFO mapreduce.Job:  map 100% reduce 89%
17/06/07 11:13:34 INFO mapreduce.Job:  map 100% reduce 90%
17/06/07 11:13:37 INFO mapreduce.Job:  map 100% reduce 91%
17/06/07 11:13:40 INFO mapreduce.Job:  map 100% reduce 92%
17/06/07 11:13:41 INFO mapreduce.Job:  map 100% reduce 93%
17/06/07 11:13:43 INFO mapreduce.Job:  map 100% reduce 94%
17/06/07 11:13:46 INFO mapreduce.Job:  map 100% reduce 95%
(...)
17/06/07 11:13:48 INFO mapreduce.Job:  map 100% reduce 79%
17/06/07 11:13:49 INFO mapreduce.Job:  map 100% reduce 80%
17/06/07 11:13:53 INFO mapreduce.Job:  map 100% reduce 81%
17/06/07 11:13:56 INFO mapreduce.Job:  map 100% reduce 82%
17/06/07 11:13:59 INFO mapreduce.Job:  map 100% reduce 83%
17/06/07 11:14:00 INFO mapreduce.Job:  map 100% reduce 86%
17/06/07 11:14:03 INFO mapreduce.Job:  map 100% reduce 87%
17/06/07 11:14:06 INFO mapreduce.Job:  map 100% reduce 88%
17/06/07 11:14:09 INFO mapreduce.Job:  map 100% reduce 89%
17/06/07 11:14:12 INFO mapreduce.Job:  map 100% reduce 93%
17/06/07 11:14:15 INFO mapreduce.Job:  map 100% reduce 95%
17/06/07 11:14:18 INFO mapreduce.Job:  map 100% reduce 96%
17/06/07 11:14:21 INFO mapreduce.Job:  map 100% reduce 97%
17/06/07 11:14:27 INFO mapreduce.Job:  map 100% reduce 98%
17/06/07 11:14:30 INFO mapreduce.Job:  map 100% reduce 99%
17/06/07 11:14:33 INFO mapreduce.Job:  map 100% reduce 100%
17/06/07 11:14:33 INFO mapreduce.Job: Job job_1496824411518_0005 completed successfully
17/06/07 11:14:34 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=4816161403
                FILE: Number of bytes written=9553991776
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=10737467480
                HDFS: Number of bytes written=10737418200
                HDFS: Number of read operations=978
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=12
        Job Counters
                Failed reduce tasks=1
                Launched map tasks=320
                Launched reduce tasks=7
                Data-local map tasks=320
                Total time spent by all maps in occupied slots (ms)=2347580
                Total time spent by all reduces in occupied slots (ms)=1040746
                Total time spent by all map tasks (ms)=2347580
                Total time spent by all reduce tasks (ms)=1040746
                Total vcore-seconds taken by all map tasks=2347580
                Total vcore-seconds taken by all reduce tasks=1040746
                Total megabyte-seconds taken by all map tasks=2403921920
                Total megabyte-seconds taken by all reduce tasks=1065723904
        Map-Reduce Framework
                Map input records=107374182
                Map output records=107374182
                Map output bytes=10952166564
                Map output materialized bytes=4697547721
                Input split bytes=49280
                Combine input records=0
                Combine output records=0
                Reduce input groups=107374182
                Reduce shuffle bytes=4697547721
                Reduce input records=107374182
                Reduce output records=107374182
                Spilled Records=214748364
                Shuffled Maps =1920
                Failed Shuffles=0
                Merged Map outputs=1920
                GC time elapsed (ms)=48594
                CPU time spent (ms)=1630280
                Physical memory (bytes) snapshot=153903284224
                Virtual memory (bytes) snapshot=903439974400
                Total committed heap usage (bytes)=161633796096
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=10737418200
        File Output Format Counters
                Bytes Written=10737418200
17/06/07 11:14:34 INFO terasort.TeraSort: done

real    8m52.732s
user    0m10.283s
sys     0m1.116s


</pre>

<h1>Teragen</h1>
<pre>
[root@ip-172-31-39-40 ~]# time hadoop jar /opt/cloudera/parcels/CDH-5.8.3-1.cdh5                                                                                        .8.3.p0.2/lib/hadoop-mapreduce/hadoop-mapreduce-examples-2.6.0-cdh5.8.3.jar tera                                                                                        gen -Ddfs.block.size=33554432 -Dmapred.map.tasks=4 107374182 tera_gen10G
17/06/07 10:32:50 INFO client.RMProxy: Connecting to ResourceManager at ip-172-3                                                                                        1-39-40.eu-west-1.compute.internal/172.31.39.40:8032
17/06/07 10:32:50 INFO terasort.TeraSort: Generating 107374182 using 4
17/06/07 10:32:50 INFO mapreduce.JobSubmitter: number of splits:4
17/06/07 10:32:50 INFO Configuration.deprecation: dfs.block.size is deprecated.                                                                                         Instead, use dfs.blocksize
17/06/07 10:32:50 INFO Configuration.deprecation: mapred.map.tasks is deprecated                                                                                        . Instead, use mapreduce.job.maps
17/06/07 10:32:50 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_14                                                                                        96824411518_0003
17/06/07 10:32:51 INFO impl.YarnClientImpl: Submitted application application_14                                                                                        96824411518_0003
17/06/07 10:32:51 INFO mapreduce.Job: The url to track the job: http://ip-172-31                                                                                        -39-40.eu-west-1.compute.internal:8088/proxy/application_1496824411518_0003/
17/06/07 10:32:51 INFO mapreduce.Job: Running job: job_1496824411518_0003
17/06/07 10:32:57 INFO mapreduce.Job: Job job_1496824411518_0003 running in uber mode : false
17/06/07 10:32:57 INFO mapreduce.Job:  map 0% reduce 0%
17/06/07 10:33:08 INFO mapreduce.Job:  map 7% reduce 0%
17/06/07 10:33:10 INFO mapreduce.Job:  map 10% reduce 0%
17/06/07 10:33:11 INFO mapreduce.Job:  map 12% reduce 0%
17/06/07 10:33:13 INFO mapreduce.Job:  map 14% reduce 0%
17/06/07 10:33:14 INFO mapreduce.Job:  map 15% reduce 0%
17/06/07 10:33:16 INFO mapreduce.Job:  map 16% reduce 0%
17/06/07 10:33:17 INFO mapreduce.Job:  map 17% reduce 0%
17/06/07 10:33:19 INFO mapreduce.Job:  map 18% reduce 0%
17/06/07 10:33:20 INFO mapreduce.Job:  map 19% reduce 0%
17/06/07 10:33:22 INFO mapreduce.Job:  map 20% reduce 0%
17/06/07 10:33:25 INFO mapreduce.Job:  map 22% reduce 0%
17/06/07 10:33:26 INFO mapreduce.Job:  map 23% reduce 0%
17/06/07 10:33:29 INFO mapreduce.Job:  map 24% reduce 0%
17/06/07 10:33:31 INFO mapreduce.Job:  map 26% reduce 0%
17/06/07 10:33:32 INFO mapreduce.Job:  map 27% reduce 0%
17/06/07 10:33:34 INFO mapreduce.Job:  map 28% reduce 0%
17/06/07 10:33:35 INFO mapreduce.Job:  map 29% reduce 0%
17/06/07 10:33:37 INFO mapreduce.Job:  map 30% reduce 0%
17/06/07 10:33:38 INFO mapreduce.Job:  map 31% reduce 0%
17/06/07 10:33:40 INFO mapreduce.Job:  map 32% reduce 0%
17/06/07 10:33:41 INFO mapreduce.Job:  map 33% reduce 0%
17/06/07 10:33:43 INFO mapreduce.Job:  map 34% reduce 0%
17/06/07 10:33:44 INFO mapreduce.Job:  map 35% reduce 0%
17/06/07 10:33:46 INFO mapreduce.Job:  map 36% reduce 0%
17/06/07 10:33:47 INFO mapreduce.Job:  map 37% reduce 0%
17/06/07 10:33:49 INFO mapreduce.Job:  map 38% reduce 0%
17/06/07 10:33:51 INFO mapreduce.Job:  map 39% reduce 0%
17/06/07 10:33:53 INFO mapreduce.Job:  map 40% reduce 0%
17/06/07 10:33:54 INFO mapreduce.Job:  map 41% reduce 0%
17/06/07 10:33:56 INFO mapreduce.Job:  map 42% reduce 0%
17/06/07 10:33:57 INFO mapreduce.Job:  map 43% reduce 0%
17/06/07 10:33:59 INFO mapreduce.Job:  map 45% reduce 0%
17/06/07 10:34:02 INFO mapreduce.Job:  map 47% reduce 0%
17/06/07 10:34:05 INFO mapreduce.Job:  map 49% reduce 0%
17/06/07 10:34:08 INFO mapreduce.Job:  map 51% reduce 0%
17/06/07 10:34:11 INFO mapreduce.Job:  map 53% reduce 0%
17/06/07 10:34:14 INFO mapreduce.Job:  map 55% reduce 0%
17/06/07 10:34:17 INFO mapreduce.Job:  map 57% reduce 0%
17/06/07 10:34:19 INFO mapreduce.Job:  map 58% reduce 0%
17/06/07 10:34:20 INFO mapreduce.Job:  map 59% reduce 0%
17/06/07 10:34:22 INFO mapreduce.Job:  map 60% reduce 0%
17/06/07 10:34:23 INFO mapreduce.Job:  map 61% reduce 0%
17/06/07 10:34:26 INFO mapreduce.Job:  map 63% reduce 0%
17/06/07 10:34:28 INFO mapreduce.Job:  map 64% reduce 0%
17/06/07 10:34:29 INFO mapreduce.Job:  map 65% reduce 0%
17/06/07 10:34:31 INFO mapreduce.Job:  map 66% reduce 0%
17/06/07 10:34:32 INFO mapreduce.Job:  map 67% reduce 0%
17/06/07 10:34:35 INFO mapreduce.Job:  map 69% reduce 0%
17/06/07 10:34:38 INFO mapreduce.Job:  map 71% reduce 0%
17/06/07 10:34:41 INFO mapreduce.Job:  map 73% reduce 0%
17/06/07 10:34:44 INFO mapreduce.Job:  map 74% reduce 0%
17/06/07 10:34:46 INFO mapreduce.Job:  map 75% reduce 0%
17/06/07 10:34:47 INFO mapreduce.Job:  map 77% reduce 0%
17/06/07 10:34:50 INFO mapreduce.Job:  map 79% reduce 0%
17/06/07 10:34:53 INFO mapreduce.Job:  map 80% reduce 0%
17/06/07 10:34:56 INFO mapreduce.Job:  map 81% reduce 0%
17/06/07 10:34:57 INFO mapreduce.Job:  map 82% reduce 0%
17/06/07 10:34:59 INFO mapreduce.Job:  map 83% reduce 0%
17/06/07 10:35:00 INFO mapreduce.Job:  map 84% reduce 0%
17/06/07 10:35:03 INFO mapreduce.Job:  map 86% reduce 0%
17/06/07 10:35:06 INFO mapreduce.Job:  map 88% reduce 0%
17/06/07 10:35:09 INFO mapreduce.Job:  map 90% reduce 0%
17/06/07 10:35:11 INFO mapreduce.Job:  map 91% reduce 0%
17/06/07 10:35:12 INFO mapreduce.Job:  map 92% reduce 0%
17/06/07 10:35:14 INFO mapreduce.Job:  map 93% reduce 0%
17/06/07 10:35:15 INFO mapreduce.Job:  map 94% reduce 0%
17/06/07 10:35:17 INFO mapreduce.Job:  map 95% reduce 0%
17/06/07 10:35:18 INFO mapreduce.Job:  map 96% reduce 0%
17/06/07 10:35:20 INFO mapreduce.Job:  map 98% reduce 0%
17/06/07 10:35:23 INFO mapreduce.Job:  map 99% reduce 0%
17/06/07 10:35:25 INFO mapreduce.Job:  map 100% reduce 0%
17/06/07 10:35:25 INFO mapreduce.Job: Job job_1496824411518_0003 completed successfully
17/06/07 10:35:25 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=488304
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=344
                HDFS: Number of bytes written=10737418200
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=565735
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=565735
                Total vcore-seconds taken by all map tasks=565735
                Total megabyte-seconds taken by all map tasks=579312640
        Map-Reduce Framework
                Map input records=107374182
                Map output records=107374182
                Input split bytes=344
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1050
                CPU time spent (ms)=165790
                Physical memory (bytes) snapshot=1442451456
                Virtual memory (bytes) snapshot=11096707072
                Total committed heap usage (bytes)=1007157248
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=230593859918397906
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=10737418200

real    2m38.135s
user    0m7.127s
sys     0m0.865s
[root@ip-172-31-39-40 ~]# time hadoop jar /opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/lib/hadoop-mapreduce/hadoop-mapreduce-examples-2.6.0-cdh5.8.3.jar teragen -Ddfs.block.size=33554432 -Dmapred.map.tasks=4 107374182 tera_gen10G /user/ainowy/teragen500
teragen <num rows> <output dir>

real    0m1.462s
user    0m2.550s
sys     0m0.382s
</pre>
