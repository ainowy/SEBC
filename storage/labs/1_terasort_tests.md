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
[root@ip-172-31-39-40 ~]# time hadoop jar /opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen 5242880 /user/ainowy/teragen
17/06/07 09:08:26 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-39-40.eu-west-1.compute.internal/172.31.39.40:8032
17/06/07 09:08:27 INFO terasort.TeraSort: Generating 5242880 using 2
17/06/07 09:08:27 INFO mapreduce.JobSubmitter: number of splits:2
17/06/07 09:08:27 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1496824411518_0001
17/06/07 09:08:27 INFO impl.YarnClientImpl: Submitted application application_1496824411518_0001
17/06/07 09:08:27 INFO mapreduce.Job: The url to track the job: http://ip-172-31-39-40.eu-west-1.compute.internal:8088/proxy/application_1496824411518_0001/
17/06/07 09:08:27 INFO mapreduce.Job: Running job: job_1496824411518_0001
17/06/07 09:08:35 INFO mapreduce.Job: Job job_1496824411518_0001 running in uber mode : false
17/06/07 09:08:35 INFO mapreduce.Job:  map 0% reduce 0%
17/06/07 09:08:45 INFO mapreduce.Job:  map 50% reduce 0%
17/06/07 09:08:46 INFO mapreduce.Job:  map 100% reduce 0%
17/06/07 09:08:47 INFO mapreduce.Job: Job job_1496824411518_0001 completed successfully
17/06/07 09:08:47 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=244146
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=167
                HDFS: Number of bytes written=524288000
                HDFS: Number of read operations=8
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=4
        Job Counters
                Launched map tasks=2
                Other local map tasks=2
                Total time spent by all maps in occupied slots (ms)=16769
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=16769
                Total vcore-seconds taken by all map tasks=16769
                Total megabyte-seconds taken by all map tasks=17171456
        Map-Reduce Framework
                Map input records=5242880
                Map output records=5242880
                Input split bytes=167
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=179
                CPU time spent (ms)=17040
                Physical memory (bytes) snapshot=719949824
                Virtual memory (bytes) snapshot=5568372736
                Total committed heap usage (bytes)=689963008
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=11257830824958050
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=524288000

real    0m23.374s
user    0m6.557s
sys     0m0.722s

</pre>
