<p>
b>MYSQL VERSION</b>

[root@ip-172-31-12-49 ~]# mysql --version
mysql  Ver 14.14 Distrib 5.6.37, for Linux (x86_64) using  EditLine wrapper


<b>list of databases</b>

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

<b>List of grants</b>

mysql> show grants for cloudera;
+---------------------------------------------------------------------------------------------------------+
| Grants for cloudera@%                                                                                   |
+---------------------------------------------------------------------------------------------------------+
| GRANT USAGE ON *.* TO 'cloudera'@'%' IDENTIFIED BY PASSWORD '*B31B944294DF71513F06E1E842F9F70D5DE65ABD' |
| GRANT ALL PRIVILEGES ON `scm`.* TO 'cloudera'@'%'                                                       |
+---------------------------------------------------------------------------------------------------------+
2 rows in set (0.00 sec)

mysql> show grants for oozie;
+------------------------------------------------------------------------------------------------------+
| Grants for oozie@%                                                                                   |
+------------------------------------------------------------------------------------------------------+
| GRANT USAGE ON *.* TO 'oozie'@'%' IDENTIFIED BY PASSWORD '*B31B944294DF71513F06E1E842F9F70D5DE65ABD' |
| GRANT ALL PRIVILEGES ON `oozie`.* TO 'oozie'@'%'                                                     |
+------------------------------------------------------------------------------------------------------+
2 rows in set (0.00 sec)

mysql> show grants for sentry;
+-------------------------------------------------------------------------------------------------------+
| Grants for sentry@%                                                                                   |
+-------------------------------------------------------------------------------------------------------+
| GRANT USAGE ON *.* TO 'sentry'@'%' IDENTIFIED BY PASSWORD '*B31B944294DF71513F06E1E842F9F70D5DE65ABD' |
| GRANT ALL PRIVILEGES ON `sentry`.* TO 'sentry'@'%'                                                    |
+-------------------------------------------------------------------------------------------------------+
2 rows in set (0.00 sec)

mysql> show grants for rman;
+-----------------------------------------------------------------------------------------------------+
| Grants for rman@%                                                                                   |
+-----------------------------------------------------------------------------------------------------+
| GRANT USAGE ON *.* TO 'rman'@'%' IDENTIFIED BY PASSWORD '*B31B944294DF71513F06E1E842F9F70D5DE65ABD' |
| GRANT ALL PRIVILEGES ON `rman`.* TO 'rman'@'%'                                                      |
+-----------------------------------------------------------------------------------------------------+
2 rows in set (0.00 sec)


</p>
