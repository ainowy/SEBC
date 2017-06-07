

<pre>
<b>Create a precious directory in HDFS; copy the ZIP course file into it.</b>
[root@ip-172-31-39-40 ~]# hdfs dfs -mkdir /user/ainowy/precious

<b>Enable snapshots</b>

I enabled snapshots through Cloudera Manager. The path to do so is: HDFS service > File Browser > search file path: /user/ainowy/precious > enable snapshot > take snapshot

<b>Create a snapshot called sebc-hdfs-test</b>

When you press "take snapshot" CM asks the name for the snapshot. Here we type "sebc-hdfs-test"

<b>Delete the directory</b>

hdfs dfs -rm -R /user/ainowy/precious

As we have done snapshots, we are not allowed:

[root@ip-172-31-39-40 ~]# hdfs dfs -rm -R /user/ainowy/precious
rm: Failed to move to trash: hdfs://ip-172-31-39-40.eu-west-1.compute.internal:8020/user/ainowy/precious: The directory /user/ainowy/precious cannot be deleted since /user/ainowy/precious is snapshottable and already has snapshots

<b>Delete the zip file</b>

[root@ip-172-31-39-40 ~]# hdfs dfs -rm -R /user/ainowy/precious/SEBC-master.zip
17/06/07 09:48:35 INFO fs.TrashPolicyDefault: Moved: 'hdfs://ip-172-31-39-40.eu-west-1.compute.internal:8020/user/ainowy/precious/SEBC-master.zip' to trash at: hdfs://ip-172-31-39-40.eu-west-1.compute.internal:8020/user/hdfs/.Trash/Current/user/ainowy/precious/SEBC-master.zip

<b>Restore deleted snapshot</b>

HDFS Service > File Browser > look for path to file > click the down arrow > restore directory from snapshot

</pre>
