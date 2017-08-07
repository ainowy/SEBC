<b>As user saturn, use teragen to generate a 65,536,000-record dataset</b>

<p>
[root@ip-172-31-12-138 ~]# time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -D dfs.block.size=33554432 -D mapred.map.tasks=12 -D mapreduce.map.java.opts.max.heap=512M 65536000 /user/saturn/tgen2
17/08/07 10:26:25 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-12-138.eu-west-1.compute.internal/172.31.12.138:8032
17/08/07 10:26:25 INFO hdfs.DFSClient: Created token for saturn: HDFS_DELEGATION_TOKEN owner=saturn@AINOWY.HQ, renewer=yarn, realUser=, issueDate=1502101585795, maxDate=1502706385795, sequenceNumber=6, masterKeyId=4 on 172.31.12.138:8020
17/08/07 10:26:25 INFO security.TokenCache: Got dt for hdfs://ip-172-31-12-138.eu-west-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.12.138:8020, Ident: (token for saturn: HDFS_DELEGATION_TOKEN owner=saturn@AINOWY.HQ, renewer=yarn, realUser=, issueDate=1502101585795, maxDate=1502706385795, sequenceNumber=6, masterKeyId=4)
17/08/07 10:26:26 INFO terasort.TeraSort: Generating 65536000 using 12
17/08/07 10:26:26 INFO mapreduce.JobSubmitter: number of splits:12
17/08/07 10:26:26 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/08/07 10:26:26 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/08/07 10:26:26 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1502098848805_0002
17/08/07 10:26:26 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.12.138:8020, Ident: (token for saturn: HDFS_DELEGATION_TOKEN owner=saturn@AINOWY.HQ, renewer=yarn, realUser=, issueDate=1502101585795, maxDate=1502706385795, sequenceNumber=6, masterKeyId=4)
17/08/07 10:26:27 INFO impl.YarnClientImpl: Submitted application application_1502098848805_0002
17/08/07 10:26:27 INFO mapreduce.Job: The url to track the job: http://ip-172-31-12-138.eu-west-1.compute.internal:8088/proxy/application_1502098848805_0002/
17/08/07 10:26:27 INFO mapreduce.Job: Running job: job_1502098848805_0002
17/08/07 10:26:38 INFO mapreduce.Job: Job job_1502098848805_0002 running in uber mode : false
17/08/07 10:26:38 INFO mapreduce.Job:  map 0% reduce 0%
17/08/07 10:26:53 INFO mapreduce.Job:  map 7% reduce 0%
17/08/07 10:26:56 INFO mapreduce.Job:  map 10% reduce 0%
17/08/07 10:26:59 INFO mapreduce.Job:  map 13% reduce 0%
17/08/07 10:27:02 INFO mapreduce.Job:  map 14% reduce 0%
17/08/07 10:27:05 INFO mapreduce.Job:  map 16% reduce 0%
17/08/07 10:27:06 INFO mapreduce.Job:  map 17% reduce 0%
17/08/07 10:27:16 INFO mapreduce.Job:  map 22% reduce 0%
17/08/07 10:27:19 INFO mapreduce.Job:  map 25% reduce 0%
17/08/07 10:27:22 INFO mapreduce.Job:  map 26% reduce 0%
17/08/07 10:27:25 INFO mapreduce.Job:  map 28% reduce 0%
17/08/07 10:27:28 INFO mapreduce.Job:  map 30% reduce 0%
17/08/07 10:27:31 INFO mapreduce.Job:  map 32% reduce 0%
17/08/07 10:27:33 INFO mapreduce.Job:  map 33% reduce 0%
17/08/07 10:27:44 INFO mapreduce.Job:  map 38% reduce 0%
17/08/07 10:27:47 INFO mapreduce.Job:  map 40% reduce 0%
17/08/07 10:27:50 INFO mapreduce.Job:  map 42% reduce 0%
17/08/07 10:27:53 INFO mapreduce.Job:  map 44% reduce 0%
17/08/07 10:27:56 INFO mapreduce.Job:  map 46% reduce 0%
17/08/07 10:27:59 INFO mapreduce.Job:  map 48% reduce 0%
17/08/07 10:28:01 INFO mapreduce.Job:  map 50% reduce 0%
17/08/07 10:28:12 INFO mapreduce.Job:  map 53% reduce 0%
17/08/07 10:28:13 INFO mapreduce.Job:  map 55% reduce 0%
17/08/07 10:28:15 INFO mapreduce.Job:  map 57% reduce 0%
17/08/07 10:28:16 INFO mapreduce.Job:  map 58% reduce 0%
17/08/07 10:28:18 INFO mapreduce.Job:  map 59% reduce 0%
17/08/07 10:28:19 INFO mapreduce.Job:  map 60% reduce 0%
17/08/07 10:28:21 INFO mapreduce.Job:  map 61% reduce 0%
17/08/07 10:28:22 INFO mapreduce.Job:  map 62% reduce 0%
17/08/07 10:28:24 INFO mapreduce.Job:  map 63% reduce 0%
17/08/07 10:28:25 INFO mapreduce.Job:  map 64% reduce 0%
17/08/07 10:28:28 INFO mapreduce.Job:  map 66% reduce 0%
17/08/07 10:28:30 INFO mapreduce.Job:  map 67% reduce 0%
17/08/07 10:28:38 INFO mapreduce.Job:  map 70% reduce 0%
17/08/07 10:28:40 INFO mapreduce.Job:  map 72% reduce 0%
17/08/07 10:28:41 INFO mapreduce.Job:  map 73% reduce 0%
17/08/07 10:28:43 INFO mapreduce.Job:  map 74% reduce 0%
17/08/07 10:28:44 INFO mapreduce.Job:  map 75% reduce 0%
17/08/07 10:28:46 INFO mapreduce.Job:  map 76% reduce 0%
17/08/07 10:28:47 INFO mapreduce.Job:  map 77% reduce 0%
17/08/07 10:28:49 INFO mapreduce.Job:  map 78% reduce 0%
17/08/07 10:28:50 INFO mapreduce.Job:  map 79% reduce 0%
17/08/07 10:28:52 INFO mapreduce.Job:  map 80% reduce 0%
17/08/07 10:28:53 INFO mapreduce.Job:  map 81% reduce 0%
17/08/07 10:28:55 INFO mapreduce.Job:  map 82% reduce 0%
17/08/07 10:28:57 INFO mapreduce.Job:  map 83% reduce 0%
17/08/07 10:29:05 INFO mapreduce.Job:  map 86% reduce 0%
17/08/07 10:29:08 INFO mapreduce.Job:  map 89% reduce 0%
17/08/07 10:29:11 INFO mapreduce.Job:  map 91% reduce 0%
17/08/07 10:29:14 INFO mapreduce.Job:  map 93% reduce 0%
17/08/07 10:29:17 INFO mapreduce.Job:  map 95% reduce 0%
17/08/07 10:29:20 INFO mapreduce.Job:  map 97% reduce 0%
17/08/07 10:29:23 INFO mapreduce.Job:  map 99% reduce 0%
17/08/07 10:29:25 INFO mapreduce.Job:  map 100% reduce 0%
17/08/07 10:29:26 INFO mapreduce.Job: Job job_1502098848805_0002 completed successfully
17/08/07 10:29:26 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=1493114
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=1025
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=48
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=24
        Job Counters
                Launched map tasks=12
                Other local map tasks=12
                Total time spent by all maps in occupied slots (ms)=317324
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=317324
                Total vcore-seconds taken by all map tasks=317324
                Total megabyte-seconds taken by all map tasks=324939776
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Input split bytes=1025
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1909
                CPU time spent (ms)=153860
                Physical memory (bytes) snapshot=4625690624
                Virtual memory (bytes) snapshot=33268568064
                Total committed heap usage (bytes)=3938451456
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=140750829423462787
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=6553600000

real    3m5.238s
user    0m8.177s
sys     0m0.927s

</p>
<b>The command and output of hdfs dfs -ls /user/saturn/tgen</b>

<p>
[root@ip-172-31-12-138 ~]# hdfs dfs -ls /user/saturn/tgen
Found 13 items
-rw-r--r--   3 saturn supergroup          0 2017-08-07 08:18 /user/saturn/tgen/_SUCCESS
-rw-r--r--   3 saturn supergroup  546133400 2017-08-07 08:16 /user/saturn/tgen/part-m-0000  0
-rw-r--r--   3 saturn supergroup  546133300 2017-08-07 08:16 /user/saturn/tgen/part-m-0000  1
-rw-r--r--   3 saturn supergroup  546133300 2017-08-07 08:16 /user/saturn/tgen/part-m-0000  2
-rw-r--r--   3 saturn supergroup  546133400 2017-08-07 08:16 /user/saturn/tgen/part-m-0000  3
-rw-r--r--   3 saturn supergroup  546133300 2017-08-07 08:17 /user/saturn/tgen/part-m-0000  4
-rw-r--r--   3 saturn supergroup  546133300 2017-08-07 08:17 /user/saturn/tgen/part-m-0000  5
-rw-r--r--   3 saturn supergroup  546133400 2017-08-07 08:17 /user/saturn/tgen/part-m-0000  6
-rw-r--r--   3 saturn supergroup  546133300 2017-08-07 08:17 /user/saturn/tgen/part-m-0000  7
-rw-r--r--   3 saturn supergroup  546133300 2017-08-07 08:18 /user/saturn/tgen/part-m-0000  8
-rw-r--r--   3 saturn supergroup  546133400 2017-08-07 08:18 /user/saturn/tgen/part-m-0000  9
-rw-r--r--   3 saturn supergroup  546133300 2017-08-07 08:18 /user/saturn/tgen/part-m-0001  0
-rw-r--r--   3 saturn supergroup  546133300 2017-08-07 08:18 /user/saturn/tgen/part-m-0001  1

</p>

<b>The command and output of hadoop fsck -blocks /user/saturn</b>

<p>
[root@ip-172-31-12-138 ~]# hdfs fsck -blocks /user/saturn
Connecting to namenode via http://ip-172-31-12-138.eu-west-1.compute.internal:50070
FSCK started by saturn (auth:KERBEROS_SSL) from /172.31.12.138 for path /user/saturn at Mon Aug 07 10:22:43 UTC 2017
...............
/user/saturn/tsort/_partition.lst:  Under replicated BP-1012525451-172.31.12.138-1502091442894:blk_1073743648_2824. Target Replicas is 10 but found 3 replica(s).
...Status: HEALTHY
 Total size:    13107200022 B
 Total dirs:    4
 Total files:   18
 Total symlinks:                0
 Total blocks (validated):      256 (avg. block size 51200000 B)
 Minimally replicated blocks:   256 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       1 (0.390625 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     2.6015625
 Corrupt blocks:                0
 Missing replicas:              7 (1.0401188 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Mon Aug 07 10:22:43 UTC 2017 in 6 milliseconds

The filesystem under path '/user/saturn' is HEALTHY

</p>
