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

### *maxShares:  

Azure shared disks have property of maxShares value that signifies the maximum VMs that can be attached to a managed disk simultaneously. You need to enable the Azure shared disks feature on the disk using Azure portal or Azure command-line interface. When enabling the feature, set maxShares=2.

### *partitioning*
Partitioning is the process of dividing a physical disk into multiple logical sections called partitions. Each partition acts as a separate storage unit with its own file system and can be managed independently. Partitioning allows you to organize and manage your data more efficiently, and it can also provide benefits such as improved performance and easier data management.

In the context of virtual disks in Azure, partitioning serves a similar purpose to physical disks, allowing you to logically organize and manage data within the virtual disk. Each partition within a virtual disk can function as an independent storage unit with its own file system.

Partitioning virtual disks in Azure can still provide benefits such as improved data organization, easier management, and potentially better performance. However, the underlying implementation and management of virtual disks are handled by the cloud provider's infrastructure, so you may not have direct access to low-level disk management features.


##  Resources

[Learn Microsoft Azure Disk Types](https://learn.microsoft.com/en-us/azure/virtual-machines/disks-types)

[Learn Microsoft Azure Attach a Disk to a Linux VM](https://learn.microsoft.com/en-us/azure/virtual-machines/linux/attach-disk-portal)

Chat GPT

[Learn Microsoft Azure Disks Performance](https://learn.microsoft.com/en-gb/azure/virtual-machines/disks-performance

[Learn Microsoft Azure Share a Disk](https://learn.microsoft.com/en-us/azure/virtual-machines/disks-shared)

[Learn Microsoft Linux Detach Disk](https://learn.microsoft.com/en-us/azure/virtual-machines/linux/detach-disk?wt.mc_id=searchAPI_azureportal_inproduct_rmskilling&sessionId=c4d234a90d5b4ce7818c8def8240ff60)

##  Difficulties

1.  I had to spend some time trying to figure out what I should choose when setting up the machines under the Disks tab, as I wasn't sure if this would affect trying to attach the disks later in the excercise.  I wanted to be as cost effective as possible but also ensure that I'm choosing the right performance metrics to get the assignment done.

2.  The second VM was created with a Public IP, which means additional costs can be incurred.  I wanted to remove this as I didn't think it was needed for this excercise:

   ![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/855e1d5e-c258-4425-8595-6addd85dd122

   ![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/3e2a5ba6-8897-417b-aa3f-0be45ee084c6)


3.  I wanted to enable sharing so I could attach the disk to both VM's but didn't have the option, as apparrently the disk has to be detached for this to be enabled:

   ![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/3703c263-d54d-45ab-9219-2c05dbbf05a4)

   So I tried to figure out if it was possible to do this another way or if I needed to detach the disk first.  I coudln't figure out a way to attach the disk to the second machine.  I also had the additional complication in that my first VM didn't have an IP address and would take additional time to troubleshoot how I would log into the VM without this information.  

4.  I decided to delete my work so far (insert grinding teeth, followed by resignation and determination!) and start with a clean slate, employing all the knowlegde I've gained so far in this assignment.


   First VM Deleted, including the attached data disk:

   ![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/1dd88f38-97d3-44c5-8d01-abc2268e6d22)

   Second VM deleted, including the IP address:

   ![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/550936c1-ecda-426a-8e62-18739d5e72d4)


5.  I had difficulty trying to mount the disk in my second VM.  So much trouble...I kept on troubleshooting



   


   



##  Results

###  *Here is how far I got with my first attempt.  I decided to delete the VM's and disk after I got so stuck that I couldn't unstick myself without a further significant investment of time.  I did however learn a lot and my second effort was significantly improved*

### 1.  *Here is the first of my VM's:*

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/4be3ded3-8a0c-4c3f-8520-19942ba101b0

###  *Here is the second of my VM's:*

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/3f60773b-2646-47e7-9beb-bf895ea4c451)

### 2.  *I created a managed disk in first VM:*

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/a0f2d269-1a82-4168-9e73-a23a7fc0c5a0)

##  *This is where I started from scracth again:*

###  1.  *First VM (second attempt):*



###      *Second VM created(Second attempt)*

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/3d6b13be-25a0-4531-8715-b7b03c196786)


###  2.  *I selected a Standard SSD disk:*

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/d1fd584f-ad7e-4782-87da-29ba73734828)

###  *And very importantlay, I enabled the 'shared disk' option under the Advanced tab:*

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/bea0388a-560a-4fd9-abf8-866df7a0655d)

###  *Shared disk succesfully created:*

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/34e096d8-c0be-4a86-97ff-fb7bcb525324)


###  3.  *I created a file on my first VM by first logging into my VM remotely and creating a directory to attach the file to.  Here I saved a .txt file in my disk:*

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/4212e073-bf36-4b8a-bfc6-b75cb6fe9a05)


###  4.  *Troubleshhooting to see why I can't mount the disk in my second VM after sucsessfully creating a mountpoint:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/3bff7b5a-1e8b-46fc-bc30-f5138cf2752c)








## Learning/Reflection

I feel like I spent too much time on this excercise and in hindsight, it would have been better to learn more about disk sharing before I started the excercise so I wouldn't have gotten so stuck and unable to change the disk settings.  However, it was also a good learning experience to really dig deep and learn more about how the disks work and also explore more areas of the VM's.  I am also happy to have had more experience in creating the VM's multiple times as I'm feeling more familiar with the process and the considerations into creating VM's.  I'm starting to reaslise the amount of thought that needs to go into the architecture and how this needs to be considered in relation to the use of the VM's.

I would like to become more familiar with the CLI in the VM's.  This is an area that I haven't practised recently and I think this is important to revisit.



