##  Subject
Subnetting is when a bigger network is divided into smaller networks.

Subnetting helps to reduce network congestion by breaking a network into smaller networks called subnets.  

It is a useful way to secure a network by dividing it into different parts. 

It also makes maintenance easier.


##  Assignment


Create a network architecture that meets the following requirements:


1.  1 subnet that is only accessible from within the LAN. This subnet must be able to accommodate at least 15 hosts.


2.  1 subnet with internet access via a router with NAT functionality. This subnet must be able to accommodate at least 30 hosts (the 30 hosts are excluding the router).


3.  1 subnet with a network gateway to the internet. This subnet must be able to accommodate at least 5 hosts (the 5 hosts are excluding the internet gateway).


Place the architecture you have created, including a brief explanation, in the GitHub repository that you have shared with the learning coach.


##  Key Terms

Host - each device that requires an IP address on a network

CIDR - Classless Internet Domain Routing is a standard notation used for subnetting.  

LAN - This is a Local Area Network, so limited to a specific geographic area like a home network or campus network.  Devices on a LAN can communicate with each other directly without needing to go to an external network.  In order to make communication on a LAN possible, each device on the network requires an IP address.  

In order to set up a LAN, the following devices are required:

Network Topology - The physcial and logical way that devices are connected on a network

Star Network Topology - Each node on the LAN is connected to a central hub

Router with NAT functionality - This router has two interfaces, one connecting to the private network and one connecting to the public network (internet)

## Diffulties


##  Resources

[Geeks for Geeks](https://www.geeksforgeeks.org/introduction-to-subnetting/?ref=header_search)

ChatGPT

[Lucidchart](https://www.lucidchart.com/pages/network-diagram/how-to-draw-a-network-diagram)

[Subnet Ninja](https://subnet.ninja)

## Results

1.  *1 subnet that is only accessible from within the LAN. This subnet must be able to accommodate at least 15 hosts.*

Using an online subnet calclutor, I got the following information for my first subnet for an internal LAN (/28)

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/27c06bf7-7bec-4c8b-8ad9-66708f80fa74

This network is private as it only accessable from within the Local Area Network.  Key components to this subnet are:




From the calulator, here is the information for my second subnet with interet access via a NAT router:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/a12c880a-5942-439d-a88e-aa3d6b87ac5e)


Here is the information for my third subnet with an internet gateway using CIDR notation (/29):

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/24e3dfbf-a38b-43a3-87f4-42a8b3964e3b)

Representing these in a diagram below:





Learning/Reflection
I found the concept of subnetting logical and elegant but the execution eluded me.  I struggled to understand how the division and allocation of the addresses worked.  I moved between this subject and the other assignments and on reflection, it worked to step away and let it rest for a bit.
