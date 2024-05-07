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

### Task 2:
 
a)  Check if you can access the web server via the endpoint of your load balancer.

b)  Perform a load test on your server(s) to trigger auto scaling. There may be a delay in creating new VMs depending on the settings in your VM Scale Set. 

Note: the Azure Load Testing service can be expensive. You can also log in to the VM to perform a manual stress test.

##  Key Terms

*backend pool*

The backend pool is a critical component of the load balancer. The backend pool defines the group of resources that will serve traffic for a given load-balancing rule.

There are two ways of configuring a backend pool:

*  Network Interface Card (NIC)

*  IP address

*endpoint*


*Orchestration modes*

*Load tests vs Stress Tests*

*  Load tests simulate normal traffic, stress tests simulate extreme traffic.

*  Load tests might crash your test environment, stress tests must break your test environment.

*  Load tests determine if you can handle an expected traffic volume, stress tests determine the upper limits of your system capacity.

##  Resources

[Learn Microsoft VMSS](https://azure.microsoft.com/en-us/products/virtual-machine-scale-sets/)

[Learn Microsoft VMSS Documentation](https://learn.microsoft.com/en-gb/azure/virtual-machine-scale-sets/)

[Learn Microsoft Azure Load Balancer Backend Pool Management](https://learn.microsoft.com/en-gb/azure/load-balancer/backend-pool-management)

ChatGPT

[Loadview Testing Microsoft Autoscale](https://www.loadview-testing.com/blog/testing-microsoft-azure-autoscale/)


##  Difficulties

*   It took a while to figure out why I couldn't connect to the Apache web server landing page but once I re-configured the Frontend IP and associated the Backend Pool with the VMSS, this was succesful.

*   The second challenge I faced was how to manually run a stress test by logging in remotely to my VM.  I reviewed YouTube videos, searched online forums and then resorted to looking at a previous student's GitHub repository and discovered that there is a CLI stress command! Genius! 

I didn't look any further as I wabt  and asked ChatGPT to put together a tuturial as I know knew how to phrase my question correctly to get helpful input.

*  The next difficulty I encountered was a peristent :Permission denied (publickey) error message that prevented me from connecting to the instance in my VMSS.  

So the troubleshooting commenced.  First, I checkd the NSG on the VMSS and confirmed that SSH(port 22) was enabled:  (It was! It's never the first thing you try, right? :-))


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/f0869f41-8cce-40ea-89f3-1d9f86807c68)

*  Next I checked my username and...you've guessed it! I left out an underscore!  Problem resolved and I promptly SSH'd in succesfully! Yay me!  Also realised that it was maybe time to stop for the day! But not before I tried a few more things! 








##  Results

###  Assignment 1:

###  Here are the details of my VMSS, I couldn't find the settings for Autoscaling to add the last parameters but the Learn Microsoft Docs seemed to indicate that this will be an option once the VMSS is created:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/9a763601-df50-417a-97b1-dc9f09f1b334)

- +-
###  Here I selected the Autoscaling settings after the VMSS was created and set it to Custom as per assignment parameters:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/ef97d4e7-24aa-4078-bbaa-4f14a2c44c8e)



###  I selected Inbound Ports 80 and 22 by creating a Network Interface and allowing selected ports.  I also enabled Public IP address: 

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/0f911d8a-bc86-406b-9b90-6ef5198ef4af)


###  Here I adjusted the Scaling Conditions according to the assignment parameters:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/c496e7e6-8712-4df9-942a-5b0ba980fd1b)


###  These are the settings of my VMSS:


### Assignment 2:

*a)  When I was setting up the VMSS, I noted that leaving the Network Settings to default as specified in Assignment 1 would mean that there was no load balancer associated with my VMSS.  I anticipated that this would mean that you counldn't progress with Assignment 2 until this was resolved.*

This is indeed the case, given that it specifies you need to connect via the Load Balancer (which isn't set up according to Assignment 2)


###  Here are 2 screenshots confirming that Load Balancing is not set up:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/2e52485c-3c2f-429f-a80e-0b574cbe96b4)

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/f34e0a8e-1df5-4cd5-bd39-c5eb717a814b)



###  Now my load balancer has been set up:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/c7482fec-15de-4cf1-b893-a52a971264e8)

###  In order to check if I could access the web server through the load balancer, I entered the load balancer's Front End IP address into my browser:


And got an error message.


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/9688d384-14e0-4769-86fd-9de244b78c1e)


###  Troubleshooting:

Here I added an Inbound Port Rule, specifying the Load Balancer IP address as the destination:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/4d94d025-487d-4546-9ed6-6dc72dfca884)

this didn't resolve the problem.  

I then associated the Load Balancer Backend Pool with the VMSS:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/c7962fde-d8b2-46fc-ade0-ea00c8397172)


And then I reviewed the Frontend IP Configuration:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/c6996b04-89b7-4d69-864a-486ea87dbad8)

Configuring the Frontend IP Confirugation and the Backend Pool resolved the issue and I was able to access the Apache landing page through my load balancer:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/064aa6e6-cab3-44e2-91ac-cddc9c9a2fc5)

*b)  First, I checked the instances and established the IP address of the VM so that I could SSH in remotely to complete a stress test:*

Here is the instance,up and running:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/141c377a-2ee5-4cb2-867d-9e07bcb2a652)


Here are the details, including IP Address that I need to SSH in:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/809c277a-c9c8-4914-88d9-78ac59ce47ff)


So next I SSH'd into my VM in my VMSS and installed the stress apt using the following command:

```
sudo apt update
sudo apt install stress
```

Next I generated a load on my Linux VM using the following command, making use of the parameters I set for scaling out and scaling in during setting up VMSS:

```
stress --cpu 1 --timeout 300s
```

This didn't trigger autoscaling as there was still only instance :

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/690f55b7-17a5-4f72-8836-5c7b829c907b)

So I repeated the command as below:

```
 stress --cpu 75 --timeout 300s
```

I again only saw once instance but when I ran the history in scaling, it seems like it was succesful and I realised that instead of shopping for books while my stress test was running I should be watching the Portal to see if it was autoscaling out:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/d2348697-1c53-451a-93a5-3e4d7038e905)

However, when I did this, I still couldn't see any additional instances being added.

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/ad5c6b98-e95f-415c-8ebd-c4067f819b57)


Here is the information in the cmd when I was completing the stress test:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/44b3cd60-d57b-4dbd-afa9-6e72fcaf9817)






















