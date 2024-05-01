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

