<h1>Challenge 1: Install a MySQL server</h1>

<p>

<b>Command and output that shows the hostname of your database server </b>



<b>A command and output that reports the database server version</b>

[root@ip-172-31-12-138 ~]# mysql --version
mysql  Ver 14.14 Distrib 5.5.57, for Linux (x86_64) using readline 5.1

<b>A command and output that lists all the databases in the server</b>

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
+--------------------+
9 rows in set (0.00 sec)

mysql> select @@hostname;
+------------------+
| @@hostname       |
+------------------+
| ip-172-31-12-138 |
+------------------+
1 row in set (0.00 sec)


</p>
