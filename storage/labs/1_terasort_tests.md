<h1><b> Terasort </b></h1>
<pre>
[root@ip-172-31-39-40 ~]# time hadoop jar /opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort /user/ainowy/teragen /user/ainowy/terasort
17/06/07 09:16:03 INFO terasort.TeraSort: starting
17/06/07 09:16:04 INFO input.FileInputFormat: Total input paths to process : 2
Spent 145ms computing base-splits.
Spent 2ms computing TeraScheduler splits.
Computing input splits took 148ms
Sampling 4 splits of 4
Making 6 from 100000 sampled records
Computing parititions took 592ms
Spent 742ms computing partitions.
17/06/07 09:16:05 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-39-40.eu-west-1.compute.internal/172.31.39.40:8032
17/06/07 09:16:05 INFO mapreduce.JobSubmitter: number of splits:4
17/06/07 09:16:05 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1496824411518_0002
17/06/07 09:16:05 INFO impl.YarnClientImpl: Submitted application application_1496824411518_0002
17/06/07 09:16:06 INFO mapreduce.Job: The url to track the job: http://ip-172-31-39-40.eu-west-1.compute.internal:8088/proxy/application_1496824411518_0002/
17/06/07 09:16:06 INFO mapreduce.Job: Running job: job_1496824411518_0002
17/06/07 09:16:12 INFO mapreduce.Job: Job job_1496824411518_0002 running in uber mode : false
17/06/07 09:16:12 INFO mapreduce.Job:  map 0% reduce 0%
17/06/07 09:16:24 INFO mapreduce.Job:  map 42% reduce 0%
17/06/07 09:16:25 INFO mapreduce.Job:  map 50% reduce 0%
17/06/07 09:16:26 INFO mapreduce.Job:  map 100% reduce 0%
17/06/07 09:16:36 INFO mapreduce.Job:  map 100% reduce 67%
17/06/07 09:16:37 INFO mapreduce.Job:  map 100% reduce 100%
17/06/07 09:16:37 INFO mapreduce.Job: Job job_1496824411518_0002 completed successfully
17/06/07 09:16:37 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=232238034
                FILE: Number of bytes written=464140716
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=524288608
                HDFS: Number of bytes written=524288000
                HDFS: Number of read operations=30
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=12
        Job Counters
                Launched map tasks=4
                Launched reduce tasks=6
                Data-local map tasks=4
                Total time spent by all maps in occupied slots (ms)=43529
                Total time spent by all reduces in occupied slots (ms)=49683
                Total time spent by all map tasks (ms)=43529
                Total time spent by all reduce tasks (ms)=49683
                Total vcore-seconds taken by all map tasks=43529
                Total vcore-seconds taken by all reduce tasks=49683
                Total megabyte-seconds taken by all map tasks=44573696
                Total megabyte-seconds taken by all reduce tasks=50875392
        Map-Reduce Framework
                Map input records=5242880
                Map output records=5242880
                Map output bytes=534773760
                Map output materialized bytes=230667852
                Input split bytes=608
                Combine input records=0
                Combine output records=0
                Reduce input groups=5242880
                Reduce shuffle bytes=230667852
                Reduce input records=5242880
                Reduce output records=5242880
                Spilled Records=10485760
                Shuffled Maps =24
                Failed Shuffles=0
                Merged Map outputs=24
                GC time elapsed (ms)=1989
                CPU time spent (ms)=64540
                Physical memory (bytes) snapshot=3881611264
                Virtual memory (bytes) snapshot=27799613440
                Total committed heap usage (bytes)=4339531776
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=524288000
        File Output Format Counters
                Bytes Written=524288000
17/06/07 09:16:37 INFO terasort.TeraSort: done

real    0m35.614s
user    0m7.945s
sys     0m0.812s
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
