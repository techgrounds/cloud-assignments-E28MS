## Subject

Azure virtual networks (VNets) ensure that resources such as VMs, web apps, and databases can communicate with each other, with users on the internet, and with on-premises machines.

VNets have the following responsibilities:

- (Network) isolation and segmentation
- Internet communication
- Communication between Azure resources
- Communication with on-premises resources
- Routing of network traffic
- Filtering of network traffic
- Connecting to other VNets

When you create a new VNet, you define a private IP range for your network. Within that range, you can create subnets.

There are three ways to connect your network to an on-premises network:

- Point-to-site VPNs: The Azure VNet is accessed with a VPN from an on-prem computer.
- Site-to-site VPNs: The on-prem VPN device or gateway is connected to the Azure VPN Gateway, effectively creating one large local network.
- Azure ExpressRoute: This is a physical connection from your local environment to Azure.

You can also connect two Azure VNets to each other using virtual network peering. This is facilitated by user-defined Routing (UDR). Peering is possible between VNets in different regions.

An easy way to determine how traffic is routed is to look at a NIC under "effective routes". This shows the routes and the route tables associated with them.

## Assignment

###  Assignment 1:

Create a Virtual Network with the following requirements:

Region: West Europe
Name: Lab-VNet
IP range: 10.0.0.0/16

Requirements for subnet 1:
Name: Subnet-1
IP Range: 10.0.0.0/24
This subnet should have no route to the internet.

Requirements for subnet 2:
Name: Subnet-2
IP Range: 10.0.1.0/24

###  Assignment 2:

Create a VM with the following requirements:

An Apache server must be installed with the following custom data:

```
#!/bin/bash
sudo su
apt update
apt install apache2 -y
ufw allow 'Apache'
systemctl enable apache2
systemctl restart apache2
```

SSH access is not required, but HTTP is.

Subnet: Subnet-1

Public IP: Enabled

Verify if your website is accessible.

##  Key Terms

*virtual network peering*

*Service Endpoints:*

Service endpoints allow your virtual network resources to communicate with Azure services over a private link. This can enhance security and performance by keeping traffic within the Azure backbone network.

You can enable service endpoints for specific Azure services such as Azure Storage, Azure SQL Database, Azure Key Vault, etc., if needed for your application.

*Subnet Delegation:*

Subnet delegation allows you to delegate the management of certain Azure services to a specific subnet within your Virtual Network. This is commonly used for Azure services like Azure Kubernetes Service (AKS) or Azure Firewall.

If you plan to use specific Azure services that require subnet delegation, you may need to configure subnet delegation accordingly.

*Network Policy for Private Endpoints:*

Network policies control the traffic flow within your Virtual Network. Private endpoints allow you to connect to Azure services privately from within your Virtual Network.
If you have private endpoints configured for specific Azure services, you may need to define network policies to control the traffic flow to and from these endpoints.

route tables

##  Resources

##  Difficulties

I found it troublesome to understand the subnet IP address ranges.  I need to spend some more time on this.

##  Results

###  Assignment 1:

###  Here are the details of Subnet-1 that I created, with the specificed IP address ranges and no internet access:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/99be7f94-725f-45f9-a0fa-9ce91ae32131)


###  Here are the details of Subnet-2:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/a49e5137-05c8-43a4-9c2b-360fb67aa1b8


###  Assignment 2:


Here are the Networking settings on my VM:


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/e5b46c0b-ce3c-4fc8-8cda-63609585d4fb)


Here my VM is created:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/26193880-2892-4585-b1a4-032c830751d0)


My Apache web server was available on the first try! Success!


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/d6b944e6-e9f4-4412-9816-c683f3ecfecb)






