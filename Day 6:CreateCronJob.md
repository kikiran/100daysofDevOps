### The Nautilus system admins team has prepared scripts to automate several day-to-day tasks. They want them to be deployed on all app servers in Stratos DC on a set schedule. Before that they need to test similar functionality with a sample cron job. Therefore, perform the steps below: 

## a. Install cronie package on all Nautilus app servers and start crond service. 

## b. Add a cron */5 * * * * echo hello > /tmp/cron_text for root user.

# Created shell script file / Solution

#!/bin/bash

#### Install cronie package
yum install -y cronie

#### Start and enable crond service
systemctl start crond
systemctl enable crond

#### Add cron job for root user
echo "*/5 * * * * echo hello > /tmp/cron_text" | crontab -

#### Verify cron job
crontab -l