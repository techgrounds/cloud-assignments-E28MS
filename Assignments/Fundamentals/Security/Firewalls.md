##  Subject

This assignment is about firewalls and understanding the first concepts of how to prevent unwanted or unauthorised access from the web into your machine.  It draws on previously covered topics like SSH, ports and the Linux command line.

##  Assignment

Install a web server on your VM.

View the default page that is installed with the web server via your browser on your PC/laptop.

Set the firewall so that you block web traffic, but allow SSH traffic.

Check whether the firewall is doing its job.

##  Key Terms

*firewall* - in this case, the firewall is a piece of software that is available on the Linux machine.  It allows you to set up rules for which ports are open to which type of traffic.

*ufw* - standard firewall for Ubuntu

*Stateful firewalls :* 
This firewall is situated at Layers 3 and 4 of the Open Systems Interconnection (OSI) model. As the name suggests, a stateful firewall always keeps track of the state of network connections. Once a particular kind of traffic has been approved by a stateful firewall, it is added to a state table. The state table entries are created for TCP (Transmission Control Protocol) streams or UDP (User Datagram Protocol) datagrams that are allowed to communicate through the firewall in accordance with the configured security policy.  If no traffic is seen for a specified time (implementation dependent), the connection is removed from the state table.

Pros- 

Stateful firewalls are highly skilled to detect forged messaging or unauthorized access.
These firewalls have a powerful memory to retain key aspects of network connections.
They are intelligent systems. They make future filtering decisions based on the past and present results. It means that it can automatically stop a specific cyber attack in the future once it encountered it, without the need for updates.
These firewalls do not need many ports open for proper communication.
Stateful firewalls offer extensive logging capabilities and stronger attack mitigation.


Cons-

-  Stateful firewalls can be vulnerable to distributed denial-of-service (DDoS) attacks.
-  These firewalls have to be updated with the latest software releases, otherwise, vulnerabilities may allow hackers to take control over the firewall.
-  They can be fooled into allowing a harmful connection to the network and it can happen with a simple action like viewing a webpage.
-  These firewalls may be more sensitive to man-in-the-middle (MITM) attacks, which involve an attacker intercepting communication between two people to either spy on the traffic or make changes to it.


*Stateless firewalls :*
It is also known as an access control list (ACL), does not store information on the connection state. Stateless ACLs are applicable to the network and physical layers, and sometimes the transport layer to find out the source and destination port numbers. When the sender sends a packet and gets filtered through a firewall, the device checks for matches to any of the ACL rules that are configured in the firewall and then drops or rejects the packet accordingly.

Pros-

Stateless firewalls do not take as much into account as stateful firewalls, they’re generally considered to be less rigorous. That is why they are fast.
As it doesn’t get into that many details, it performs quite well in heavy traffic.
They are generally cheaper than stateful firewalls.

Cons-

A stateless firewall cannot analyze all network traffic (or packets), making it unable to identify traffic type. This results in making it less secure compared to stateful firewalls.
These firewalls, in many instances, may need to be carefully configured by someone familiar with the kinds of traffic and attacks that impact the network. This may require extra time and energy to perform.

##  Resources

[Amazon Tutorials](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Tutorials.WebServerDB.CreateWebServer.html)

[Geeks for Geeks Stateless vs Stateful Firewalls]9https://www.geeksforgeeks.org/stateless-vs-stateful-packet-filtering-firewalls/)



##  Difficulties

I couldn't connect with with my VM on the first try:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/78a6be34-df6a-410d-a964-6f06b062b76a)

So I checked the status of appache, confirmed that it was running now and tried again, with the same result.  Next , I troubleshooted the port access.

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/efc1a89b-34e2-4c0c-8ae1-7c4df0699b5d)



##  Results

##  *Here I found the open ports on my VM:*

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/d0ccdc34-130b-4dc9-a145-9844dec7b0eb)

## *Here I viewed the default page that is installed with the web server via my browser:*

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/f23e6508-d0de-4559-ba86-87f7d01d548d)

## *Install Firewall on VM that allows SSH traffic but blocks web traffic*

Here are the commands I used to allow SSH traffic to standard SSH port 22 as well as my SSH Port 52200.  I then blocked web traffic by denying access to port 443 (https) and port 80 (http):

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/696f51ee-6103-4b2e-984e-2b1229697b71)

I then checked to see if the rules were applied before trying to enable the firewall again:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/b0ef7080-dcbe-4c5f-9e9a-d0713eb82f5d)

And finally enabled the firewall using ufw :

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/d6c00883-d352-4d93-8d54-564c0dc4adff)



Here I tested if I could connect to the webserver on my machine and I couldn't connect

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/f2e5ba94-88c7-42f2-9021-be0228623031)

Here I checked the status of my firewall to see if my set up was succesful and it appears that web traffic is denied and SSH traffic on two ports only are allowed:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/abb3b454-242c-4864-b8c9-6fb85152a84e)





##  Learning/Reflection
Finding out which port to use was key here, I needed to use my webport to view the webpage. 


