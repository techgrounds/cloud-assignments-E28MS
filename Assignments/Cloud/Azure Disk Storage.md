## Subject

## Assignment

##  Key Terms

###  *IOPS*

input/output operations per second (IOPS):  Your application's performance gets capped when it requests more IOPS or throughput than what is allotted for the virtual machines or attached disks.

When capped, the application experiences suboptimal performance. This can lead to negative consequences like increased latency. 

###  Here is a diagram expanding on the definition and implications of IOPS:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/475f52a7-dd0f-4d77-b87a-8a9beae17a01)


### *Standard HDD (Hard Disk Drive):*

Offers the lowest cost per GB.

Provides standard magnetic hard disk drives with rotational latency and slower read/write speeds compared to SSDs.

Suitable for workloads with low I/O requirements or where cost is a primary concern.

###  *Standard SSD (Solid State Drive):*

Offers better performance than HDDs with faster read/write speeds and lower latency.

Generally more expensive than HDDs but less expensive than Premium SSDs.

Suitable for general-purpose workloads that require better performance than HDDs but do not require the highest performance offered by Premium SSDs.

###  *Premium SSD:*
Provides the highest performance with low latency and high throughput.

Uses solid-state drives (SSDs) optimized for I/O-intensive workloads.

Offers the best performance for mission-critical applications, databases, and high-performance computing.

Generally more expensive than both Standard HDDs and Standard SSDs.

##  Resources

[Learn Microsoft Azure Attach a Disk to a Linux VM](https://learn.microsoft.com/en-us/azure/virtual-machines/linux/attach-disk-portal)

Chat GPT

[Learn Microsoft Azure Disks Performance](https://learn.microsoft.com/en-gb/azure/virtual-machines/disks-performance)

##  Difficulties

I had to spend some time trying to figure out what I should choose when setting up the machines under the Disks tab, as I wasn't sure if this would affect trying to attach the disks later in the excercise.

##  Results
