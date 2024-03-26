## Subject : Networking Protocols

Protocols are used to perform one of three main functions: communication, security and network management.  Essentially, network protocols are a set of established rules that determines how data is transmitted between different devices on a network.

It enables different devices to communicate with each other despite differences in the devices by making use of pre-determined rule (protocols) in their hardware of software.


## Assignment
1.  Identify several other protocols and their associated OSI layer. Name at least one for each layer.


2.  Figure out who determines what protocols we use and what is needed to introduce your own protocol.


3.  Look into wireshark and install this program. Try and capture a bit of your own network data. Search for a protocol you know and try to understand how it functions.

## Key Terms

TCP/IP model- The Transmission Control Protocol/Internet Protocol has 4 layers.  It is widely used to reliably deliver data from host to client.

TCP - In laymens terms, it works as follows: The data is broken into smaller 'packets' by TCP.  Each packet is numbered to ensure that they arrive in good order.  A 'checksum' is added to each packet to ensure that they are not altered en route.  Lastly, each packet is given it's origin and destination addresses so it can be appropriately routed.  The destination addressed are where IP addresses come in, as each device on the internet has a unique IP address.  Once the packets arrive, they are re-assembled for viewing by TCP.

UDP

SSH

HTTP

OSI - Open Systems Interconnection model



Wireshark - This is a network packet analyser.  It can be used to analyse what is happening inside a network.  It is free and open source and claims to be one of the best packet anaylysers on the market. 


## Resources

[InfoSys Beckhoff](https://infosys.beckhoff.com/english.php?content=../content/1033/tf6310_tc3_tcpip/84246923.html&id=)


[Wireshark Docs](https://www.wireshark.org/docs/wsug_html_chunked/ChapterIntroduction.html#ChIntroWhatIs)

[Comptia](https://www.comptia.org/content/guides/what-is-a-network-protocol#:~:text=Network%20protocols%20are%20typically%20created,Internet%20Engineering%20Task%20Force%20(IETF))

[How do you create network protocols?](https://www.linkedin.com/advice/3/how-do-you-create-network-protocols-work-any)

[Geeks for Geeks](https://www.geeksforgeeks.org/network-protocols-and-proxies-in-system-design/#commonly-used-network-protocols-in-system-design)


## Difficulties

Understanding the wealth of information relayed by Wireshark proved a challenge.  Over 3000 protocols can be analysed. 


## Results

OSI Layers with corresponding protocols per layer:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/fdb6a016-8401-4492-b684-a514e5a4c83e)


The use of protocols for networking are determined by formal institutions and are designed according to industry standards.  This is crucial if you consider that networking protocols enable easy communication internationally.    Here are some of the more prominent institutions that have created and published networking protocols that are used internationally :


The Institute of Electrical and Electronics Engineers (IEEE)


The Internet Engineering Task Force (IETF)


The International Organization for Standardization (ISO)


The International Telecommunications Union (ITU)


The World Wide Web Consortium (W3C


Information captures with Wireshark:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/58ff8aed-32d4-4880-aed8-1ea659bcf275)









## Learning/Reflection

I enjoyed learning more about how the OSI stack and TCP/IP protocols work.  I also learnt about other protocols I haven't studied before like UDP.
