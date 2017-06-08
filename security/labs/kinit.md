
For example, I will create a Kerberos ticket with cloudera-scm principal:

[root@ip-172-31-39-40 ~]# kinit cloudera-scm/admin
Password for cloudera-scm/admin@AINOWY.ES:


We check out that the ticket was created:

[root@ip-172-31-39-40 ~]# klist
Ticket cache: FILE:/tmp/krb5cc_0
Default principal: cloudera-scm/admin@AINOWY.ES

Valid starting     Expires            Service principal
06/08/17 00:42:07  06/09/17 00:42:07  krbtgt/AINOWY.ES@AINOWY.ES
        renew until 06/08/17 00:42:07
