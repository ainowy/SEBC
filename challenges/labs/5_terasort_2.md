<b>terasort command </b>

[root@ip-172-31-12-49 ~]# hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort /user/bavaria/tgen512m /user/bavaria/terasort
17/08/08 15:57:30 INFO terasort.TeraSort: starting
17/08/08 15:57:32 INFO hdfs.DFSClient: Created token for bavaria: HDFS_DELEGATION_TOKEN owner=bavaria@AINOWY.UK, renewer=yarn, realUser=, issueDate=1502207852766, maxDate=1502812652766, sequenceNumber=1, masterKeyId=2 on 172.31.12.49:8020
17/08/08 15:57:32 INFO security.TokenCache: Got dt for hdfs://ip-172-31-12-49.eu-west-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.12.49:8020, Ident: (token for bavaria: HDFS_DELEGATION_TOKEN owner=bavaria@AINOWY.UK, renewer=yarn, realUser=, issueDate=1502207852766, maxDate=1502812652766, sequenceNumber=1, masterKeyId=2)
17/08/08 15:57:33 INFO input.FileInputFormat: Total input paths to process : 2
Spent 629ms computing base-splits.
Spent 8ms computing TeraScheduler splits.
Computing input splits took 638ms
Sampling 10 splits of 306
Making 3 from 100000 sampled records
Computing parititions took 1541ms
Spent 2181ms computing partitions.
17/08/08 15:57:34 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-12-49.eu-west-1.compute.internal/172.31.12.49:8032
17/08/08 15:57:35 INFO mapreduce.JobSubmitter: number of splits:306
17/08/08 15:57:35 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1502207750243_0001
17/08/08 15:57:35 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.12.49:8020, Ident: (token for bavaria: HDFS_DELEGATION_TOKEN owner=bavaria@AINOWY.UK, renewer=yarn, realUser=, issueDate=1502207852766, maxDate=1502812652766, sequenceNumber=1, masterKeyId=2)
17/08/08 15:57:36 INFO impl.YarnClientImpl: Submitted application application_1502207750243_0001
17/08/08 15:57:37 INFO mapreduce.Job: The url to track the job: http://ip-172-31-12-49.eu-west-1.compute.internal:8088/proxy/application_1502207750243_0001/
17/08/08 15:57:37 INFO mapreduce.Job: Running job: job_1502207750243_0001
17/08/08 15:57:49 INFO mapreduce.Job: Job job_1502207750243_0001 running in uber mode : false
17/08/08 15:57:49 INFO mapreduce.Job:  map 0% reduce 0%
17/08/08 15:58:02 INFO mapreduce.Job:  map 1% reduce 0%
17/08/08 15:58:15 INFO mapreduce.Job:  map 2% reduce 0%
17/08/08 15:58:23 INFO mapreduce.Job:  map 3% reduce 0%
17/08/08 15:58:37 INFO mapreduce.Job:  map 4% reduce 0%
17/08/08 15:58:45 INFO mapreduce.Job:  map 5% reduce 0%
17/08/08 15:58:58 INFO mapreduce.Job:  map 6% reduce 0%
17/08/08 15:59:05 INFO mapreduce.Job:  map 7% reduce 0%
17/08/08 15:59:18 INFO mapreduce.Job:  map 8% reduce 0%
17/08/08 15:59:32 INFO mapreduce.Job:  map 9% reduce 0%
17/08/08 15:59:40 INFO mapreduce.Job:  map 10% reduce 0%
17/08/08 15:59:54 INFO mapreduce.Job:  map 11% reduce 0%
17/08/08 16:00:02 INFO mapreduce.Job:  map 12% reduce 0%
17/08/08 16:00:15 INFO mapreduce.Job:  map 13% reduce 0%
17/08/08 16:00:22 INFO mapreduce.Job:  map 14% reduce 0%
17/08/08 16:00:36 INFO mapreduce.Job:  map 15% reduce 0%
17/08/08 16:00:44 INFO mapreduce.Job:  map 16% reduce 0%
17/08/08 16:00:57 INFO mapreduce.Job:  map 17% reduce 0%
17/08/08 16:01:05 INFO mapreduce.Job:  map 18% reduce 0%
17/08/08 16:01:18 INFO mapreduce.Job:  map 19% reduce 0%
17/08/08 16:01:25 INFO mapreduce.Job:  map 20% reduce 0%
17/08/08 16:01:38 INFO mapreduce.Job:  map 21% reduce 0%
17/08/08 16:01:47 INFO mapreduce.Job:  map 22% reduce 0%
17/08/08 16:01:59 INFO mapreduce.Job:  map 23% reduce 0%
17/08/08 16:02:07 INFO mapreduce.Job:  map 24% reduce 0%
17/08/08 16:02:20 INFO mapreduce.Job:  map 25% reduce 0%
17/08/08 16:02:34 INFO mapreduce.Job:  map 26% reduce 0%
17/08/08 16:02:44 INFO mapreduce.Job:  map 27% reduce 0%
17/08/08 16:02:56 INFO mapreduce.Job:  map 28% reduce 0%
17/08/08 16:03:04 INFO mapreduce.Job:  map 29% reduce 0%
17/08/08 16:03:17 INFO mapreduce.Job:  map 30% reduce 0%
17/08/08 16:03:25 INFO mapreduce.Job:  map 31% reduce 0%
17/08/08 16:03:37 INFO mapreduce.Job:  map 32% reduce 0%
17/08/08 16:03:46 INFO mapreduce.Job:  map 33% reduce 0%
17/08/08 16:03:59 INFO mapreduce.Job:  map 34% reduce 0%
17/08/08 16:04:08 INFO mapreduce.Job:  map 35% reduce 0%
17/08/08 16:04:20 INFO mapreduce.Job:  map 36% reduce 0%
17/08/08 16:04:29 INFO mapreduce.Job:  map 37% reduce 0%
17/08/08 16:04:41 INFO mapreduce.Job:  map 38% reduce 0%
17/08/08 16:04:51 INFO mapreduce.Job:  map 39% reduce 0%
17/08/08 16:05:02 INFO mapreduce.Job:  map 40% reduce 0%
17/08/08 16:05:13 INFO mapreduce.Job:  map 41% reduce 0%
17/08/08 16:05:23 INFO mapreduce.Job:  map 42% reduce 0%
17/08/08 16:05:37 INFO mapreduce.Job:  map 43% reduce 0%
17/08/08 16:05:47 INFO mapreduce.Job:  map 44% reduce 0%
17/08/08 16:05:59 INFO mapreduce.Job:  map 45% reduce 0%
17/08/08 16:06:08 INFO mapreduce.Job:  map 46% reduce 0%
17/08/08 16:06:20 INFO mapreduce.Job:  map 47% reduce 0%
17/08/08 16:06:28 INFO mapreduce.Job:  map 48% reduce 0%
17/08/08 16:06:40 INFO mapreduce.Job:  map 49% reduce 0%
17/08/08 16:06:48 INFO mapreduce.Job:  map 50% reduce 0%
17/08/08 16:06:58 INFO mapreduce.Job:  map 51% reduce 0%
17/08/08 16:07:08 INFO mapreduce.Job:  map 52% reduce 0%
17/08/08 16:07:18 INFO mapreduce.Job:  map 53% reduce 0%
17/08/08 16:07:30 INFO mapreduce.Job:  map 54% reduce 0%
17/08/08 16:07:39 INFO mapreduce.Job:  map 55% reduce 0%
17/08/08 16:07:48 INFO mapreduce.Job:  map 56% reduce 0%
17/08/08 16:07:59 INFO mapreduce.Job:  map 57% reduce 0%
17/08/08 16:08:07 INFO mapreduce.Job:  map 58% reduce 0%
17/08/08 16:08:20 INFO mapreduce.Job:  map 59% reduce 0%
17/08/08 16:08:31 INFO mapreduce.Job:  map 60% reduce 0%
17/08/08 16:08:42 INFO mapreduce.Job:  map 61% reduce 0%
17/08/08 16:08:49 INFO mapreduce.Job:  map 62% reduce 0%
17/08/08 16:09:02 INFO mapreduce.Job:  map 63% reduce 0%
17/08/08 16:09:09 INFO mapreduce.Job:  map 64% reduce 0%
17/08/08 16:09:20 INFO mapreduce.Job:  map 65% reduce 0%
17/08/08 16:09:30 INFO mapreduce.Job:  map 66% reduce 0%
17/08/08 16:09:40 INFO mapreduce.Job:  map 67% reduce 0%
17/08/08 16:09:51 INFO mapreduce.Job:  map 68% reduce 0%
17/08/08 16:09:59 INFO mapreduce.Job:  map 69% reduce 0%
17/08/08 16:10:12 INFO mapreduce.Job:  map 70% reduce 0%
17/08/08 16:10:19 INFO mapreduce.Job:  map 71% reduce 0%
17/08/08 16:10:31 INFO mapreduce.Job:  map 72% reduce 0%
17/08/08 16:10:41 INFO mapreduce.Job:  map 73% reduce 0%
17/08/08 16:10:49 INFO mapreduce.Job:  map 74% reduce 0%
17/08/08 16:11:01 INFO mapreduce.Job:  map 75% reduce 0%
17/08/08 16:11:14 INFO mapreduce.Job:  map 76% reduce 0%
17/08/08 16:11:25 INFO mapreduce.Job:  map 77% reduce 0%
17/08/08 16:11:33 INFO mapreduce.Job:  map 78% reduce 0%
17/08/08 16:11:45 INFO mapreduce.Job:  map 79% reduce 0%
17/08/08 16:11:56 INFO mapreduce.Job:  map 80% reduce 0%
17/08/08 16:12:03 INFO mapreduce.Job:  map 81% reduce 0%
17/08/08 16:12:13 INFO mapreduce.Job:  map 81% reduce 5%
17/08/08 16:12:16 INFO mapreduce.Job:  map 81% reduce 7%
17/08/08 16:12:19 INFO mapreduce.Job:  map 81% reduce 8%
17/08/08 16:12:22 INFO mapreduce.Job:  map 81% reduce 9%
17/08/08 16:12:26 INFO mapreduce.Job:  map 82% reduce 9%
17/08/08 16:12:49 INFO mapreduce.Job:  map 83% reduce 9%
17/08/08 16:13:10 INFO mapreduce.Job:  map 84% reduce 9%
17/08/08 16:13:30 INFO mapreduce.Job:  map 85% reduce 9%
17/08/08 16:13:49 INFO mapreduce.Job:  map 86% reduce 9%
17/08/08 16:13:50 INFO mapreduce.Job:  map 86% reduce 10%
17/08/08 16:14:09 INFO mapreduce.Job:  map 87% reduce 10%
17/08/08 16:14:28 INFO mapreduce.Job:  map 88% reduce 10%
17/08/08 16:14:48 INFO mapreduce.Job:  map 89% reduce 10%
17/08/08 16:15:07 INFO mapreduce.Job:  map 90% reduce 10%
17/08/08 16:15:27 INFO mapreduce.Job:  map 91% reduce 10%
17/08/08 16:15:47 INFO mapreduce.Job:  map 92% reduce 10%
17/08/08 16:16:12 INFO mapreduce.Job:  map 93% reduce 10%
17/08/08 16:16:30 INFO mapreduce.Job:  map 94% reduce 10%
17/08/08 16:16:50 INFO mapreduce.Job:  map 95% reduce 10%
17/08/08 16:16:53 INFO mapreduce.Job:  map 95% reduce 11%
17/08/08 16:17:10 INFO mapreduce.Job:  map 96% reduce 11%
17/08/08 16:17:30 INFO mapreduce.Job:  map 97% reduce 11%
17/08/08 16:17:50 INFO mapreduce.Job:  map 98% reduce 11%
17/08/08 16:18:10 INFO mapreduce.Job:  map 99% reduce 11%
17/08/08 16:18:30 INFO mapreduce.Job:  map 100% reduce 11%
17/08/08 16:18:42 INFO mapreduce.Job:  map 100% reduce 23%
17/08/08 16:18:45 INFO mapreduce.Job:  map 100% reduce 24%
17/08/08 16:18:48 INFO mapreduce.Job:  map 100% reduce 30%
17/08/08 16:18:51 INFO mapreduce.Job:  map 100% reduce 32%
17/08/08 16:18:54 INFO mapreduce.Job:  map 100% reduce 35%
17/08/08 16:18:57 INFO mapreduce.Job:  map 100% reduce 39%
17/08/08 16:19:00 INFO mapreduce.Job:  map 100% reduce 41%
17/08/08 16:19:03 INFO mapreduce.Job:  map 100% reduce 54%
17/08/08 16:19:06 INFO mapreduce.Job:  map 100% reduce 56%
17/08/08 16:19:09 INFO mapreduce.Job:  map 100% reduce 57%
17/08/08 16:19:12 INFO mapreduce.Job:  map 100% reduce 59%
17/08/08 16:19:15 INFO mapreduce.Job:  map 100% reduce 60%
17/08/08 16:19:18 INFO mapreduce.Job:  map 100% reduce 61%
17/08/08 16:19:19 INFO mapreduce.Job:  map 100% reduce 67%
17/08/08 16:19:21 INFO mapreduce.Job:  map 100% reduce 68%
17/08/08 16:19:22 INFO mapreduce.Job:  map 100% reduce 69%
17/08/08 16:19:24 INFO mapreduce.Job:  map 100% reduce 70%
17/08/08 16:19:25 INFO mapreduce.Job:  map 100% reduce 71%
17/08/08 16:19:27 INFO mapreduce.Job:  map 100% reduce 73%
17/08/08 16:19:28 INFO mapreduce.Job:  map 100% reduce 74%
17/08/08 16:19:30 INFO mapreduce.Job:  map 100% reduce 75%
17/08/08 16:19:31 INFO mapreduce.Job:  map 100% reduce 76%
17/08/08 16:19:32 INFO mapreduce.Job:  map 100% reduce 77%
17/08/08 16:19:34 INFO mapreduce.Job:  map 100% reduce 78%
17/08/08 16:19:37 INFO mapreduce.Job:  map 100% reduce 89%
17/08/08 16:19:40 INFO mapreduce.Job:  map 100% reduce 90%
17/08/08 16:19:43 INFO mapreduce.Job:  map 100% reduce 91%
17/08/08 16:19:46 INFO mapreduce.Job:  map 100% reduce 93%
17/08/08 16:19:49 INFO mapreduce.Job:  map 100% reduce 94%
17/08/08 16:19:52 INFO mapreduce.Job:  map 100% reduce 95%
17/08/08 16:19:55 INFO mapreduce.Job:  map 100% reduce 97%
17/08/08 16:19:58 INFO mapreduce.Job:  map 100% reduce 98%
17/08/08 16:20:01 INFO mapreduce.Job:  map 100% reduce 99%
17/08/08 16:20:03 INFO mapreduce.Job:  map 100% reduce 100%
17/08/08 16:20:04 INFO mapreduce.Job: Job job_1502207750243_0001 completed successfully
17/08/08 16:20:04 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=2288942428
                FILE: Number of bytes written=4564553686
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=5120047124
                HDFS: Number of bytes written=5120000000
                HDFS: Number of read operations=927
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=6
        Job Counters
                Launched map tasks=306
                Launched reduce tasks=3
                Data-local map tasks=304
                Rack-local map tasks=2
                Total time spent by all maps in occupied slots (ms)=1669814
                Total time spent by all reduces in occupied slots (ms)=530702
                Total time spent by all map tasks (ms)=1669814
                Total time spent by all reduce tasks (ms)=530702
                Total vcore-seconds taken by all map tasks=1669814
                Total vcore-seconds taken by all reduce tasks=530702
                Total megabyte-seconds taken by all map tasks=1709889536
                Total megabyte-seconds taken by all reduce tasks=543438848
        Map-Reduce Framework
                Map input records=51200000
                Map output records=51200000
                Map output bytes=5222400000
                Map output materialized bytes=2237702879
                Input split bytes=47124
                Combine input records=0
                Combine output records=0
                Reduce input groups=51200000
                Reduce shuffle bytes=2237702879
                Reduce input records=51200000
                Reduce output records=51200000
                Spilled Records=102400000
                Shuffled Maps =918
                Failed Shuffles=0
                Merged Map outputs=918
                GC time elapsed (ms)=30464
                CPU time spent (ms)=1194180
                Physical memory (bytes) snapshot=139977281536
                Virtual memory (bytes) snapshot=853321383936
                Total committed heap usage (bytes)=137886171136
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=5120000000
        File Output Format Counters
                Bytes Written=5120000000
17/08/08 16:20:04 INFO terasort.TeraSort: done
