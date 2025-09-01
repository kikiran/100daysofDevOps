# Task: Day 2: Temporary User Setup with Expiry

## Description
As part of the temporary assignment to the Nautilus project, a developer named kirsty requires access for a limited duration. To ensure smooth access management, a temporary user account with an expiry date is needed. Here's what you need to do:


## Details
Create a user named kirsty on App Server 2 in Stratos Datacenter. Set the expiry date to 2024-04-15, ensuring the user is created in lowercase as per standard protocol.

**Solution**
sudo useradd -e 2024-04-15 kirsty

**Verify user expiry**
sudo chage -l  kristy