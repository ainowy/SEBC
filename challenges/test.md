
<pre>
REVIEW:

-impala -> impala-shell -i node:21000 (desde el gateway a un worker) -> impala -i worker1
In order to use impala with sentry, we need to do "kinit impala" and then, impala-shell -i

-git hub practice

-AWS: get version of an aws instance, list region, ami id and os you are using
	
	aws ec2 describe-instances --query 'Reservations[*].Instances[*].[InstanceId,Platform]' --output text
	cat /etc/issue
	cat /etc/os-release
	aws ec2 describe-images --image-ids "ami-xxxxxxxx"

$HOME/.aws/config -> ./list -v
aws ec2 describe-instances|grep PublicIpAddress

-github (upload images) -> folder -> upload file -> drag, drop and commit 


-------------------------------

-AWS (instances, security groups (cloudera port, firewall...IPs changing(when turning them off and on))

-practice linux commands

-upgrading cloudera


----------------------

-AWS: get version of an aws instance, list region, ami id and os you are using -> 

-connect with .pem between nodes

-practice linux commands


</pre>
