<pre>

<b>A command and output that shows the hostname of your database server</b>

mysql> select @@hostname;
+------------------+
| @@hostname       |
+------------------+
| ip-172-31-21-134 |
+------------------+
1 row in set (0.00 sec)


<b>A command and output that reports the database server version</b>

[root@ip-172-31-21-134 ~]# mysql --version
mysql  Ver 14.14 Distrib 5.5.57, for Linux (x86_64) using readline 5.1

[root@ip-172-31-21-134 ~]# mysql
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 5
Server version: 5.5.57 MySQL Community Server (GPL)

Copyright (c) 2000, 2017, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.


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
| test               |
+--------------------+
9 rows in set (0.00 sec)


</pre>
