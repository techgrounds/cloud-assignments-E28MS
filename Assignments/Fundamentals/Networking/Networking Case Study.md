##  Subject
Case study on networking

##  Assignment

In this case study you take the role of a network administrator setting up a network in the new office of a small e-commerce company. Of course there are multiple ways to go about this problem, but this company has specifically said that network security is extremely important to them.


The office contains the following devices:


A web server where our webshop is hosted
A database with login credentials for users on the webshop
5 workstations for the office workers
A printer
An AD server
A file server containing internal documents


As a network administrator you get to choose which networking devices get used.

##  Key Terms

Web Server -  A server that uses HTTP and other protocols to provide content to users over the internet via a browser.  

Database - A collection of organised and structured information, usually kept on a computer system.  Accessed and controlled by a database management system. 

AD Server - Thhis is a technology system that acts as a centralised platform for managing adverstisements (ads)

File server - This is a computer that stores and makes files available for shared use to all users on a LAN

DMZ - A De-militarized Zone in networking is where a logical or physcical subnet seperates and protects a network's LAN from untrusted network traffic

ACL's - Access control lists are made up of rules that determine if access to a computer environment is allowed or denied. 
 This means that unless the proper credentials are presented by a device, it cannot gain access.  There are two types of Access Control Lists:  

  Network Access Control Lists (NACL's) are used to restrict access to a network by giving instructions to routers and 
  switches about which type of traffic is allowed to interface with a network.  They also provide instruction on what each 
  user or device is allowed to do once interfacing with the network.

  File Access Control lists are used to restrict access to files

VLAN's - A Virtual Local Area Network is a way of logically seperating a group of computers into a seperate network, so they will only communicate with each other and not with any other devices connected to the same physcial network.  

Firewall - A network security system or shielding layer between your computer (or network) and the internet.  It can be a piece of hardware or software.


##  Resources

[SolarWinds](https://www.solarwinds.com/resources/it-glossary/web-server#:~:text=a%20web%20server-,Web%20Server%20Definition,internet%20via%20a%20web%20browser.)

[Oracle](https://www.oracle.com/database/what-is-database/#:~:text=A%20database%20is%20an%20organized,database%20management%20system%20(DBMS).)

[ADjust](https://www.adjust.com/glossary/ad-server-definition/)

[Fortinet](https://www.fortinet.com/resources/cyberglossary/network-access-control-list#:~:text=A%20network%20access%20control%20list%20(ACL)%20is%20made%20up%20of,are%20allowed%20in%20the%20doors.)

([Beer 30 Good Network Design](https://www.youtube.com/watch?v=oopkClg1kxM&t=373s&ab_channel=SecureState)

[Geeks for Geeks](https://www.geeksforgeeks.org/difference-between-hardware-firewall-and-software-firewall/?ref=header_search)


##  Difficulties

##  Results

Using the Bonus Video as a starting place made the proposed architecture easy and logical to understand.  

In summary, in order to set up a secure network as per the case study, it is important to make use of several security measures in setting up the network architecture.  

This ensures that outside traffic does not have direct access into your network.  

Instead, my proposed architecture seperates the e-commerce copmany's network into several subnets and a VLAN (for the part of the network dealing with outside traffic from customers) and makes use of various network devices like routers (incuding an edge router) and software like ACL's to add additional layers of security, both to control the traffic into the external server that has the client log in details and also internally by seperating the commercial assests from the user zone.

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/3679fcfe-5eaa-4333-a480-3f1f32a2282a)




##  
