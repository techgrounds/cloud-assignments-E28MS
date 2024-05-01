## Subject

The service for creating VMs in Azure is appropriately named Azure Virtual Machines. You can use these VMs for anything you would use a physical server for. Since they reside in a Microsoft datacenter, you can only connect to them via the internet. To connect to a remote Linux machine, you use the Secure Shell (SSH) protocol. For connecting to Windows machines, you use the Remote Desktop Protocol (RDP).

To create a VM, you need to select an image. An image is a kind of blueprint for your machine, containing a template for the OS among other things.

VMs come in various sizes, each offering different amounts of vCPUs, RAM, Data disks, Max IOPS, Temp storage, Premium disk support, and price.

For the OS disk (the root volume), you can choose from Premium SSD, Standard SSD, and Standard HDD. You also have the option to add extra Data disks.

You can optionally secure your VM with a NIC network security group. It's recommended to configure network security groups at the subnet level (and not at the instance level) where possible, but sometimes you may need an allow/deny rule on a specific instance, so the option is there. In any case, you can manage firewalls outside the instance, eliminating the need for an additional firewall configuration within the VM.

With Custom Data, you can include a cloud-init script, config file, or other data during VM startup. This allows you to automatically configure servers without needing to log in. User data is a newer version of Custom Data. The main difference is that User Data remains available throughout the VM's lifespan.

The price of an Azure VM depends on the size, image, region it's in, the number of minutes it's running, and the type of payment you choose.

Pay-as-you-go is the most expensive option but also the most flexible. Reserved Instances are cheaper, but you're committed to a reservation of 1 or 3 years. Spot instances are generally the cheapest, but their availability depends on the demand for VMs at that time, so they're not always reliable.

## Assignment

Log in to your Azure Console.

Create a VM with the following requirements:

*  Ubuntu Server 20.04 LTS - Gen1
*  Size: Standard_B1ls
*  Allowed inbound ports: HTTP (80), SSH (22)
*  OS Disk type: Standard SSD
*  Networking: defaults
*  Boot diagnostics are not needed
  
Custom data:

```
bash
Copy code
#!/bin/bash
sudo su
apt update
apt install apache2 -y
ufw allow 'Apache'
systemctl enable apache2
systemctl restart apache2

```

Verify that your server is functioning.

Note: After completing the task, don't forget to clean up everything. You can delete each component individually or delete the entire resource group at once.







##  Key Terms

##  Resources

##  Difficulties

##  Results

###  Here I'm setting up the VM according to the parameters of the assignment:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/1618cd3a-5ad0-403c-ac38-80c68335650e)

###  Here are the networking default settings:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/0caa930b-9f81-48f3-a42a-e889d70caee8)


###  Boot diagnostics disabled:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/34959014-4a2e-41f8-bd26-492df82e57fb)

###  Custom data provided in assignment added to the Custom Data section int he Advanced tab:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/bc9631eb-1542-43c6-912b-d3fafd2c0b42)

###  Deployment complete:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/5ba82c8f-90c5-4dbc-9774-0cd078b428a6)

##  Verifying that VM is up and running, see Public IP Address:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/f3fb930f-ee2a-4b56-8ee4-e29d0ae6e6fe)

###  Here I've logged into my VM:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/566a1c76-e282-41d8-8e11-83a577825733)

###  And tested that Apache is running:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/c3d89bd2-fc37-474c-b7b8-75b0b1b3976d)

###  Tested access through web browser by entering IP Address and got confirmation in the form of the Apache landing page:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/ff99a168-63e3-4c37-9e19-505926f6bb70)

###  Tested Port 80 is accessable:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/ed7a54d2-5233-413d-b625-d35215a12138)










