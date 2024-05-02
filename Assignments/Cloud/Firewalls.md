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

###  d)  The difference between Azure Firewall and NSG.


Requirements:

Your Azure Cloud environment.
Azure documentation.

## Assignment

1.  Deploy a web server. Ensure that ports for both SSH and HTTP are open.


2.  Create an NSG in your VNET. Ensure that your web server is still accessible via HTTP but that SSH is blocked.


3.  Test if your NSG is functioning.

##  Key Terms



##  Resources

[Neovera Azure Firewall Difference between Basic and Premioum](https://neovera.com/azure-firewall/#:~:text=The%20main%20difference%20between%20Azure,names%20(FQDNs)%20and%20URLs.)

[Learn Microsoft Firewall Policy](https://learn.microsoft.com/en-us/azure/firewall/policy-rule-sets)



[Microsoft Learn

##  Difficulties

##  Results
