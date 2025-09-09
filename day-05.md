
# Task: Day 5: SElinux Installation and Configuration

## Description

Following a security audit, the xFusionCorp Industries security team has opted to enhance application and server security with SELinux. To initiate testing, the following requirements have been established for App server 1 in the Stratos Datacenter:


# Tasks

Install the required SELinux packages.

Permanently disable SELinux for the time being; it will be re-enabled after necessary configuration changes.

No need to reboot the server, as a scheduled maintenance reboot is already planned for tonight.

Disregard the current status of SELinux via the command line; the final status after the reboot should be disabled.

# Solution

[tony@stapp01 ~]$ sudo yum install -y selinux-policy selinux-policy-targeted 

[tony@stapp01 ~]$ sudo su -

[root@stapp01 ~]# vi /etc/selinux/config

Find the line:

SELINUX=enforcing

change into 

SELINUX=disabled

[root@stapp01 ~]# grep SELINUX /etc/selinux/config
# SELINUX= can take one of these three values:
# NOTE: Up to RHEL 8 release included, SELINUX=disabled would also
SELINUX=disabled