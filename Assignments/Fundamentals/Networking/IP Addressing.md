## Subject
This assignment is about IP Addressing and introduces concepts like public and private IP Addresses, IPv4 and IPv6 etc.


##  Assignment

1.  Find out what your public IP address is for your laptop and mobile on WiFi.


   Are the addresses the same or not? Explain why.


2.  Find out what your private IP address is for your laptop and mobile on WiFi.


   Are the addresses the same or not? Explain why.


3.  Change the private IP address of your mobile to that of your laptop. What happens then?


4.  Try changing the private IP address of your mobile to an address outside your network. What happens then?




## Key Terms

*IP adresses* - A unique numerical label that is assigned to each device on the internet.  Internet Protocol (IP) addresses are needed to ensure that information can be sent to the correct location ie the device that requested it.


*IPv4*

*IPv4 is the fourth version of the Internet Protocol, which has been widely used since the early days of the internet.

*It uses a 32-bit address scheme, allowing for approximately 4.3 billion unique addresses.

*IPv4 addresses are typically expressed in dotted-decimal notation (e.g., 192.168.0.1).

*Due to the rapid growth of internet-connected devices, IPv4 addresses are now in short supply, leading to the adoption of IPv6.

*IPv6*

*IPv6 is the latest version of the Internet Protocol, designed to address the limitations of IPv4 and accommodate the growing number of internet-connected devices.

*It uses a 128-bit address scheme, providing an exponentially larger pool of unique addresses compared to IPv4.

*IPv6 addresses are typically expressed in hexadecimal notation (e.g., 2001:0db8:85a3:0000:0000:8a2e:0370:7334).

*IPv6 offers built-in features such as improved security, better support for mobile devices, and enhanced network auto-configuration.

*While IPv6 adoption has been steadily increasing, IPv4 remains widely used, and many networks operate with dual-stack support for both IPv4 and IPv6.



Public and Private IPs - IP addresses are classified as Public and Private.  

*Private IP* addresses are not able to be viewed by people outside of your private network.  

Private IP addresses are used for devices on the same (private) network (LAN) to communicate with each other and only work on LAN.

They are more secure than Public IP addresses and are assigned by the router. 

They require NAT to communicate with devices.

Can be viewed used ipconfig command in terminal.

*Public IP* addresses are used for communication outside the private network (the internet).  

They are not as secure and are assignmed by the Internet Service Provider. 

*NAT* - Network Address Translation allows multiple devices to access the Internet through a single public address. To achieve this, the translation of a private IP address to a public IP address is required. NAT is a process in which one or more local IP address is translated into one or more Global IP address and vice versa in order to provide Internet access to the local hosts. 

When a packet traverse outside the local (inside) network, then NAT converts that local (private) IP address to a global (public) IP address. When a packet enters the local network, the global (public) IP address is converted to a local (private) IP address. 


Static and dynamic adresses:

*Static*

*A static IP address remains constant and doesn't change unless manually modified by the network administrator.

*Configuration: It's configured directly on the device or assigned by the network administrator via the router or DHCP server settings.

*Use Cases:  Static IP addresses are often used for servers, network devices, printers, and other equipment that need consistent and predictable addressing.
They are beneficial for services that require remote access or hosting, such as web servers, FTP servers, or email servers.

*Dynamic*  
* Every time your device connects to the internet, your Internet Service Provider (ISP) provides an IP address to your device.  It will be a new IP address every time.  This is a dynamic IP address. 

* They are typically assigned by a DHCP (Dynamic Host Configuration Protocol) server. Unlike static IP addresses, dynamic IP addresses may change over time.

* Assigned automatically by a DHCP server when a device connects to a network. The DHCP server manages a pool of available IP addresses and assigns them dynamically to devices as needed.

* Devices configured to obtain IP addresses dynamically (using DHCP) request an address from the DHCP server when they connect to the network. The DHCP server then assigns an available IP address from its pool to the requesting device.

*  Dynamic IP addresses are commonly used in home and office networks, where devices connect and disconnect frequently.


## Resources

[Geeks for Geeks](https://www.geeksforgeeks.org/difference-between-private-and-public-ip-addresses/)

ChatGPT

[What's My IP?](https://whatsmyip.com/)

[Geeks for Geeks DHCP](https://www.geeksforgeeks.org/dynamic-host-configuration-protocol-dhcp/?ref=header_search)


##  Results

1.   In order to find the public IP adress for my tablet, I just googled : What is my IP address? and found several websites that shows this information:
   

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/4ef2b7c9-73cd-491a-a706-84886eb0c3f5)



To get my phone's public IP, I opened my browser and googled the same: What is My IP address?




My phone and tablet's public IP addresses are different, because each device on network has a different IP address.


2.  I located my phone's private IP address by opening the Settings menu, and from there opening the WiFi settings.  It displayed the IP adress with some other information like Security and Network Speed.

In order to locate my tablet's private IP address, I used the terminal and the *ipconfig* command:  


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/135ebfcc-bb3d-4b77-b701-381fab4b27df)

3.  I changed my phone's private IPv4 address to the same IPv4 address as my laptop by first changing my phone's private IP address to 'Static' and then changing the last few digits of the IP address on my phone.  Consequently, even though my phone showed that it was connected to the WiFi network, it couldn't access the internet.  Once I reverted the settings back from Static to DHCP, the IP address changed to another one and my phone then connected to the internet as normal.

4.  I changed my phone's IP address to 203.0.113.1, which is outside my network and it wouldn't connect to the internet.  Once I reverted back to DHCP, it re-connected and started working as normal.
  

##  Learning/Reflection
It feels like I've just scratched the surface of this subject.  Doing these excercises has deepened my understanding of how the devices in a network communicate with each other but I have a lot left to learn.

