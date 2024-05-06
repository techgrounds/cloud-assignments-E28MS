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

endpoint - 

##  Resources

##  Difficulties

##  Results
