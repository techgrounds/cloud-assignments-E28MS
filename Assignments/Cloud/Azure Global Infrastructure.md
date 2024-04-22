## Subject

##  Assignment
Study:

What is an Azure Region?

What is an Azure Availability Zone?

What is an Azure Region Pair?

Why would you choose one region over another?

## Key Terms

Study:
What is an Azure Region?
What is an Azure Availability Zone?
What is an Azure Region Pair?
Why would you choose one region over another?

##  Resources

[Microsoft Learn Regions](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/azure-setup-guide/regions)

[Microfsoft Learn Availbility Zones](https://learn.microsoft.com/en-us/azure/reliability/availability-zones-overview?tabs=azure-cli)



##  Difficulties

##  Results

The concept behind having three availability zones in Azure is to provide high availability and flexibility for applications and services running in the cloud. Each availability zone is a physically separate data center within a region, with independent power, cooling, and networking infrastructure.

###  What is an Azure Region?
A region is a geographical area that contains one or more data centers. Each region is independent and has its own set of services, resources, and network infrastructure.

Azure offers two types of regions:

Recommended regions are suitable for most workloads.

Alternate regions aren't optimized for primary workloads. Instead, alternate regions are available only for backup or failover, or only for customers with a company presence within a defined country/region.



### What are Azure Availabilty Zones?

An availability zone is a physically separate data center within a region that is designed to be available and fault tolerant**.** Azure has at least three availability zones in each region and defined by unique name as "Zone 1" or "Zone 2".

Many Azure regions provide availability zones, which are separated groups of datacenters within a region. Availability zones are close enough to have low-latency connections to other availability zones. They're connected by a high-performance network with a round-trip latency of less than 2ms. However, availability zones are far enough apart to reduce the likelihood that more than one will be affected by local outages or weather. Availability zones have independent power, cooling, and networking infrastructure. They're designed so that if one zone experiences an outage, then regional services, capacity, and high availability are supported by the remaining zones. They help your data stay synchronized and accessible when things go wrong.

Datacenter locations are selected by using rigorous vulnerability risk assessment criteria. This process identifies all significant datacenter-specific risks and considers shared risks between availability zones.

The following diagram shows several example Azure regions. Regions 1 and 2 support availability zones.

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/fc74ec62-a0c1-4edf-a606-9bf7a82d14cb)


A paired region is a second region within the same geography as the primary region, which is paired with the primary region for disaster recovery purposes. The paired region is located far enough away from the primary region to ensure that it is not affected by the same disasters or events that could impact the primary region.

A cluster is a group of interconnected computers or servers that work together to provide a service or application. In Azure, a cluster can refer to a group of virtual machines or containers that are deployed together to provide a service or application. This means that if one availability zone goes down due to a disaster or other event, the other availability zones can continue to provide service, ensuring that your applications and services remain available.

###  Why would you choose one region over another?
When deciding on a region, it's a good idea to select a recommended region if you can, because of the following benefits:

Recommended regions typically have higher capacity. Because of the larger capacity, recommended regions can often support your long-term growth better than alternate regions can.

Lower costs. Many recommended regions provide lower costs for a range of Azure services. By using recommended regions, you might reduce your overall Azure bill.

Gain early access to the latest offerings. For example, AI capabilities and GPU resources are typically available in recommended regions sooner than in other regions. 
