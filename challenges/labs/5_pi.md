<h1>Challenge 5 - Kerberize the cluster</h1>

<p>

<b>As user saturn, use teragen to generate a 65,536,000-record dataset</b>

[root@ip-172-31-12-138 ~]# kinit haley
Password for haley@AINOWY.HQ:
[root@ip-172-31-12-138 ~]# hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar pi 4 10
Number of Maps  = 4
Samples per Map = 10
Wrote input for Map #0
Wrote input for Map #1
Wrote input for Map #2
Wrote input for Map #3
Starting Job
17/08/07 09:19:47 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-12-138.eu-west-1.compute.internal/172.31.12.138:8032
17/08/07 09:19:47 INFO hdfs.DFSClient: Created token for haley: HDFS_DELEGATION_TOKEN owner=haley@AINOWY.HQ, renewer=yarn, realUser=, issueDate=1502097587396, maxDate=1502702387396, sequenceNumber=4, masterKeyId=2 on 172.31.12.138:8020
17/08/07 09:19:47 INFO security.TokenCache: Got dt for hdfs://ip-172-31-12-138.eu-west-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.12.138:8020, Ident: (token for haley: HDFS_DELEGATION_TOKEN owner=haley@AINOWY.HQ, renewer=yarn, realUser=, issueDate=1502097587396, maxDate=1502702387396, sequenceNumber=4, masterKeyId=2)
17/08/07 09:19:47 INFO input.FileInputFormat: Total input paths to process : 4
17/08/07 09:19:47 INFO mapreduce.JobSubmitter: number of splits:4
17/08/07 09:19:47 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1502095435378_0002
17/08/07 09:19:47 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.12.138:8020, Ident: (token for haley: HDFS_DELEGATION_TOKEN owner=haley@AINOWY.HQ, renewer=yarn, realUser=, issueDate=1502097587396, maxDate=1502702387396, sequenceNumber=4, masterKeyId=2)
17/08/07 09:19:48 INFO impl.YarnClientImpl: Submitted application application_1502095435378_0002
17/08/07 09:19:48 INFO mapreduce.Job: The url to track the job: http://ip-172-31-12-138.eu-west-1.compute.internal:8088/proxy/application_1502095435378_0002/
17/08/07 09:19:48 INFO mapreduce.Job: Running job: job_1502095435378_0002
17/08/07 09:19:59 INFO mapreduce.Job: Job job_1502095435378_0002 running in uber mode : false
17/08/07 09:19:59 INFO mapreduce.Job:  map 0% reduce 0%
17/08/07 09:20:09 INFO mapreduce.Job:  map 50% reduce 0%
17/08/07 09:20:14 INFO mapreduce.Job:  map 100% reduce 0%
17/08/07 09:20:21 INFO mapreduce.Job:  map 100% reduce 100%
17/08/07 09:20:22 INFO mapreduce.Job: Job job_1502095435378_0002 completed successfully
17/08/07 09:20:22 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=65
                FILE: Number of bytes written=624985
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=1196
                HDFS: Number of bytes written=215
                HDFS: Number of read operations=19
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=3
        Job Counters
                Launched map tasks=4
                Launched reduce tasks=1
                Data-local map tasks=4
                Total time spent by all maps in occupied slots (ms)=22485
                Total time spent by all reduces in occupied slots (ms)=4032
                Total time spent by all map tasks (ms)=22485
                Total time spent by all reduce tasks (ms)=4032
                Total vcore-seconds taken by all map tasks=22485
                Total vcore-seconds taken by all reduce tasks=4032
                Total megabyte-seconds taken by all map tasks=23024640
                Total megabyte-seconds taken by all reduce tasks=4128768
        Map-Reduce Framework
                Map input records=4
                Map output records=8
                Map output bytes=72
                Map output materialized bytes=135
                Input split bytes=724
                Combine input records=0
                Combine output records=0
                Reduce input groups=2
                Reduce shuffle bytes=135
                Reduce input records=8
                Reduce output records=0
                Spilled Records=16
                Shuffled Maps =4
                Failed Shuffles=0
                Merged Map outputs=4
                GC time elapsed (ms)=454
                CPU time spent (ms)=4080
                Physical memory (bytes) snapshot=1857183744
                Virtual memory (bytes) snapshot=13811470336
                Total committed heap usage (bytes)=1780482048
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=472
        File Output Format Counters
                Bytes Written=97
Job Finished in 35.497 seconds
Estimated value of Pi is 3.40000000000000000000


</p>
