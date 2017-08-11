<pre>

<b>Run the terasort program as user nimbus with the output target /user/nimbus/tsort</b>
[root@ip-172-31-21-134 ~]# hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort /user/nimbus/tgen /user/nimbus/tsort 8000000
17/08/11 08:06:59 INFO terasort.TeraSort: starting
17/08/11 08:07:01 INFO hdfs.DFSClient: Created token for nimbus: HDFS_DELEGATION_TOKEN owner=nimbus@AINOWY.PA, renewer=yarn, realUser=, issueDate=1502438821022, maxDate=1503043621022, sequenceNumber=1, masterKeyId=2 on 172.31.21.134:8020
17/08/11 08:07:01 INFO security.TokenCache: Got dt for hdfs://ip-172-31-21-134.eu-west-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.21.134:8020, Ident: (token for nimbus: HDFS_DELEGATION_TOKEN owner=nimbus@AINOWY.PA, renewer=yarn, realUser=, issueDate=1502438821022, maxDate=1503043621022, sequenceNumber=1, masterKeyId=2)
17/08/11 08:07:01 INFO input.FileInputFormat: Total input paths to process : 16
Spent 416ms computing base-splits.
Spent 5ms computing TeraScheduler splits.
Computing input splits took 422ms
Sampling 10 splits of 112
Making 6 from 100000 sampled records
Computing parititions took 902ms
Spent 1326ms computing partitions.
17/08/11 08:07:02 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-21-134.eu-west-1.compute.internal/172.31.21.134:8032
17/08/11 08:07:02 INFO mapreduce.JobSubmitter: number of splits:112
17/08/11 08:07:02 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1502438585943_0001
17/08/11 08:07:02 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.21.134:8020, Ident: (token for nimbus: HDFS_DELEGATION_TOKEN owner=nimbus@AINOWY.PA, renewer=yarn, realUser=, issueDate=1502438821022, maxDate=1503043621022, sequenceNumber=1, masterKeyId=2)
17/08/11 08:07:03 INFO impl.YarnClientImpl: Submitted application application_1502438585943_0001
17/08/11 08:07:03 INFO mapreduce.Job: The url to track the job: http://ip-172-31-21-134.eu-west-1.compute.internal:8088/proxy/application_1502438585943_0001/
17/08/11 08:07:03 INFO mapreduce.Job: Running job: job_1502438585943_0001
17/08/11 08:07:14 INFO mapreduce.Job: Job job_1502438585943_0001 running in uber mode : false
17/08/11 08:07:14 INFO mapreduce.Job:  map 0% reduce 0%
17/08/11 08:07:24 INFO mapreduce.Job:  map 2% reduce 0%
17/08/11 08:07:25 INFO mapreduce.Job:  map 3% reduce 0%
17/08/11 08:07:28 INFO mapreduce.Job:  map 4% reduce 0%
17/08/11 08:07:31 INFO mapreduce.Job:  map 5% reduce 0%
17/08/11 08:07:33 INFO mapreduce.Job:  map 7% reduce 0%
17/08/11 08:07:36 INFO mapreduce.Job:  map 9% reduce 0%
17/08/11 08:07:38 INFO mapreduce.Job:  map 10% reduce 0%
17/08/11 08:07:42 INFO mapreduce.Job:  map 12% reduce 0%
17/08/11 08:07:45 INFO mapreduce.Job:  map 14% reduce 0%
17/08/11 08:07:51 INFO mapreduce.Job:  map 16% reduce 0%
17/08/11 08:07:52 INFO mapreduce.Job:  map 17% reduce 0%
17/08/11 08:07:54 INFO mapreduce.Job:  map 19% reduce 0%
17/08/11 08:07:59 INFO mapreduce.Job:  map 21% reduce 0%
17/08/11 08:08:02 INFO mapreduce.Job:  map 23% reduce 0%
17/08/11 08:08:06 INFO mapreduce.Job:  map 24% reduce 0%
17/08/11 08:08:07 INFO mapreduce.Job:  map 25% reduce 0%
17/08/11 08:08:08 INFO mapreduce.Job:  map 26% reduce 0%
17/08/11 08:08:09 INFO mapreduce.Job:  map 27% reduce 0%
17/08/11 08:08:10 INFO mapreduce.Job:  map 28% reduce 0%
17/08/11 08:08:13 INFO mapreduce.Job:  map 29% reduce 0%
17/08/11 08:08:16 INFO mapreduce.Job:  map 30% reduce 0%
17/08/11 08:08:17 INFO mapreduce.Job:  map 31% reduce 0%
17/08/11 08:08:18 INFO mapreduce.Job:  map 32% reduce 0%
17/08/11 08:08:20 INFO mapreduce.Job:  map 33% reduce 0%
17/08/11 08:08:24 INFO mapreduce.Job:  map 35% reduce 0%
17/08/11 08:08:26 INFO mapreduce.Job:  map 36% reduce 0%
17/08/11 08:08:27 INFO mapreduce.Job:  map 38% reduce 0%
17/08/11 08:08:32 INFO mapreduce.Job:  map 39% reduce 0%
17/08/11 08:08:33 INFO mapreduce.Job:  map 41% reduce 0%
17/08/11 08:08:34 INFO mapreduce.Job:  map 42% reduce 0%
17/08/11 08:08:40 INFO mapreduce.Job:  map 43% reduce 0%
17/08/11 08:08:41 INFO mapreduce.Job:  map 46% reduce 0%
17/08/11 08:08:46 INFO mapreduce.Job:  map 47% reduce 0%
17/08/11 08:08:48 INFO mapreduce.Job:  map 48% reduce 0%
17/08/11 08:08:49 INFO mapreduce.Job:  map 50% reduce 0%
17/08/11 08:08:50 INFO mapreduce.Job:  map 51% reduce 0%
17/08/11 08:08:53 INFO mapreduce.Job:  map 52% reduce 0%
17/08/11 08:08:57 INFO mapreduce.Job:  map 54% reduce 0%
17/08/11 08:08:58 INFO mapreduce.Job:  map 55% reduce 0%
17/08/11 08:08:59 INFO mapreduce.Job:  map 56% reduce 0%
17/08/11 08:09:04 INFO mapreduce.Job:  map 57% reduce 0%
17/08/11 08:09:05 INFO mapreduce.Job:  map 58% reduce 0%
17/08/11 08:09:06 INFO mapreduce.Job:  map 60% reduce 0%
17/08/11 08:09:07 INFO mapreduce.Job:  map 61% reduce 0%
17/08/11 08:09:12 INFO mapreduce.Job:  map 63% reduce 0%
17/08/11 08:09:14 INFO mapreduce.Job:  map 65% reduce 0%
17/08/11 08:09:19 INFO mapreduce.Job:  map 66% reduce 0%
17/08/11 08:09:21 INFO mapreduce.Job:  map 68% reduce 0%
17/08/11 08:09:22 INFO mapreduce.Job:  map 70% reduce 0%
17/08/11 08:09:26 INFO mapreduce.Job:  map 71% reduce 0%
17/08/11 08:09:30 INFO mapreduce.Job:  map 72% reduce 0%
17/08/11 08:09:31 INFO mapreduce.Job:  map 74% reduce 0%
17/08/11 08:09:32 INFO mapreduce.Job:  map 75% reduce 0%
17/08/11 08:09:38 INFO mapreduce.Job:  map 77% reduce 0%
17/08/11 08:09:39 INFO mapreduce.Job:  map 79% reduce 0%
17/08/11 08:09:46 INFO mapreduce.Job:  map 81% reduce 0%
17/08/11 08:09:47 INFO mapreduce.Job:  map 84% reduce 0%
17/08/11 08:09:52 INFO mapreduce.Job:  map 86% reduce 0%
17/08/11 08:09:55 INFO mapreduce.Job:  map 87% reduce 0%
17/08/11 08:09:57 INFO mapreduce.Job:  map 88% reduce 0%
17/08/11 08:09:58 INFO mapreduce.Job:  map 88% reduce 7%
17/08/11 08:10:01 INFO mapreduce.Job:  map 89% reduce 8%
17/08/11 08:10:03 INFO mapreduce.Job:  map 89% reduce 12%
17/08/11 08:10:04 INFO mapreduce.Job:  map 89% reduce 14%
17/08/11 08:10:06 INFO mapreduce.Job:  map 91% reduce 15%
17/08/11 08:10:11 INFO mapreduce.Job:  map 93% reduce 15%
17/08/11 08:10:16 INFO mapreduce.Job:  map 95% reduce 16%
17/08/11 08:10:21 INFO mapreduce.Job:  map 96% reduce 16%
17/08/11 08:10:26 INFO mapreduce.Job:  map 98% reduce 16%
17/08/11 08:10:31 INFO mapreduce.Job:  map 100% reduce 19%
17/08/11 08:10:33 INFO mapreduce.Job:  map 100% reduce 25%
17/08/11 08:10:34 INFO mapreduce.Job:  map 100% reduce 34%
17/08/11 08:10:36 INFO mapreduce.Job:  map 100% reduce 35%
17/08/11 08:10:37 INFO mapreduce.Job:  map 100% reduce 36%
17/08/11 08:10:39 INFO mapreduce.Job:  map 100% reduce 37%
17/08/11 08:10:40 INFO mapreduce.Job:  map 100% reduce 38%
17/08/11 08:10:41 INFO mapreduce.Job:  map 100% reduce 43%
17/08/11 08:10:42 INFO mapreduce.Job:  map 100% reduce 44%
17/08/11 08:10:43 INFO mapreduce.Job:  map 100% reduce 49%
17/08/11 08:10:44 INFO mapreduce.Job:  map 100% reduce 51%
17/08/11 08:10:45 INFO mapreduce.Job:  map 100% reduce 52%
17/08/11 08:10:46 INFO mapreduce.Job:  map 100% reduce 53%
17/08/11 08:10:47 INFO mapreduce.Job:  map 100% reduce 60%
17/08/11 08:10:48 INFO mapreduce.Job:  map 100% reduce 61%
17/08/11 08:10:49 INFO mapreduce.Job:  map 100% reduce 64%
17/08/11 08:10:50 INFO mapreduce.Job:  map 100% reduce 66%
17/08/11 08:10:51 INFO mapreduce.Job:  map 100% reduce 67%
17/08/11 08:10:52 INFO mapreduce.Job:  map 100% reduce 74%
17/08/11 08:10:53 INFO mapreduce.Job:  map 100% reduce 75%
17/08/11 08:10:55 INFO mapreduce.Job:  map 100% reduce 76%
17/08/11 08:10:56 INFO mapreduce.Job:  map 100% reduce 78%
17/08/11 08:10:58 INFO mapreduce.Job:  map 100% reduce 79%
17/08/11 08:10:59 INFO mapreduce.Job:  map 100% reduce 80%
17/08/11 08:11:01 INFO mapreduce.Job:  map 100% reduce 85%
17/08/11 08:11:04 INFO mapreduce.Job:  map 100% reduce 86%
17/08/11 08:11:07 INFO mapreduce.Job:  map 100% reduce 89%
17/08/11 08:11:10 INFO mapreduce.Job:  map 100% reduce 95%
17/08/11 08:11:13 INFO mapreduce.Job:  map 100% reduce 96%
17/08/11 08:11:16 INFO mapreduce.Job:  map 100% reduce 98%
17/08/11 08:11:19 INFO mapreduce.Job:  map 100% reduce 99%
17/08/11 08:11:21 INFO mapreduce.Job:  map 100% reduce 100%
17/08/11 08:11:21 INFO mapreduce.Job: Job job_1502438585943_0001 completed successfully
17/08/11 08:11:21 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=2935798614
                FILE: Number of bytes written=5823661220
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
                Total time spent by all maps in occupied slots (ms)=731306
                Total time spent by all reduces in occupied slots (ms)=276279
                Total time spent by all map tasks (ms)=731306
                Total time spent by all reduce tasks (ms)=276279
                Total vcore-seconds taken by all map tasks=731306
                Total vcore-seconds taken by all reduce tasks=276279
                Total megabyte-seconds taken by all map tasks=748857344
                Total megabyte-seconds taken by all reduce tasks=282909696
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
                GC time elapsed (ms)=16877
                CPU time spent (ms)=742510
                Physical memory (bytes) snapshot=58984652800
                Virtual memory (bytes) snapshot=327079768064
                Total committed heap usage (bytes)=61363716096
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
17/08/11 08:11:21 INFO terasort.TeraSort: done





</pre>
