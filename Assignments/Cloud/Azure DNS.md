## Subject
Azure DNS is a hosting service for DNS domains that provides name resolution by using Microsoft Azure infrastructure.

By hosting your domains in Azure, you can manage your DNS records using the same credentials, APIs, tools, and billing as your other Azure services.

## Benefits of Azure DNS

Azure DNS leverages the scope and scale of Microsoft Azure to provide numerous benefits, including:

### Reliability and Performance

DNS domains in Azure DNS are hosted on Azure's global network of DNS name servers, providing resiliency and high availability. Azure DNS uses anycast networking, so each DNS query is answered by the closest available DNS server to provide fast performance and high availability for your domain.

### Security

Azure DNS is based on Azure Resource Manager, which provides features such as:

- **Azure role-based access control (Azure RBAC)** to control who has access to specific actions for your organization.
- **Activity logs** to monitor how a user in your organization modified a resource or to find an error when troubleshooting.
- **Resource locking** to lock a subscription, resource group, or resource. Locking prevents other users in your organization from accidentally deleting or modifying critical resources.

### Ease of Use

Azure DNS can manage DNS records for your Azure services and provide DNS for your external resources as well. Azure DNS is integrated in the Azure portal and uses the same credentials, support contract, and billing as your other Azure services.

Because Azure DNS is running on Azure, it means you can manage your domains and records with the Azure portal, Azure PowerShell cmdlets, and the cross-platform Azure CLI. Applications that require automated DNS management can integrate with the service by using the REST API and SDKs.

### Customizable Virtual Networks with Private Domains

Azure DNS also supports private DNS domains. This feature allows you to use your own custom domain names in your private virtual networks, rather than being stuck with the Azure-provided names.

**Example**:
- Imagine you have a private network in Azure for your company, and within this network, you have several internal applications and services.
- Instead of accessing these services with long, complex Azure-generated names, you can use your own domain names. For instance, you can access your internal email server with `mail.companyname.internal` instead of some complicated Azure-assigned name.

### Alias Records

Azure DNS also supports alias record sets. You can use an alias record set to refer to an Azure resource, such as an Azure public IP address, an Azure Traffic Manager profile, or an Azure Content Delivery Network (CDN) endpoint. If the IP address of the underlying resource changes, the alias record set seamlessly updates itself during DNS resolution. The alias record set points to the service instance, and the service instance is associated with an IP address.

**Example**:
- Let's say you have a web application hosted on an Azure virtual machine with a public IP address. You can create a DNS alias record for `www.mywebsite.com` that points to this virtual machine.
- If for some reason the public IP of your virtual machine changes (maybe you redeployed the VM or made changes to your infrastructure), the alias record will automatically update to the new IP address. Your users can still access `www.mywebsite.com` without any disruption or need for manual updates.

> **Important**: You can't use Azure DNS to buy a domain name. For an annual fee, you can buy a domain name by using App Service domains or a third-party domain name registrar. Once purchased, your domains can be hosted in Azure DNS for record management.

## Assignment
The objective of this assignment is to provide you with foundational knowledge about Azure DNS. This will help you understand the concepts required for the AZ-900: Microsoft Azure Fundamentals exam.

## Key Terms
1. **DNS (Domain Name System)**: A hierarchical and decentralized naming system for computers, services, or other resources connected to the internet or a private network.
2. **Azure DNS**: A hosting service for DNS domains, providing name resolution using Microsoft Azure infrastructure.
3. **DNS Zone**: A container for DNS records for a specific domain. It allows you to manage and configure DNS settings.
4. **DNS Record**: An entry in a DNS zone file that specifies mappings between domain names and IP addresses or other resources.
5. **Name Server**: A server that handles requests to translate domain names into IP addresses.
6. **CNAME Record (Canonical Name Record)**: A DNS record that maps an alias name to a true or canonical domain name.
7. **A Record (Address Record)**: A DNS record that maps a domain name to an IPv4 address.
8. **AAAA Record**: A DNS record that maps a domain name to an IPv6 address.
9. **MX Record (Mail Exchange Record)**: A DNS record that specifies the mail servers responsible for receiving email messages on behalf of a domain.
10. **TTL (Time to Live)**: The duration in seconds that a DNS record is cached by a DNS resolver.

## Resources
1. **Microsoft Learn - Introduction to Azure DNS**: [Azure DNS Documentation](https://docs.microsoft.com/en-us/azure/dns/dns-overview)
2. **Azure Fundamentals Learning Path**: [Microsoft Learn](https://docs.microsoft.com/en-us/learn/paths/azure-fundamentals/)
3. **AZ-900 Exam Skills Outline**: [Microsoft Certification](https://learn.microsoft.com/en-us/certifications/exams/az-900)
4. **Azure DNS Pricing**: [Azure Pricing Calculator](https://azure.microsoft.com/en-us/pricing/calculator/?service=dns)
5. **Azure DNS - How-To Guides**: [Microsoft How-To Guides](https://docs.microsoft.com/en-us/azure/dns/dns-how-to)

## Difficulties
1. **Understanding DNS Concepts**: Beginners may find it challenging to grasp how DNS works and its importance in the internet infrastructure.
2. **Configuring DNS Records**: Setting up and managing different types of DNS records (A, AAAA, CNAME, MX) can be confusing without practical experience.
3. **TTL Management**: Deciding appropriate TTL values for different records requires understanding the balance between performance and DNS propagation time.
4. **Azure Portal Navigation**: Navigating the Azure portal to manage DNS zones and records might be overwhelming for those new to Azure.


