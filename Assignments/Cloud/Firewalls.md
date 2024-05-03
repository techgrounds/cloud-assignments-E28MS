## Subject

Since all resources in the cloud are always online, it's important to secure them against intentional and unintentional harmful traffic. Azure Firewall can protect VNets from this traffic. You can use the Firewall in various configurations within a subnet or in a hub-and-spoke network. A Firewall always has a public IP address where all incoming traffic should be directed and a private IP address where all outgoing traffic should go.

As you have learned earlier, there are two types of firewalls: stateless and stateful. Azure Firewall is a stateful firewall. Because Azure Firewall monitors all traffic in detail, it is a relatively expensive service. During the training, we will not use Azure Firewall but its cheaper alternative: Network Security Group (NSG).

##  Study:

###  a)  The difference between Basic and Premium Firewall.

Azure Firewall now supports *three different* versions to cater to a wide range of customer use cases and preferences.

*  Azure Firewall Premium is recommended to secure highly sensitive applications (such as payment processing). It supports advanced threat protection capabilities like malware and TLS inspection.
  
*  Azure Firewall Standard is recommended for customers looking for Layer 3–Layer 7 firewall and needs autoscaling to handle peak traffic periods of up to 30 Gbps. It supports enterprise features like threat intelligence, DNS proxy, custom DNS, and web categories.
  
*  Azure Firewall Basic is recommended for SMB customers with throughput needs of 250 Mbps.

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/95dfc817-4cb5-4fc8-b593-c9f12763139d)

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/d60c9dac-89ce-4f32-b997-375a3e4d1f80)



###  b)  The difference between a Firewall and a Firewall Policy.

Firewall Policy is a top-level resource that contains security and operational settings for Azure Firewall. You can use Firewall Policy to manage rule sets that the Azure Firewall uses to filter traffic.

###  c)  That Azure Firewall is much more than just a firewall.

Azure Firewall is a scalable, intelligent firewall service in Azure that provides east-west and north-south traffic inspection, filtering, and monitoring. 

Azure Firewall inspects traffic on Layers 3 to 7 and can alert and deny traffic in real time from/to known malicious IP addresses and domains.

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/6331ec6c-68f9-420a-b778-d6b4d56c430e)


###  d)  The difference between Azure Firewall and NSG.

NSGs are basic firewall services that filter traffic at Layers 3 and 4 of the OSI model. 

Azure Firewall, in comparison, is a managed firewall service that filters and analyzes traffic at Layers 3, 4, and 7 of the OSI model. 

The tables below lay out many areas of comparison for the two solutions.





Azure Firewall and Network Security Groups are Azure security services to secure and control inbound and outbound traffic to and from Azure resources. 

They share a few common functionalities and differ in others, and they can work together to provide organizations with a “defense-in-depth” deployment in Azure. 

Use NSGs to control network traffic between Azure resources in a VNet, and use Azure Firewall on the network edge to control inbound and outbound traffic to and from the environment. 

Azure Firewall’s threat protection, IDPS, TLS inspection, URL filtering, and web categories features also provide enterprises with advanced security, flexible deployment, and streamlined protection. 






###  Network Security Group Deployments:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/c44dee0c-c1ce-4307-b010-64aeb07a55f3)


##  Requirements:

Your Azure Cloud environment.
Azure documentation.

## Assignment

1.  Deploy a web server. Ensure that ports for both SSH and HTTP are open.


2.  Create an NSG in your VNET. Ensure that your web server is still accessible via HTTP but that SSH is blocked.


3.  Test if your NSG is functioning.

##  Key Terms

*NSG = Network Security Groups*

An NSG is a group of security rules that filter inbound and outbound traffic to and from Azure resources based on a 5-tuple hash. 

Allow or deny decisions are processed in priority order based on these fields: Source, Source Port, Destination, Destination Port, and Protocol. 

These decisions apply to the traffic flow in and out of VNet subnets and network interface cards (NICs).



##  Resources

[Neovera Azure Firewall Difference between Basic and Premioum](https://neovera.com/azure-firewall/#:~:text=The%20main%20difference%20between%20Azure,names%20(FQDNs)%20and%20URLs.)

[Learn Microsoft Firewall Policy](https://learn.microsoft.com/en-us/azure/firewall/policy-rule-sets)

[CoreStack Azure Security Tools: Firewall vs NSG](https://www.corestack.io/azure-security-tools/azure-firewall-vs-nsg/)

[Learn Microsoft Network Security Group](https://learn.microsoft.com/en-us/azure/virtual-network/manage-network-security-group?tabs=network-security-group-portal)



[Learn Microsoft Linux Secure Web Server](https://learn.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-secure-web-server)

##  Difficulties

##  Results

###  1.  During the creation of my new VM for this excercise, I added a cloud-init script to install the nginx web server:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/5ddad659-bbdc-451d-a050-a009db171b03)

###  Here the web server is succesfully installed and working:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/c3e930a9-75b3-403e-bc44-11ef29838e5b)

###  2.  Here I succesfully associated the NSG with the V-net:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/87ed8ee3-b5a2-4e04-a133-94449faac555)


### The inbound security rules indicated that SSH was still open, as well as HTTP:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/cbc12e5a-0bd3-4e68-9b8f-366a31f0e69e)

###   So I denied SSH access by adding a new Inbound Security Rule with a higher priority than the existing Inbound Security Rule that allows SSH access through port 22:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/e4f6a258-14b0-4664-87c8-c75459d9e937)


###  3.  In order to check if my NSG was working, I did the following:


##  a)  I checked my NSG settings and confirmed that the Inbound Security Rule denying SSH access has been prioritised over the SSH Inbound Security Rule that was allowing SSH access:  

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/2a2423af-db31-4088-bd6b-0bca640f34b2)

##  b) I tried to use SSH to connect to my remote VM and got a timed out error message, indicating that the SSH connection was not availalbe:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/bb5ecc6e-70d3-44ed-b504-9c820aac4fb3)








   



###  Bonus Section: Best Practices

Recommended Best Practices

1.  Deploy Azure Firewall on a central VNet and peer other VNets in a hub-and-spoke model. Set the default route from the peered VNets to point to Azure Firewall in the central VNet. This topology provides central management, streamlined security, and cost efficiency.

2.  Use Azure Firewall’s application rules where possible. For example, for HTTP/S or MSSQL traffic, use application rules for FQDN filtering. For Azure services (e.g., AzureBackup and HDInsight), use application rules with FQDN tags. For any other protocols, use network rules for FQDN filtering.

3.  Associate NSGs with subnets where possible, and associate NSGs with subnets and NICs in extreme scenarios. Avoid associating NSGs with subnets and NICs at the same time.
   
4.  Use Azure NSG Flow Logs in Azure Network Watcher to monitor NSG traffic for security, compliance, and performance and get alerts. Export logs to SIEM for analysis and diagnostics.

5.  Use logical naming convention on NSG security rules; use DNAT, network, and application rules in Azure Firewall. It helps a lot! 

6.  Leave space between rule priority numbers to accommodate future rules that may need precedence. This recommended best practice applies to NSG and Azure Firewall rules.
