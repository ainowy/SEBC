<b>Run the terasort program as user saturn with the output target /user/saturn/tsort</b>

<p>

[root@ip-172-31-12-138 ~]# hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort /user/saturn/tgen /user/saturn/tsort 10000000
17/08/07 09:53:56 INFO terasort.TeraSort: starting
17/08/07 09:53:58 INFO hdfs.DFSClient: Created token for saturn: HDFS_DELEGATION_TOKEN owner=saturn@AINOWY.HQ, renewer=yarn, realUser=, issueDate=1502099638359, maxDate=1502704438359, sequenceNumber=5, masterKeyId=4 on 172.31.12.138:8020
17/08/07 09:53:58 INFO security.TokenCache: Got dt for hdfs://ip-172-31-12-138.eu-west-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.12.138:8020, Ident: (token for saturn: HDFS_DELEGATION_TOKEN owner=saturn@AINOWY.HQ, renewer=yarn, realUser=, issueDate=1502099638359, maxDate=1502704438359, sequenceNumber=5, masterKeyId=4)
17/08/07 09:53:58 INFO input.FileInputFormat: Total input paths to process : 12
Spent 555ms computing base-splits.
Spent 7ms computing TeraScheduler splits.
Computing input splits took 563ms
Sampling 10 splits of 204
Making 3 from 100000 sampled records
Computing parititions took 1092ms
Spent 1659ms computing partitions.
17/08/07 09:53:59 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-12-138.eu-west-1.compute.internal/172.31.12.138:8032
17/08/07 09:54:00 INFO mapreduce.JobSubmitter: number of splits:204
17/08/07 09:54:00 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1502098848805_0001
17/08/07 09:54:00 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.12.138:8020, Ident: (token for saturn: HDFS_DELEGATION_TOKEN owner=saturn@AINOWY.HQ, renewer=yarn, realUser=, issueDate=1502099638359, maxDate=1502704438359, sequenceNumber=5, masterKeyId=4)
17/08/07 09:54:02 INFO impl.YarnClientImpl: Submitted application application_1502098848805_0001
17/08/07 09:54:02 INFO mapreduce.Job: The url to track the job: http://ip-172-31-12-138.eu-west-1.compute.internal:8088/proxy/application_1502098848805_0001/
17/08/07 09:54:02 INFO mapreduce.Job: Running job: job_1502098848805_0001
17/08/07 09:54:15 INFO mapreduce.Job: Job job_1502098848805_0001 running in uber mode : false
17/08/07 09:54:15 INFO mapreduce.Job:  map 0% reduce 0%
17/08/07 09:54:28 INFO mapreduce.Job:  map 1% reduce 0%
17/08/07 09:54:35 INFO mapreduce.Job:  map 2% reduce 0%
17/08/07 09:54:43 INFO mapreduce.Job:  map 3% reduce 0%
17/08/07 09:54:49 INFO mapreduce.Job:  map 4% reduce 0%
17/08/07 09:54:57 INFO mapreduce.Job:  map 5% reduce 0%
17/08/07 09:55:04 INFO mapreduce.Job:  map 6% reduce 0%
17/08/07 09:55:11 INFO mapreduce.Job:  map 7% reduce 0%
17/08/07 09:55:18 INFO mapreduce.Job:  map 8% reduce 0%
17/08/07 09:55:25 INFO mapreduce.Job:  map 9% reduce 0%
17/08/07 09:55:32 INFO mapreduce.Job:  map 10% reduce 0%
17/08/07 09:55:38 INFO mapreduce.Job:  map 11% reduce 0%
17/08/07 09:55:46 INFO mapreduce.Job:  map 12% reduce 0%
17/08/07 09:55:53 INFO mapreduce.Job:  map 13% reduce 0%
17/08/07 09:56:00 INFO mapreduce.Job:  map 14% reduce 0%
17/08/07 09:56:06 INFO mapreduce.Job:  map 15% reduce 0%
17/08/07 09:56:14 INFO mapreduce.Job:  map 16% reduce 0%
17/08/07 09:56:20 INFO mapreduce.Job:  map 17% reduce 0%
17/08/07 09:56:28 INFO mapreduce.Job:  map 18% reduce 0%
17/08/07 09:56:35 INFO mapreduce.Job:  map 19% reduce 0%
17/08/07 09:56:42 INFO mapreduce.Job:  map 20% reduce 0%
17/08/07 09:56:49 INFO mapreduce.Job:  map 21% reduce 0%
17/08/07 09:56:57 INFO mapreduce.Job:  map 22% reduce 0%
17/08/07 09:57:04 INFO mapreduce.Job:  map 23% reduce 0%
17/08/07 09:57:11 INFO mapreduce.Job:  map 24% reduce 0%
17/08/07 09:57:17 INFO mapreduce.Job:  map 25% reduce 0%
17/08/07 09:57:29 INFO mapreduce.Job:  map 26% reduce 0%
17/08/07 09:57:36 INFO mapreduce.Job:  map 27% reduce 0%
17/08/07 09:57:43 INFO mapreduce.Job:  map 28% reduce 0%
17/08/07 09:57:50 INFO mapreduce.Job:  map 29% reduce 0%
17/08/07 09:57:57 INFO mapreduce.Job:  map 30% reduce 0%
17/08/07 09:58:04 INFO mapreduce.Job:  map 31% reduce 0%
17/08/07 09:58:11 INFO mapreduce.Job:  map 32% reduce 0%
17/08/07 09:58:18 INFO mapreduce.Job:  map 33% reduce 0%
17/08/07 09:58:25 INFO mapreduce.Job:  map 34% reduce 0%
17/08/07 09:58:32 INFO mapreduce.Job:  map 35% reduce 0%
17/08/07 09:58:39 INFO mapreduce.Job:  map 36% reduce 0%
17/08/07 09:58:46 INFO mapreduce.Job:  map 37% reduce 0%
17/08/07 09:58:53 INFO mapreduce.Job:  map 38% reduce 0%
17/08/07 09:59:00 INFO mapreduce.Job:  map 39% reduce 0%
17/08/07 09:59:07 INFO mapreduce.Job:  map 40% reduce 0%
17/08/07 09:59:14 INFO mapreduce.Job:  map 41% reduce 0%
17/08/07 09:59:21 INFO mapreduce.Job:  map 42% reduce 0%
17/08/07 09:59:28 INFO mapreduce.Job:  map 43% reduce 0%
17/08/07 09:59:35 INFO mapreduce.Job:  map 44% reduce 0%
17/08/07 09:59:42 INFO mapreduce.Job:  map 45% reduce 0%
17/08/07 09:59:49 INFO mapreduce.Job:  map 46% reduce 0%
17/08/07 09:59:56 INFO mapreduce.Job:  map 47% reduce 0%
17/08/07 10:00:03 INFO mapreduce.Job:  map 48% reduce 0%
17/08/07 10:00:10 INFO mapreduce.Job:  map 49% reduce 0%
17/08/07 10:00:17 INFO mapreduce.Job:  map 50% reduce 0%
17/08/07 10:00:28 INFO mapreduce.Job:  map 51% reduce 0%
17/08/07 10:00:35 INFO mapreduce.Job:  map 52% reduce 0%
17/08/07 10:00:42 INFO mapreduce.Job:  map 53% reduce 0%
17/08/07 10:00:49 INFO mapreduce.Job:  map 54% reduce 0%
17/08/07 10:00:56 INFO mapreduce.Job:  map 55% reduce 0%
17/08/07 10:01:03 INFO mapreduce.Job:  map 56% reduce 0%
17/08/07 10:01:10 INFO mapreduce.Job:  map 57% reduce 0%
17/08/07 10:01:17 INFO mapreduce.Job:  map 58% reduce 0%
17/08/07 10:01:24 INFO mapreduce.Job:  map 59% reduce 0%
17/08/07 10:01:31 INFO mapreduce.Job:  map 60% reduce 0%
17/08/07 10:01:38 INFO mapreduce.Job:  map 61% reduce 0%
17/08/07 10:01:45 INFO mapreduce.Job:  map 62% reduce 0%
17/08/07 10:01:52 INFO mapreduce.Job:  map 63% reduce 0%
17/08/07 10:01:59 INFO mapreduce.Job:  map 64% reduce 0%
17/08/07 10:02:06 INFO mapreduce.Job:  map 65% reduce 0%
17/08/07 10:02:13 INFO mapreduce.Job:  map 66% reduce 0%
17/08/07 10:02:20 INFO mapreduce.Job:  map 67% reduce 0%
17/08/07 10:02:28 INFO mapreduce.Job:  map 68% reduce 0%
17/08/07 10:02:35 INFO mapreduce.Job:  map 69% reduce 0%
17/08/07 10:02:43 INFO mapreduce.Job:  map 70% reduce 0%
17/08/07 10:02:49 INFO mapreduce.Job:  map 71% reduce 0%
17/08/07 10:02:56 INFO mapreduce.Job:  map 72% reduce 0%
17/08/07 10:03:03 INFO mapreduce.Job:  map 73% reduce 0%
17/08/07 10:03:11 INFO mapreduce.Job:  map 74% reduce 0%
17/08/07 10:03:18 INFO mapreduce.Job:  map 75% reduce 0%
17/08/07 10:03:25 INFO mapreduce.Job:  map 76% reduce 0%
17/08/07 10:03:32 INFO mapreduce.Job:  map 77% reduce 0%
17/08/07 10:03:39 INFO mapreduce.Job:  map 78% reduce 0%
17/08/07 10:03:46 INFO mapreduce.Job:  map 79% reduce 0%
17/08/07 10:03:53 INFO mapreduce.Job:  map 80% reduce 0%
17/08/07 10:04:00 INFO mapreduce.Job:  map 81% reduce 0%
17/08/07 10:04:07 INFO mapreduce.Job:  map 82% reduce 0%
17/08/07 10:04:17 INFO mapreduce.Job:  map 82% reduce 4%
17/08/07 10:04:20 INFO mapreduce.Job:  map 82% reduce 5%
17/08/07 10:04:22 INFO mapreduce.Job:  map 83% reduce 5%
17/08/07 10:04:23 INFO mapreduce.Job:  map 83% reduce 7%
17/08/07 10:04:26 INFO mapreduce.Job:  map 83% reduce 8%
17/08/07 10:04:29 INFO mapreduce.Job:  map 83% reduce 9%
17/08/07 10:04:36 INFO mapreduce.Job:  map 84% reduce 9%
17/08/07 10:04:50 INFO mapreduce.Job:  map 85% reduce 9%
17/08/07 10:05:04 INFO mapreduce.Job:  map 86% reduce 9%
17/08/07 10:05:05 INFO mapreduce.Job:  map 86% reduce 10%
17/08/07 10:05:18 INFO mapreduce.Job:  map 87% reduce 10%
17/08/07 10:05:32 INFO mapreduce.Job:  map 88% reduce 10%
17/08/07 10:05:46 INFO mapreduce.Job:  map 89% reduce 10%
17/08/07 10:06:00 INFO mapreduce.Job:  map 90% reduce 10%
17/08/07 10:06:14 INFO mapreduce.Job:  map 91% reduce 10%
17/08/07 10:06:28 INFO mapreduce.Job:  map 92% reduce 10%
17/08/07 10:06:42 INFO mapreduce.Job:  map 93% reduce 10%
17/08/07 10:06:55 INFO mapreduce.Job:  map 94% reduce 10%
17/08/07 10:07:07 INFO mapreduce.Job:  map 95% reduce 10%
17/08/07 10:07:08 INFO mapreduce.Job:  map 95% reduce 11%
17/08/07 10:07:21 INFO mapreduce.Job:  map 96% reduce 11%
17/08/07 10:07:34 INFO mapreduce.Job:  map 97% reduce 11%
17/08/07 10:07:46 INFO mapreduce.Job:  map 98% reduce 11%
17/08/07 10:07:58 INFO mapreduce.Job:  map 99% reduce 11%
17/08/07 10:08:12 INFO mapreduce.Job:  map 100% reduce 11%
17/08/07 10:08:22 INFO mapreduce.Job:  map 100% reduce 22%
17/08/07 10:08:25 INFO mapreduce.Job:  map 100% reduce 23%
17/08/07 10:08:28 INFO mapreduce.Job:  map 100% reduce 24%
17/08/07 10:08:29 INFO mapreduce.Job:  map 100% reduce 29%
17/08/07 10:08:31 INFO mapreduce.Job:  map 100% reduce 30%
17/08/07 10:08:32 INFO mapreduce.Job:  map 100% reduce 31%
17/08/07 10:08:34 INFO mapreduce.Job:  map 100% reduce 32%
17/08/07 10:08:35 INFO mapreduce.Job:  map 100% reduce 33%
17/08/07 10:08:37 INFO mapreduce.Job:  map 100% reduce 34%
17/08/07 10:08:38 INFO mapreduce.Job:  map 100% reduce 36%
17/08/07 10:08:40 INFO mapreduce.Job:  map 100% reduce 37%
17/08/07 10:08:41 INFO mapreduce.Job:  map 100% reduce 38%
17/08/07 10:08:43 INFO mapreduce.Job:  map 100% reduce 39%
17/08/07 10:08:44 INFO mapreduce.Job:  map 100% reduce 41%
17/08/07 10:08:46 INFO mapreduce.Job:  map 100% reduce 42%
17/08/07 10:08:47 INFO mapreduce.Job:  map 100% reduce 53%
17/08/07 10:08:49 INFO mapreduce.Job:  map 100% reduce 54%
17/08/07 10:08:50 INFO mapreduce.Job:  map 100% reduce 55%
17/08/07 10:08:52 INFO mapreduce.Job:  map 100% reduce 56%
17/08/07 10:08:53 INFO mapreduce.Job:  map 100% reduce 57%
17/08/07 10:08:56 INFO mapreduce.Job:  map 100% reduce 58%
17/08/07 10:08:59 INFO mapreduce.Job:  map 100% reduce 59%
17/08/07 10:09:02 INFO mapreduce.Job:  map 100% reduce 60%
17/08/07 10:09:04 INFO mapreduce.Job:  map 100% reduce 64%
17/08/07 10:09:05 INFO mapreduce.Job:  map 100% reduce 65%
17/08/07 10:09:07 INFO mapreduce.Job:  map 100% reduce 66%
17/08/07 10:09:08 INFO mapreduce.Job:  map 100% reduce 67%
17/08/07 10:09:10 INFO mapreduce.Job:  map 100% reduce 68%
17/08/07 10:09:12 INFO mapreduce.Job:  map 100% reduce 69%
17/08/07 10:09:13 INFO mapreduce.Job:  map 100% reduce 71%
17/08/07 10:09:16 INFO mapreduce.Job:  map 100% reduce 72%
17/08/07 10:09:18 INFO mapreduce.Job:  map 100% reduce 73%
17/08/07 10:09:19 INFO mapreduce.Job:  map 100% reduce 74%
17/08/07 10:09:21 INFO mapreduce.Job:  map 100% reduce 75%
17/08/07 10:09:22 INFO mapreduce.Job:  map 100% reduce 76%
17/08/07 10:09:24 INFO mapreduce.Job:  map 100% reduce 77%
17/08/07 10:09:25 INFO mapreduce.Job:  map 100% reduce 88%
17/08/07 10:09:26 INFO mapreduce.Job:  map 100% reduce 89%
17/08/07 10:09:29 INFO mapreduce.Job:  map 100% reduce 90%
17/08/07 10:09:32 INFO mapreduce.Job:  map 100% reduce 91%
17/08/07 10:09:35 INFO mapreduce.Job:  map 100% reduce 92%
17/08/07 10:09:38 INFO mapreduce.Job:  map 100% reduce 93%
17/08/07 10:09:41 INFO mapreduce.Job:  map 100% reduce 94%
17/08/07 10:09:44 INFO mapreduce.Job:  map 100% reduce 95%
17/08/07 10:09:47 INFO mapreduce.Job:  map 100% reduce 96%
17/08/07 10:09:50 INFO mapreduce.Job:  map 100% reduce 97%
17/08/07 10:09:53 INFO mapreduce.Job:  map 100% reduce 98%
17/08/07 10:09:56 INFO mapreduce.Job:  map 100% reduce 99%
17/08/07 10:09:58 INFO mapreduce.Job:  map 100% reduce 100%
17/08/07 10:09:59 INFO mapreduce.Job: Job job_1502098848805_0001 completed successfully
17/08/07 10:09:59 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=2941466947
                FILE: Number of bytes written=5834830178
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=6553630600
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=621
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=6
        Job Counters
                Launched map tasks=204
                Launched reduce tasks=3
                Data-local map tasks=202
                Rack-local map tasks=2
                Total time spent by all maps in occupied slots (ms)=1223944
                Total time spent by all reduces in occupied slots (ms)=415375
                Total time spent by all map tasks (ms)=1223944
                Total time spent by all reduce tasks (ms)=415375
                Total vcore-seconds taken by all map tasks=1223944
                Total vcore-seconds taken by all reduce tasks=415375
                Total megabyte-seconds taken by all map tasks=1253318656
                Total megabyte-seconds taken by all reduce tasks=425344000
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Map output bytes=6684672000
                Map output materialized bytes=2867339343
                Input split bytes=30600
                Combine input records=0
                Combine output records=0
                Reduce input groups=65536000
                Reduce shuffle bytes=2867339343
                Reduce input records=65536000
                Reduce output records=65536000
                Spilled Records=131072000
                Shuffled Maps =612
                Failed Shuffles=0
                Merged Map outputs=612
                GC time elapsed (ms)=22842
                CPU time spent (ms)=982190
                Physical memory (bytes) snapshot=98914594816
                Virtual memory (bytes) snapshot=571801874432
                Total committed heap usage (bytes)=93610573824
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
17/08/07 10:09:59 INFO terasort.TeraSort: done


</p>
