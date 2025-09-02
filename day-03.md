
# Task: Day 3: Secure Root SSH Access

## Description
Following security audits, the xFusionCorp Industries security team has rolled out new protocols, including the restriction of direct root SSH login. 

# Task 

Your task is to disable direct SSH root login on all app servers within the Stratos Datacenter.

[root@stapp01 ~] ssh tony@serveraddress

[root@stapp01 ~] sudo su -

[root@stapp01 ~]# vi /etc/ssh/sshd_config


**Find the line and modify**

PermitRootLogin no

[root@stapp01 ~]# systemctl restart sshd


