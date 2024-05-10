##  Subject

From this moment on, you will receive fewer concrete assignments. We will rely more on your independent learning skills. Don't worry, you're not alone. You have each other, and the established structure remains where you can still ask everyone for help.

Some services you only need to know theoretically. Others you should have turned on and configured at least once. Each topic describes whether it is a theoretical or practical subject.

Useful questions to keep in mind during your research on the topics:

1.  What problem does X solve?
2.  What key terms are associated with X?
3.  How does X fit into / replace X in an on-premises setting?
4.  How can I combine X with other services?
5.  What is the difference between X and other similar services?
6.  A handy list of tasks you need to be able to perform practically:

7.  Where can I find this service in the console?
8.  How do I turn on this service?
9.  How can I connect this service to other resources?
    
Requirements:

Your Azure environment

##  Assignment:
Gain practical experience with:

A)  Azure Files

B)  SQL Databases in Azure

C)  Azure App Service

D)  CosmosDB

    Gain theoretical knowledge of:
    
E)  Azure CDN

F)  Azure DNS

##  How I'm planning to structure my learning:

I requested that ChatGPT generate a tutorial for me on how to ensure that I complete this assignment as I wanted to make sure that I do it comprehensively: 

Understanding the Assignment:

The assignment requires you to gain practical experience with some Azure services while gaining theoretical knowledge of others.

Researching the Topics:
Start by understanding the purpose and functionality of each service listed in the assignment. Use the provided questions as guidelines for your research.
For practical services (Azure Files, SQL Databases in Azure, Azure App Service), focus on understanding how to use them, where to find them in the Azure portal, how to turn them on, and how to connect them to other resources.
For theoretical services (Azure CDN, Azure DNS), focus on understanding their roles, key terms, and how they integrate into Azure environments.

Practical Experience:
Begin by accessing the Azure portal and locating each service mentioned in the practical section.
Follow tutorials or documentation provided by Azure to turn on and configure each service at least once.
Experiment with connecting these services to other Azure resources to understand their integration capabilities.

Theoretical Knowledge:
Dive into documentation, tutorials, and other resources to understand the concepts behind Azure CDN and Azure DNS.
Focus on key terms, use cases, and differences from similar services.

Documentation and Troubleshooting:
Throughout your exploration, refer to Azure documentation for each service for detailed guidance.
If you encounter any issues or have questions, utilize community forums, Azure support, or peers for assistance.

Review and Reflection:
Once you've completed the practical tasks and gained theoretical knowledge, review your understanding of each service.
Reflect on how you can apply this knowledge in real-world scenarios or in your current or future projects.

Completion:
Once you feel confident in your understanding and have gained practical experience with the required services, you've completed the assignment.



###  



## Resources

###  A) Azure Files Resources

[Microsoft Learn Introduction to Azure Files](https://learn.microsoft.com/en-us/azure/storage/files/storage-files-introduction)

ChatGPT

[Azure Files ](https://www.youtube.com/watch?v=BCzeb0IAy2k&ab_channel=AdamMarczak-AzureforEveryone)

###  F) Azure DNS

[Learn Microsoft DNS Overview](https://learn.microsoft.com/en-us/azure/dns/dns-overview)

ChatGPT



###  


##  Difficulties

It proved challenging to make a decision about how to structure this .md file to reflect my learning and what I have achieved.  

It felt like a lot of information to try and replicate in a logical and tidy order.  I decided to structure it as much as possible for ease of reference and to ensure that I cover all the areas I wanted 


##  Results

###  A)  Files

I decided to complete the following 2 excercises to familiarise myself with Azure Files:

### Exercise 1: Setting Up and Accessing an Azure File Share

**Objective:** Create an Azure file share, mount it on a virtual machine, and access it from your local machine.

**Steps:**

1. **Create a Storage Account:**
   - Sign in to the Azure portal and navigate to the Azure Storage Accounts service.
   - Create a new storage account or use an existing one.

2. **Create a File Share:**
   - Within your storage account, navigate to the File Shares section.
   - Create a new file share with a unique name and desired quota size.

3. **Set Access Control:**
   - Define access control rules for the file share, specifying who can access it and with what permissions (e.g., Read, Write).

4. **Mount the File Share on a Virtual Machine:**
   - Provision a Windows or Linux virtual machine in Azure (or use an existing one).
   - Connect to the virtual machine using Remote Desktop Protocol (RDP) or Secure Shell (SSH).
   - Mount the Azure file share as a network drive or file system on the virtual machine.

5. **Access the File Share:**
   - Navigate to the mounted drive or file system on the virtual machine.
   - Create, upload, download, and manage files and folders as needed.
   
6. **Access the File Share from Your Local Machine:**
   - Install the Azure Storage Explorer or use the Azure portal to access the file share from your local machine.
   - Connect to the file share using the provided connection information.
   - Upload, download, and manage files and folders from your local machine.

### Exercise 2: Implementing File Share Backup and Restore

**Objective:** Configure backup and restore procedures for an Azure file share to ensure data resilience and recoverability.

**Steps:**

1. **Enable Azure File Share Soft Delete:**
   - Navigate to the Azure Storage Account containing your file share.
   - Enable Soft Delete for Azure file shares to retain deleted files and snapshots for a specified retention period.

2. **Configure Azure File Share Snapshot:**
   - Create a snapshot of your Azure file share to capture its current state.
   - Verify that the snapshot is available in the Azure portal or using Azure Storage Explorer.

3. **Implement Regular Backup Policy:**
   - Set up a backup policy to automatically create snapshots of your file share at regular intervals (e.g., daily, weekly).
   - Configure retention settings to retain snapshots for an appropriate duration.

4. **Test File Share Restore:**
   - Simulate data loss or corruption by deleting or modifying files within the file share.
   - Restore the file share from a snapshot or backup using Azure Storage Explorer or Azure PowerShell.

5. **Verify Data Integrity:**
   - Validate that the restored file share contains the correct data and that files are accessible and intact.

#  E) Azure CDN

# Azure CDN: Enhancing Content Delivery

## Introduction

Azure CDN is a content delivery network service provided by Microsoft Azure. 

It accelerates the delivery of web content, including images, videos, scripts, and stylesheets, by caching content at strategically distributed edge locations worldwide. 

By leveraging Azure CDN, you can improve the performance, scalability, and reliability of your web applications and deliver content to users with lower latency and higher throughput.

## Key Terms

To understand Azure CDN better, it's essential to be familiar with the following key terms:

1. **Content Delivery Network (CDN):** A distributed network of servers that delivers web content to users based on their geographic location, reducing latency and improving performance.

2. **Edge Location:** Data centers located near end-users that cache content and serve requests for cached content, reducing the distance and time required to deliver content to users.

3. **Origin Server:** The original server where web content is stored before being distributed to edge locations by the CDN.

4. **Cache Control:** Mechanisms used to control how long content remains cached at edge locations and when it should be refreshed from the origin server.

5. **HTTP/HTTPS Protocol:** The protocols used for transmitting data over the internet, with HTTPS providing secure communication via encryption.

6. **Purge:** The process of removing cached content from edge locations before its expiration time, typically used to update content or respond to content removal requests.

## Solving the Problem
Azure CDN addresses several challenges related to content delivery and performance optimization:

- **Improved Performance:** By caching content at edge locations closer to end-users, Azure CDN reduces the latency and time required to access web content, resulting in faster page load times and a better user experience.
- **Scalability:** Azure CDN scales automatically to handle increasing traffic and deliver content to users worldwide, ensuring consistent performance and availability even during traffic spikes.
- **Bandwidth Optimization:** By offloading traffic from origin servers and serving cached content from edge locations, Azure CDN reduces the bandwidth consumption and server load, resulting in cost savings and improved server performance.
- **Security:** Azure CDN supports HTTPS encryption, ensuring secure communication between users and the CDN, and provides features such as token authentication and origin protection to enhance security and prevent unauthorized access to content.

## Integration with On-Premises Settings
Azure CDN can be seamlessly integrated with on-premises environments in the following ways:

- **Origin Shield:** Azure CDN allows you to designate a central cache location (origin shield) that serves as the primary source of content for all edge locations, reducing the load on origin servers and improving cache hit ratios.
- **Custom Origin:** You can configure Azure CDN to fetch content from custom origin servers hosted on-premises, enabling you to leverage existing infrastructure and seamlessly integrate on-premises content with Azure CDN.

## Combining with Other Services
Azure CDN can be combined with various Azure services to enhance content delivery and improve performance:

- **Azure Blob Storage:** Integrate Azure CDN with Azure Blob Storage to accelerate the delivery of static assets such as images, videos, and documents stored in blob containers, improving the performance of web applications and reducing latency for end-users.
- **Azure App Service:** Use Azure CDN to cache dynamic content generated by Azure App Service web apps, such as HTML pages, API responses, and dynamic images, improving the scalability and responsiveness of web applications.
- **Azure Front Door:** Combine Azure CDN with Azure Front Door to implement advanced traffic management and optimization strategies, such as routing based on performance metrics, URL-based routing, and global load balancing, to optimize content delivery and improve the user experience.

## Comparison with Similar Services
While Azure CDN shares similarities with other content delivery networks, such as Amazon CloudFront and Google Cloud CDN, it offers several distinct advantages:

- **Integration with Azure Services:** Azure CDN seamlessly integrates with other Azure services, allowing you to manage and configure CDN settings alongside your other Azure resources from a unified interface.
- **Global Network Backbone:** Azure CDN leverages Microsoft's global network infrastructure, including over 200 edge locations worldwide, ensuring low-latency content delivery and high availability for users across regions.
- **Advanced Edge Optimization:** Azure CDN provides advanced edge optimization features, such as HTTP/2 support, dynamic site acceleration, and real-time analytics, to improve content delivery performance and enhance the user experience.

In conclusion, Azure CDN (X) is a powerful content delivery network service that accelerates content delivery, improves performance, and enhances scalability, making it an ideal choice for organizations looking to optimize their web applications and deliver content to users worldwide.

---

Let me know if there's anything else I can assist you with!

# F) Azure DNS

## Introduction
Azure DNS is a scalable Domain Name System (DNS) hosting service provided by Microsoft Azure. It enables you to manage your DNS records using Microsoft’s global network of DNS servers. By leveraging Azure DNS, you can efficiently resolve DNS queries for your domains and provide reliable and high-performance access to your web applications, services, and resources hosted on Azure or elsewhere.

## Key Terms
To understand Azure DNS better, it's essential to be familiar with the following key terms:

1. **Domain Name System (DNS):** A hierarchical decentralized naming system for computers, services, or other resources connected to the internet or a private network.

2. **Domain Registrar:** An organization that manages the reservation of internet domain names.

3. **DNS Zone:** A portion of the DNS namespace that is managed by an organization or administrator.

4. **Resource Record (RR):** A data record in the DNS that specifies the mapping between domain names and IP addresses or other information.

5. **Name Server:** A server that provides DNS services for a specific DNS zone.

6. **TTL (Time to Live):** A value in a DNS record that determines how long a resolver is supposed to cache the DNS query before refreshing it.

## Why use Azure DNS? (What problem does it solve?)

Azure DNS solves several challenges related to managing DNS records and providing reliable DNS resolution:

- **Scalability:** Azure DNS scales automatically to handle millions of queries per second, ensuring your applications remain accessible even under heavy loads.
- **Global Availability:** With a distributed network of name servers across Azure data centers worldwide, Azure DNS offers low-latency DNS resolution from anywhere in the world.
- **Simplified Management:** Azure DNS integrates seamlessly with other Azure services, allowing you to manage your DNS records alongside your other resources from a unified interface.
- **High Availability:** Azure DNS provides built-in redundancy and fault tolerance, reducing the risk of DNS failures and ensuring continuous availability for your applications.

## Integration with On-Premises Settings
Azure DNS can be seamlessly integrated with on-premises environments in the following ways:

- **DNS Forwarding:** You can configure your on-premises DNS servers to forward DNS queries for specific domains to Azure DNS, allowing you to leverage Azure's global network for DNS resolution.
- **Hybrid Cloud Connectivity:** Azure Virtual Network (VNet) allows you to establish secure connections between your on-premises network and Azure, enabling DNS resolution between on-premises resources and Azure-hosted services via Azure DNS.

## Combining with Other Services
Azure DNS can be combined with various Azure services to enhance functionality and streamline operations:

- **Azure Traffic Manager:** Integrate Azure DNS with Azure Traffic Manager to implement global load balancing and improve the availability and performance of your applications.
- **Azure App Service:** Use Azure DNS to map custom domain names to your Azure App Service web apps, enabling users to access your applications using memorable domain names.
- **Azure Private DNS:** Combine Azure DNS with Azure Private DNS to resolve DNS queries within your virtual networks and across Azure services without exposing DNS traffic to the public internet.

## Comparison with Similar Services
While Azure DNS shares similarities with other DNS hosting services, such as Amazon Route 53 and Google Cloud DNS, it offers several distinct advantages:

- **Integration with Azure Ecosystem:** Azure DNS seamlessly integrates with other Azure services, simplifying management and enabling deeper integration with your Azure infrastructure.
- **Global Network Backbone:** Azure DNS leverages Microsoft's global network infrastructure, ensuring low-latency DNS resolution and high availability for your applications worldwide.
- **Enterprise-grade Security:** Azure DNS provides advanced security features, such as DNSSEC (DNS Security Extensions) support, to protect against DNS-related attacks and unauthorized DNS modifications.

In conclusion, Azure DNS is a powerful DNS hosting service that offers scalability, reliability, and seamless integration with Azure services, making it an ideal choice for organizations looking to manage their DNS infrastructure effectively in the cloud.



##  Reflection/Learning

It was interesting to have to chart my own course and determine what I wanted to learn about each aspect that was specified in the assignment.  As the learning coach pointed out, this is to prepare for working in a team where you are responsible for your own learning.  

I enjoyed the challenge of it and from the beginning tried to set clear time goals per subject for myself.  I also built in a buffer for the inevevitable things that will require troubleshooting and that takes more time than estimated but I tried to be strict with the limits I set myself. 
