## Subject

One of the greatest advantages of the cloud is that you don't have to guess how much capacity you need. You can always scale up and down with on-demand services. One of the services that makes this possible is called Autoscaling.

When you run applications with a spiky workload, you can create a VM Scale Set instead of a single server. When demand for the application is high, Autoscaling can automatically add VMs to your Scale Set. When demand decreases, it can also remove instances.

To ensure that all VMs are the same, you need to designate an image during the configuration of a VM Scale Set. You can later modify this image using the reimage option. Auto Scaling uses Azure Monitor to determine whether VMs should be added or removed.

In a traditional architecture, a client connects to a single server with a single public IP address. When you have a fleet of servers, this no longer works. 

That's why you can use a load balancer as an endpoint for the client. The load balancer will forward the request to one of the servers in your fleet and send the response back to the client.

Azure offers two managed solutions for load balancing to a fleet of servers:

Azure Load Balancer: You get this for free with a VM Scale Set. The ALB operates at layer 4 of the OSI stack (TCP/UDP). An ALB can only route to Azure resources.

Application Gateway: This load balancer operates at layer 7 of the OSI stack (HTTP/HTTPS). It also supports features such as SSL termination and Web Application Firewall (WAF). An Application Gateway can route to any routable IP address.



## Assignment

###  Task 1:
Create a Virtual Machine Scale Set with the following requirements:

Ubuntu Server 20.04 LTS - Gen1

Size: Standard_B1ls

Allowed inbound ports:
SSH (22)
HTTP (80)

OS Disk type: Standard SSD

Networking: defaults

Boot diagnostics are not required

Custom data:

```
#!/bin/bash
sudo su
apt update
apt install apache2 -y
ufw allow 'Apache'
systemctl enable apache2
systemctl restart apache2
```

Initial Instance Count: 2

Scaling Policy: Custom

Number of VMs: minimum 1 and maximum 4

Add a VM at 75% CPU usage

Remove a VM at 30% CPU usage

 Task 2:
 
Check if you can access the web server via the endpoint of your load balancer.

Perform a load test on your server(s) to trigger auto scaling. There may be a delay in creating new VMs depending on the settings in your VM Scale Set. 

Note: the Azure Load Testing service can be expensive. You can also log in to the VM to perform a manual stress test.

##  Key Terms

*endpoint*
=w21`
*Orchestration modes*

*Load tests vs Stress Tests*

*  Load tests simulate normal traffic, stress tests simulate extreme traffic.

*  Load tests might crash your test environment, stress tests must break your test environment.

*  Load tests determine if you can handle an expected traffic volume, stress tests determine the upper limits of your system capacity.

##  Resources

[Learn Microsoft VMSS](https://azure.microsoft.com/en-us/products/virtual-machine-scale-sets/)

[Learn Microsoft VMSS Documentation](https://learn.microsoft.com/en-gb/azure/virtual-machine-scale-sets/)



##  Difficulties

##  Results

###  Assignment 1:

###  Here are the details of my VMSS, I couldn't find the settings for Autoscaling to add the last parameters but the Learn Microsoft Docs seemed to indicate that this will be an option once the VMSS is created:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/9a763601-df50-417a-97b1-dc9f09f1b334)


###  I selected Inbound Ports 80 and 22 by creating a Network Interface and allowing selected ports.  I also enabled Public IP address: 

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/0f911d8a-bc86-406b-9b90-6ef5198ef4af)


###  Here I adjusted the Scaling Conditions according to the assignment parameters:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/c496e7e6-8712-4df9-942a-5b0ba980fd1b)


###  These are the settings of my VMSS:


### Assignment 2:

When I was setting up the VMSS, I noted that leaving the Network Settings to default as specified in Assignment 1 would mean that there was no load balancer associated with my VMSS.  I anticipated that this would mean that you counldn't progress with Assignment 2 until this was resolved.  

This is indeed the case, given that it specifies you need to connect via the Load Balancer (which isn't set up according to Assignment 2)


###  Here are 2 screenshots confirming that Load Balancing is not set up:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/2e52485c-3c2f-429f-a80e-0b574cbe96b4)

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/f34e0a8e-1df5-4cd5-bd39-c5eb717a814b)



###  Now my load balancer has been set up:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/c7482fec-15de-4cf1-b893-a52a971264e8)

###  In order to check if I could access the web server through the load balancer, I entered the load balancer's Front End IP address into my browser:








