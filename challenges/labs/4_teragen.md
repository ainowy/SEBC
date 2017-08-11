<pre>

<b>The full teragen command and output</b>

[nimbus@ip-172-31-21-134 ~]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -D dfs.block.size=67108864 -D mapred.map.tasks=16 -D mapreduce.map.java.opts.max.heap=768M 65536000 /user/nimbus/tgen
17/08/11 07:50:04 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-21-134.eu-west-1.compute.internal/172.31.21.134:8032
17/08/11 07:50:05 INFO terasort.TeraSort: Generating 65536000 using 16
17/08/11 07:50:05 INFO mapreduce.JobSubmitter: number of splits:16
17/08/11 07:50:05 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/08/11 07:50:05 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/08/11 07:50:05 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1502437305455_0001
17/08/11 07:50:06 INFO impl.YarnClientImpl: Submitted application application_1502437305455_0001
17/08/11 07:50:06 INFO mapreduce.Job: The url to track the job: http://ip-172-31-21-134.eu-west-1.compute.internal:8088/proxy/application_1502437305455_0001/
17/08/11 07:50:06 INFO mapreduce.Job: Running job: job_1502437305455_0001
17/08/11 07:50:13 INFO mapreduce.Job: Job job_1502437305455_0001 running in uber mode : false
17/08/11 07:50:13 INFO mapreduce.Job:  map 0% reduce 0%
17/08/11 07:50:26 INFO mapreduce.Job:  map 4% reduce 0%
17/08/11 07:50:27 INFO mapreduce.Job:  map 7% reduce 0%
17/08/11 07:50:28 INFO mapreduce.Job:  map 13% reduce 0%
17/08/11 07:50:29 INFO mapreduce.Job:  map 14% reduce 0%
17/08/11 07:50:30 INFO mapreduce.Job:  map 15% reduce 0%
17/08/11 07:50:31 INFO mapreduce.Job:  map 19% reduce 0%
17/08/11 07:50:32 INFO mapreduce.Job:  map 20% reduce 0%
17/08/11 07:50:33 INFO mapreduce.Job:  map 21% reduce 0%
17/08/11 07:50:34 INFO mapreduce.Job:  map 23% reduce 0%
17/08/11 07:50:36 INFO mapreduce.Job:  map 24% reduce 0%
17/08/11 07:50:37 INFO mapreduce.Job:  map 27% reduce 0%
17/08/11 07:50:40 INFO mapreduce.Job:  map 30% reduce 0%
17/08/11 07:50:43 INFO mapreduce.Job:  map 31% reduce 0%
17/08/11 07:50:46 INFO mapreduce.Job:  map 33% reduce 0%
17/08/11 07:50:48 INFO mapreduce.Job:  map 36% reduce 0%
17/08/11 07:50:49 INFO mapreduce.Job:  map 37% reduce 0%
17/08/11 07:50:51 INFO mapreduce.Job:  map 39% reduce 0%
17/08/11 07:50:52 INFO mapreduce.Job:  map 40% reduce 0%
17/08/11 07:50:55 INFO mapreduce.Job:  map 41% reduce 0%
17/08/11 07:50:56 INFO mapreduce.Job:  map 44% reduce 0%
17/08/11 07:50:57 INFO mapreduce.Job:  map 46% reduce 0%
17/08/11 07:50:58 INFO mapreduce.Job:  map 49% reduce 0%
17/08/11 07:51:00 INFO mapreduce.Job:  map 50% reduce 0%
17/08/11 07:51:01 INFO mapreduce.Job:  map 51% reduce 0%
17/08/11 07:51:02 INFO mapreduce.Job:  map 52% reduce 0%
17/08/11 07:51:03 INFO mapreduce.Job:  map 53% reduce 0%
17/08/11 07:51:04 INFO mapreduce.Job:  map 54% reduce 0%
17/08/11 07:51:05 INFO mapreduce.Job:  map 55% reduce 0%
17/08/11 07:51:06 INFO mapreduce.Job:  map 56% reduce 0%
17/08/11 07:51:08 INFO mapreduce.Job:  map 57% reduce 0%
17/08/11 07:51:09 INFO mapreduce.Job:  map 58% reduce 0%
17/08/11 07:51:10 INFO mapreduce.Job:  map 60% reduce 0%
17/08/11 07:51:11 INFO mapreduce.Job:  map 61% reduce 0%
17/08/11 07:51:12 INFO mapreduce.Job:  map 63% reduce 0%
17/08/11 07:51:14 INFO mapreduce.Job:  map 65% reduce 0%
17/08/11 07:51:15 INFO mapreduce.Job:  map 66% reduce 0%
17/08/11 07:51:16 INFO mapreduce.Job:  map 67% reduce 0%
17/08/11 07:51:18 INFO mapreduce.Job:  map 70% reduce 0%
17/08/11 07:51:21 INFO mapreduce.Job:  map 73% reduce 0%
17/08/11 07:51:24 INFO mapreduce.Job:  map 75% reduce 0%
17/08/11 07:51:29 INFO mapreduce.Job:  map 78% reduce 0%
17/08/11 07:51:30 INFO mapreduce.Job:  map 80% reduce 0%
17/08/11 07:51:32 INFO mapreduce.Job:  map 82% reduce 0%
17/08/11 07:51:33 INFO mapreduce.Job:  map 85% reduce 0%
17/08/11 07:51:35 INFO mapreduce.Job:  map 87% reduce 0%
17/08/11 07:51:36 INFO mapreduce.Job:  map 89% reduce 0%
17/08/11 07:51:38 INFO mapreduce.Job:  map 91% reduce 0%
17/08/11 07:51:39 INFO mapreduce.Job:  map 93% reduce 0%
17/08/11 07:51:41 INFO mapreduce.Job:  map 94% reduce 0%
17/08/11 07:51:42 INFO mapreduce.Job:  map 95% reduce 0%
17/08/11 07:51:43 INFO mapreduce.Job:  map 96% reduce 0%
17/08/11 07:51:44 INFO mapreduce.Job:  map 98% reduce 0%
17/08/11 07:51:45 INFO mapreduce.Job:  map 99% reduce 0%
17/08/11 07:51:46 INFO mapreduce.Job:  map 100% reduce 0%
17/08/11 07:51:47 INFO mapreduce.Job: Job job_1502437305455_0001 completed successfully
17/08/11 07:51:47 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=1978934
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=1368
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=64
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=32
        Job Counters
                Launched map tasks=16
                Other local map tasks=16
                Total time spent by all maps in occupied slots (ms)=416044
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=416044
                Total vcore-seconds taken by all map tasks=416044
                Total megabyte-seconds taken by all map tasks=426029056
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Input split bytes=1368
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=2923
                CPU time spent (ms)=163450
                Physical memory (bytes) snapshot=6014222336
                Virtual memory (bytes) snapshot=44406333440
                Total committed heap usage (bytes)=5750915072
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=140750829423462787
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=6553600000

real    1m45.479s
user    0m6.892s
sys     0m0.865s

<b>The time command </b>

real    1m45.479s
user    0m6.892s
sys     0m0.865s


<b>The command and output of hdfs dfs -ls /user/nimbus/tgen</b>

[nimbus@ip-172-31-21-134 ~]$ hdfs dfs -ls /user/nimbus/tgen
Found 17 items
-rw-r--r--   3 nimbus supergroup          0 2017-08-11 07:51 /user/nimbus/tgen/_SUCCESS
-rw-r--r--   3 nimbus supergroup  409600000 2017-08-11 07:50 /user/nimbus/tgen/part-m-00000
-rw-r--r--   3 nimbus supergroup  409600000 2017-08-11 07:50 /user/nimbus/tgen/part-m-00001
-rw-r--r--   3 nimbus supergroup  409600000 2017-08-11 07:50 /user/nimbus/tgen/part-m-00002
-rw-r--r--   3 nimbus supergroup  409600000 2017-08-11 07:50 /user/nimbus/tgen/part-m-00003
-rw-r--r--   3 nimbus supergroup  409600000 2017-08-11 07:50 /user/nimbus/tgen/part-m-00004
-rw-r--r--   3 nimbus supergroup  409600000 2017-08-11 07:50 /user/nimbus/tgen/part-m-00005
-rw-r--r--   3 nimbus supergroup  409600000 2017-08-11 07:50 /user/nimbus/tgen/part-m-00006
-rw-r--r--   3 nimbus supergroup  409600000 2017-08-11 07:51 /user/nimbus/tgen/part-m-00007
-rw-r--r--   3 nimbus supergroup  409600000 2017-08-11 07:51 /user/nimbus/tgen/part-m-00008
-rw-r--r--   3 nimbus supergroup  409600000 2017-08-11 07:51 /user/nimbus/tgen/part-m-00009
-rw-r--r--   3 nimbus supergroup  409600000 2017-08-11 07:51 /user/nimbus/tgen/part-m-00010
-rw-r--r--   3 nimbus supergroup  409600000 2017-08-11 07:51 /user/nimbus/tgen/part-m-00011
-rw-r--r--   3 nimbus supergroup  409600000 2017-08-11 07:51 /user/nimbus/tgen/part-m-00012
-rw-r--r--   3 nimbus supergroup  409600000 2017-08-11 07:51 /user/nimbus/tgen/part-m-00013
-rw-r--r--   3 nimbus supergroup  409600000 2017-08-11 07:51 /user/nimbus/tgen/part-m-00014
-rw-r--r--   3 nimbus supergroup  409600000 2017-08-11 07:51 /user/nimbus/tgen/part-m-00015


<b>The command and output of hadoop fsck -blocks /user/nimbus</b>


[nimbus@ip-172-31-21-134 ~]$ hadoop fsck -blocks /user/nimbus
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.

Connecting to namenode via http://ip-172-31-21-134.eu-west-1.compute.internal:50070
FSCK started by nimbus (auth:SIMPLE) from /172.31.21.134 for path /user/nimbus at Fri Aug 11 07:53:37 UTC 2017
.................Status: HEALTHY
 Total size:    6553600000 B
 Total dirs:    3
 Total files:   17
 Total symlinks:                0
 Total blocks (validated):      112 (avg. block size 58514285 B)
 Minimally replicated blocks:   112 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Fri Aug 11 07:53:37 UTC 2017 in 5 milliseconds


The filesystem under path '/user/nimbus' is HEALTHY


</pre>
