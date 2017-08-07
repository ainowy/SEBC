Show tables 
1: jdbc:hive2://ip-172-31-36-207:10000/defaul> show tables;
INFO  : Compiling command(queryId=hive_20170608091919_2e27d05a-8260-409a-8c4c-342860fe3de5): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170608091919_2e27d05a-8260-409a-8c4c-342860fe3de5); Time taken: 0.916 seconds
INFO  : Executing command(queryId=hive_20170608091919_2e27d05a-8260-409a-8c4c-342860fe3de5): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170608091919_2e27d05a-8260-409a-8c4c-342860fe3de5); Time taken: 0.324 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (2.51 seconds)

 show tables with grant 

1: jdbc:hive2://ip-172-31-36-207:10000/defaul> show tables;
INFO  : Compiling command(queryId=hive_20170608092121_1182522c-eeaf-491d-a7ac-753ad2ad74fd): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170608092121_1182522c-eeaf-491d-a7ac-753ad2ad74fd); Time taken: 0.079 seconds
INFO  : Executing command(queryId=hive_20170608092121_1182522c-eeaf-491d-a7ac-753ad2ad74fd): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170608092121_1182522c-eeaf-491d-a7ac-753ad2ad74fd); Time taken: 0.154 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.288 seconds)

show tables george's group

beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-36-207@REALM.COM
scan complete in 3ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-36-207@REALM.COM
Enter username for jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-36-207@REALM.COM: george
Enter password for jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-36-207@REALM.COM: *********
Connected to: Apache Hive (version 1.1.0-cdh5.8.3)
Driver: Hive JDBC (version 1.1.0-cdh5.8.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170608095353_030499ea-4ac8-4c74-8c81-d9fdcbc017f5): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170608095353_030499ea-4ac8-4c74-8c81-d9fdcbc017f5); Time taken: 0.067 seconds
INFO  : Executing command(queryId=hive_20170608095353_030499ea-4ac8-4c74-8c81-d9fdcbc017f5): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170608095353_030499ea-4ac8-4c74-8c81-d9fdcbc017f5); Time taken: 0.142 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.332 seconds)

 show tables ferdinand's group

beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-36-207@REALM.COM
scan complete in 3ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-36-207@REALM.COM
Enter username for jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-36-207@REALM.COM: ferdinand
Enter password for jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-36-207@REALM.COM: *********
Connected to: Apache Hive (version 1.1.0-cdh5.8.3)
Driver: Hive JDBC (version 1.1.0-cdh5.8.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170608095555_3592d832-438f-4fa3-9741-90873f9d89a9): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170608095555_3592d832-438f-4fa3-9741-90873f9d89a9); Time taken: 0.062 seconds
INFO  : Executing command(queryId=hive_20170608095555_3592d832-438f-4fa3-9741-90873f9d89a9): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170608095555_3592d832-438f-4fa3-9741-90873f9d89a9); Time taken: 0.128 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.312 seconds)
```
