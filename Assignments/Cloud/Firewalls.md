## Subject

Since all resources in the cloud are always online, it's important to secure them against intentional and unintentional harmful traffic. Azure Firewall can protect VNets from this traffic. You can use the Firewall in various configurations within a subnet or in a hub-and-spoke network. A Firewall always has a public IP address where all incoming traffic should be directed and a private IP address where all outgoing traffic should go.

As you have learned earlier, there are two types of firewalls: stateless and stateful. Azure Firewall is a stateful firewall. Because Azure Firewall monitors all traffic in detail, it is a relatively expensive service. During the training, we will not use Azure Firewall but its cheaper alternative: Network Security Group (NSG).

Study:

The difference between Basic and Premium Firewall.
The difference between a Firewall and a Firewall Policy.
That Azure Firewall is much more than just a firewall.
The difference between Azure Firewall and NSG.


Requirements:

Your Azure Cloud environment.
Azure documentation.

## Assignment

Deploy a web server. Ensure that ports for both SSH and HTTP are open.


Create an NSG in your VNET. Ensure that your web server is still accessible via HTTP but that SSH is blocked.


Test if your NSG is functioning.

##  Key Terms

##  Resources

##  Difficulties

##  Results
