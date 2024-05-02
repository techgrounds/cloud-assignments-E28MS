## Subject

Azure Disk Storage can be seen as a virtual hard drive in the cloud. 

A disk can be an OS disk (where the OS is located) or a Data Disk (comparable to an external hard drive). 

You have a choice between Managed Disks and Unmanaged Disks. 

Unmanaged Disks are cheaper, but you need a Storage Account for them (and you have to manage the disk yourself). 

Managed Data Disks can be shared among multiple VMs, but that is a relatively new feature and there are some complexities involved. 

Backups of a Managed Disk can be made with Incremental Snapshots that only store the changes since the last snapshot. For an Unmanaged Disk, you can only take a 'regular' snapshot.

There are 5 managed disk types. Generally, it can be said that higher performance leads to higher costs. 

See https://learn.microsoft.com/en-us/azure/virtual-machines/disks-types for an up-to-date overview of the available disk types.

A disk can be encrypted for security. Disks can be made larger, but not smaller.

If you want to use an external device (including a Data Disk) on Linux, you need to mount it first.


## Assignment

1.  Start 2 Linux VMs. Ensure that you have SSH access to both.

2.  Create an Azure Managed Disk and attach it to both VMs simultaneously.

3.  On your first machine, create a file and place it on the Shared Disk.

4.  Check on the second machine if you can read the file. (Note: you may need to remount the disk on your 2nd VM)

5.  Take a snapshot of the disk and try to create a new Disk from it.

6.  Mount this new Disk and view the file.

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


###  *Diagram explaining different disk types*

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/5085d2b6-3318-4250-abc5-8a024982a189)


##  Resources

[Learn Microsoft Azure Disk Types](https://learn.microsoft.com/en-us/azure/virtual-machines/disks-types)

[Learn Microsoft Azure Attach a Disk to a Linux VM](https://learn.microsoft.com/en-us/azure/virtual-machines/linux/attach-disk-portal)

Chat GPT

[Learn Microsoft Azure Disks Performance](https://learn.microsoft.com/en-gb/azure/virtual-machines/disks-performance)

##  Difficulties

1.  I had to spend some time trying to figure out what I should choose when setting up the machines under the Disks tab, as I wasn't sure if this would affect trying to attach the disks later in the excercise.  I wanted to be as cost effective as possible but also ensure that I'm choosing the right performance metrics to get the assignment done.

2.  The second VM was created with a Public IP, which means additional costs can be incurred.  I wanted to remove this as I didn't think it was needed for this excercise:

   ![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/855e1d5e-c258-4425-8595-6addd85dd122

   ![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/3e2a5ba6-8897-417b-aa3f-0be45ee084c6)

   



##  Results

### *Here is the first of my VM's:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/4be3ded3-8a0c-4c3f-8520-19942ba101b0

###  *Here is the second of my VM's:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/3f60773b-2646-47e7-9beb-bf895ea4c451)


