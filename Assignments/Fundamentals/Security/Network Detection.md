##  Subject

The subject of this assigment is network detection.  

Network detection refers to the process of identifying and understanding the devices, connections, and traffic on a computer network. It's like mapping out the roads, intersections, and vehicles in a city to understand how everything is connected and where it's going.  For the purposes of this excercise, it relates mainly to understanding the network traffic.

Interestingly, I found it difficult to find a defintion that didn't include NDR (see below):

Network detection and response (NDR) solutions use a combination of non-signature-based advanced analytical techniques such as machine learning to detect suspicious network activity. This enables teams to respond to anomalous or malicious traffic and threats that other security tools miss

##  Key Terms

Nmap -Short for Network Mapper. It is an open-source Linux command-line tool that is used to scan IP addresses and ports in a network and to detect installed applications.



##  Assignment

Scan the network of your Linux machine using nmap. What do you find?


Open Wireshark in Windows/MacOS Machine. Analyse what happens when you open an internet browser. (Tip: you will find that Zoom is constantly sending packets over the network. You can either turn off Zoom for a minute, or look for the packets sent by the browser between the packets sent by Zoom.)

##  Resources

[Cisco NDR](https://www.cisco.com/c/en/us/products/security/what-is-network-detection-response.html#:~:text=Network%20detection%20and%20response%20(NDR,that%20other%20security%20tools%20miss)

ChatGPT

[Free Code Camp The Greatest Scanning Tool of All Time](https://www.freecodecamp.org/news/what-is-nmap-and-how-to-use-it-a-tutorial-for-the-greatest-scanning-tool-of-all-time/)



##  Difficulties

The first time I tried scanning my VM, I got an error message saying the host may be down.  I resolved this by using the *-Pn* command, see screenshots in *Results*

I don't feel like I've been succesful at understanding the information displayed by Wireshark.

##  Results

# Scanning VM's Network:

First attempts at scanning VM's network not succesful:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/0c89f5e7-beaf-4b9b-8fd8-865dcb1126a7)

Using the *-Pn* command enabled the VM to be scanned:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/16fa4bbd-3018-464c-b249-d6dc61e95c85)

### I interpreted this information as follows:

The Nmap scan report indicates that the host (in this case, an EC2 instance on AWS) is up, but all 1000 scanned ports are in ignored states, and 1000 filtered TCP ports are not shown due to no response.


1. **Host is up**: This indicates that the target host (EC2 instance) is online and responsive to Nmap probes.

2. **All 1000 scanned ports are in ignored states**: This means that Nmap has determined that all 1000 scanned ports on the host are in an "ignored" state. An "ignored" state typically means that Nmap couldn't determine whether the port is open, closed, or filtered due to various reasons such as firewalls, network configurations, or Nmap timing settings.

3. **Not shown: 1000 filtered TCP ports (no-response)**: This part of the report indicates that Nmap did not show information about 1000 filtered TCP ports. Filtered ports are those where Nmap is unable to determine whether they are open or closed due to firewall filtering, packet filtering, or other reasons. In this case, Nmap received no response from these ports during the scan.

Overall, the scan report suggests that the target host, my VM,  is up and responsive, but the scan results for the ports are inconclusive due to being in ignored or filtered states. This could be due to various factors such as firewall configurations, network settings, or Nmap timing options.

### I repeated the scan of my VM a week later and got different results:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/0ab9b627-239f-4950-a80f-d9caa240d8e4)

Both scans indicate that the host is up, meaning the target EC2 instance is online and responsive.


In the previous scan, all 1000 scanned ports were reported to be in ignored states, which means Nmap couldn't determine their status due to various reasons such as firewalls, network configurations, or Nmap timing settings.


In the current scan, all 1000 scanned ports are reported as filtered, indicating that Nmap did not receive any response from these ports during the scan.

### Analysis:

The difference between the previous and current scan results lies in how Nmap categorized the ports. In the previous scan, the ports were categorized as "ignored," while in the current scan, they are categorized as "filtered."

The change in categorization could be attributed to changes in the network configuration, firewall rules, or Nmap timing settings between the two scans.

It's also possible that the previous scan encountered different network conditions or configurations that resulted in Nmap being unable to determine the status of the ports, whereas in the current scan, the ports were definitively reported as filtered due to lack of response.

I take it that this could be because of the work I've done between the first VM scan and this scan around setting up a firewall on my VM.


### Analyze what happens when you open an internet browser

At first I tried to filter for http but this didn't bring up any traffic, possibly as I'm using a VPN, which encrypts and decripts data.  In order to see the traffic when I open a web browser, I then focussed on analysing the TCP traffic.

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/6fb6ec73-c9e8-4975-8112-4869570db932)

I coulnd't discern any differences between opening a browser and not having a browser open.




##  Learning/Reflection
On my research to complete this assignment, I came accross information from ChatGPT which stated that it's illegal to scan networks without proper authorisation, which made me wonder about all the legislation that governs data security in Europe.  This is an area that I have to develop and explore further as I find it very interesting and it gives structure to how businesses will structure their documentation, communication and procedures in case of cyber security breaches.  I anticipate that learning more about the legislation around European Data Protection and Cyber security will provide a good framework to understand this side of the tech industry.


