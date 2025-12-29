The system admins team of xFusionCorp Industries has set up some scripts on jump host that run on regular intervals and perform operations on all app servers in Stratos Datacenter. To make these scripts work properly we need to make sure the thor user on jump host has password-less SSH access to all app servers through their respective sudo users (i.e tony for app server 1). Based on the requirements, perform the following:


# Task: linux SSH Authentication

Set up a password-less authentication from user thor on jump host to all app servers through their respective sudo users.


✅ STEP 1: Login as thor on jump host

su - thor

✅ STEP 2: Generate SSH key for thor (if not exists)

ssh-keygen -t rsa -b 2048

✅ STEP 3: Copy public key to all app servers

ssh-copy-id tony@stapp01

# make it copy all servers

# to check use below command

ssh tony@stapp01
