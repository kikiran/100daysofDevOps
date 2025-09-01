To accommodate the backup agent tool's specifications, the system admin team at 
xFusionCorp Industries requires the creation of a user with a non-interactive shell. Here's your task:



Create a user named james with a non-interactive shell on App Server 3.

**Solution**

#login with user using ssh

ssh banner@stapp03.stratos.xfusioncorp.com
sudo useradd -s /sbin/nologin james

sudo grep james /etc/passwd