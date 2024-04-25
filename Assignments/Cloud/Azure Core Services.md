## Subject

You can consider this document as a sort of guide to your AZ-900 certification. It contains the services you need to know in a bit more detail. 

Additionally, this document describes how to deal with the other services you may encounter in the (practice) exam.

There are many services in Azure, but some are more important than others. 

Azure mentions the following architectural components and services that you should know reasonably in-depth about what they do:

- Regions and Region Pairs
- Availability Zones
- Resource Groups
- Subscriptions
- Management Groups
- Azure Resource Manager
- Virtual Machines
- Azure App Services
- Azure Container Instances (ACI)
- Azure Kubernetes Service (AKS)
- Azure Virtual Desktop
- Virtual Networks
- VPN Gateway
- Virtual Network Peering
- ExpressRoute
- Container (Blob) Storage
- Disk Storage
- File Storage
- Storage Tiers
- Cosmos DB
- Azure SQL Database
- Azure Database for MySQL
- Azure Database for PostgreSQL
- SQL Managed Instance
- Azure Marketplace

Of course, there are many more services that may appear on your exam. For these services, it's enough to be familiar with the product page (see an example of an Azure product page here).

In addition to the services, you can also expect questions about various cloud concepts, such as High Availability, the consumption-based pricing model, and the shared responsibility model.

## Assignment

Study:

The Exam Guide for Microsoft Azure Fundamentals (AZ-900)


##  Key Terms

Architectural components - 

Services - 

Core Services - 

Physical Infrastructure - 

Resources  - 

##  Resources

[Azure Mentor AZ-900 Study Guide](https://github.com/AzureMentor/Azure-AZ-900-Study-Guide/blob/master/1-Describe%20cloud%20concepts%20(25%E2%80%9330%25).md)

[Splunk Azure Core Services](https://www.splunk.com/en_us/blog/learn/microsoft-azure-services.html#:~:text=The%20core%20services%20of%20Azure,security%2C%20development%2C%20and%20integration

[Learn Microsoft Describe Core Architectural Components ](https://learn.microsoft.com/en-us/training/modules/describe-core-architectural-components-of-azure/5-describe-azure-physical-infrastructure)



##  Difficulties

It was difficult to understand at first how all the services can be grouped or divided.  Once I found the right resources, it helped me to structure it into 4 broad categories of Compute, Storage, Networking and Database.  

Another way to categorise it is services related to PaaS, IaaS and SaaS.

##  Results

In order to make sense of the assignment, I divided the list provided into architectural components and services to better understand how everything fits together:

### Architectural Components:
Regions and Region Pairs
Availability Zones
Resource Groups
Subscriptions
Management Groups
Azure Resource Manager
Virtual Networks
Virtual Network Peering
ExpressRoute

###  Services:
Virtual Machines
Azure App Services
Azure Container Instances (ACI)
Azure Kubernetes Service (AKS)
Azure Virtual Desktop
VPN Gateway
Container (Blob) Storage
Disk Storage
File Storage
Storage Tiers
Cosmos DB
Azure SQL Database
Azure Database for MySQL
Azure Database for PostgreSQL
SQL Managed Instance
Azure Marketplace

###   Azure compute services
Azure compute services enable organizations to deploy, manage, and scale applications and workloads in the cloud. Here are some of the core compute services provided by Azure.

*  Azure App Service - Allows easy creation, deployment, and scaling of web applications and APIs using .NET, .NET Core, Node.js, Java, Python, or PHP languages and running in containers, Windows, or Linux.
  
*  Azure Functions - A serverless platform that simplifies development using any programming language, allowing faster development.
  
*  Container Instances - Provide a way to run containers without managing the underlying infrastructure. They allow you to launch containers on Azure without setting up and managing a container orchestration platform.
  
*  Virtual Machines (VMs) -  Allow you to create and run Windows or Linux virtual machines in the cloud.
  
  ###  Azure storage services
Azure storage provides scalable and secure storage options for organizations. A few examples are as follows:

*Azure Data Lake Storage* - Designed for big data analytics workloads. It allows for storing and analyzing large volumes of structured, semi-structured, and unstructured data.

*  HPC Cache - Enables caching data for high-performance computing (HPC) workloads. It is specifically designed to enhance performance and reduce latency for compute-intensive applications.
*  Managed Disks - Provides high-performance block storage for critical Azure Virtual Machines and Azure VMware Solution applications. It offers various disk options for optimized costs and performance, including Ultra Disk Storage, Premium SSD, Standard SSD, and Standard HDD. 

### Azure database services
Provides managed databases to simplify the deployment, management, and scaling of databases in the cloud. Here are some of the core database services provided by Azure.

*  Apache Cassandra MI - Enables cost-effective scaling of mission-critical workloads, offering flexible management and high availability.
*  Azure Cosmo DB - A fully managed serverless distributed database that supports PostgreSQL, MongoDB, and Apache Cassandra.
*  Redis Cache - Provides in-memory storage for faster data access.
*  Azure Database for MySQL - A cost-effective solution comes with advanced security, high availability options, and a reliable SLA.
  
### Azure Networking Services
Azure Networking Services provide networking solutions for organizations to build, manage, and secure their network infrastructure in the Azure cloud environment. Following are some of the core networking services provided by Azure.

*  Application Gateway
 The Azure Application Gateway has features like a web application firewall, integration with various Azure services, end-to-end SSL encryption, layer seven intelligent routing, SSL offload, and centralized certificate management.
*  Azure DNS - Provide DNS hosting capabilities.
*  ExpressRoute - Allows private connections between Azure data centers and on-premises or colocation infrastructure. 
*  Private Link - Helps establish secure and private connections between virtual networks and Azure PaaS, customer-owned or Microsoft partner services, enhancing network security and simplifying architecture.
