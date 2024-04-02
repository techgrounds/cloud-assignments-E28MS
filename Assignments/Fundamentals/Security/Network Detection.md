##  Subject

##  Key Terms
Nmap - 

##  Assignment

Scan the network of your Linux machine using nmap. What do you find?


Open Wireshark in Windows/MacOS Machine. Analyse what happens when you open an internet browser. (Tip: you will find that Zoom is constantly sending packets over the network. You can either turn off Zoom for a minute, or look for the packets sent by the browser between the packets sent by Zoom.)

##  Resources

##  Difficulties
The first time I tried scanning my VM, I got an error message saying the host may be down.  I resolved this by using the *-Pn* command, see screenshots in *Results*

##  Results

# Scanning VM's Network:

First attempts at scanning VM's network not succesful:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/0c89f5e7-beaf-4b9b-8fd8-865dcb1126a7)

Using the *-Pn* command enabled the VM to be scanned:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/16fa4bbd-3018-464c-b249-d6dc61e95c85)

I interpreted this information as follows:

The Nmap scan report indicates that the host (in this case, an EC2 instance on AWS) is up, but all 1000 scanned ports are in ignored states, and 1000 filtered TCP ports are not shown due to no response.


1. **Host is up**: This indicates that the target host (EC2 instance) is online and responsive to Nmap probes.

2. **All 1000 scanned ports are in ignored states**: This means that Nmap has determined that all 1000 scanned ports on the host are in an "ignored" state. An "ignored" state typically means that Nmap couldn't determine whether the port is open, closed, or filtered due to various reasons such as firewalls, network configurations, or Nmap timing settings.

3. **Not shown: 1000 filtered TCP ports (no-response)**: This part of the report indicates that Nmap did not show information about 1000 filtered TCP ports. Filtered ports are those where Nmap is unable to determine whether they are open or closed due to firewall filtering, packet filtering, or other reasons. In this case, Nmap received no response from these ports during the scan.

Overall, the scan report suggests that the target host, my VM,  is up and responsive, but the scan results for the ports are inconclusive due to being in ignored or filtered states. This could be due to various factors such as firewall configurations, network settings, or Nmap timing options.

# Analyze what happens when you open an internet browser

At first I tried to filter for http but this didn't bring up any traffic, possibly as I'm using a VPN, which encrypts and decripts data.  In order to see the traffic when I open a web browser, I then focussed on analysing the TCP traffic.

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/6fb6ec73-c9e8-4975-8112-4869570db932)




##  Learning/Reflection
On my research to complete this assignment, I came accross from ChatGPT which stated that it's illegal to scan networks without proper authorisation, which made me wonder about all the legislation that governs data security in Europe.  This is an area that I have to develop and explore further.


