<pre>

<b>For example, I will create a Kerberos ticket with cloudera-scm principal:</b>

[root@ip-172-31-39-40 ~]# kinit cloudera-scm/admin
Password for cloudera-scm/admin@AINOWY.ES:


<b>We check out that the ticket was created:</b>

[root@ip-172-31-39-40 ~]# klist
Ticket cache: FILE:/tmp/krb5cc_0
Default principal: cloudera-scm/admin@AINOWY.ES

Valid starting     Expires            Service principal
06/08/17 00:42:07  06/09/17 00:42:07  krbtgt/AINOWY.ES@AINOWY.ES
        renew until 06/08/17 00:42:07
        
In order to access hdfs, we will need to create a principal too so we create it and create a ticket too to check everything was done 
correctly:

[root@ip-172-31-39-40 ~]# kinit hdfs@AINOWY.ES
Password for hdfs@AINOWY.ES:

[root@ip-172-31-39-40 ~]# klist -e
Ticket cache: FILE:/tmp/krb5cc_0
Default principal: hdfs@AINOWY.ES

Valid starting     Expires            Service principal
06/08/17 08:20:48  06/09/17 08:20:48  krbtgt/AINOWY.ES@AINOWY.ES
        renew until 06/08/17 08:20:48, Etype (skey, tkt): arcfour-hmac, aes256-cts-hmac-sha1-96


</pre>
