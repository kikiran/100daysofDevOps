# Task: Create User with Non-Interactive Shell

## Description
To accommodate the backup agent tool's specifications, the system admin team at **xFusionCorp Industries** requires the creation of a user with a **non-interactive shell**.  

We need to create a user named **james** on **App Server 3**

**Solution**

#login with user using ssh

ssh banner@stapp03.stratos.xfusioncorp.com
sudo useradd -s /sbin/nologin james

sudo grep james /etc/passwd