## Subject

To store data in Azure, you need an Azure Storage Account.

In a Storage Account, all Azure Storage data objects such as blobs, files, disks, and tables are stored.

Data in a Storage Account is secure, highly available, durable, and massively scalable. 

All data in a Storage Account is accessible via the internet using HTTP and HTTPS. 

Because it's easily accessible, you need to ensure that only the correct identities have permissions to access the data. 

Azure Storage Explorer is a free GUI for managing your data in Azure. 

Many IaaS and PaaS services of Azure also utilize Azure Storage Accounts. Besides storing data, Blob Storage can also be used for hosting static websites.

Note: AWS has shared a static demo website with Techgrounds. Because it's nothing more than HTML, CSS, and JavaScript, it also works when hosted in Azure Blob Storage.

## Assignment

Assignment 1:

1.  Create an Azure Storage Account. Ensure that only you have access to the data.

2.  Place data in a storage service of your choice via the console (for example, a cat photo in Blob storage).
   
3.  Retrieve the data to your own computer using Azure Storage Explorer.

   
Assignment 2:

1.  Create a new container.
   
2.  Upload the 4 files that together form the AWS Demo Website. (note: this is an Azure assignment, but we are using the demo website from AWS. It's a simple combination of HTML, CSS, and JavaScript and does not have any cloud-specific functionalities)

3.  Ensure that Static Website Hosting is enabled.

4.  Share the URL with a teammate. Ensure that your teammate can view the website.

##  Key Terms

*Azure Storage*

Azure provides many ways to store your data, including multiple database options like Azure SQL Database, Azure Cosmos DB, and Azure Table Storage. 

Azure offers multiple ways to store and send messages, such as Azure Queues and Event Hubs. 

You can even store loose files using services like Azure Files and Azure Blobs.

Azure groups four of these data services together under the name Azure Storage. 

The four services are Azure Blobs, Azure Files, Azure Queues, and Azure Tables. The following illustration shows the elements of Azure Storage.

Illustration identifying the Azure data services that are part of Azure Storage.

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/b9109d6c-60c4-40cb-a666-314394abe214)


These four data services are all primitive, cloud-based storage services, and are often used together in the same application.

*Azure Storage Account*

A storage account is a container that groups a set of Azure Storage services together. 

Only data services from Azure Storage can be included in a storage account (Azure Blobs, Azure Files, Azure Queues, and Azure Tables). 

Combining data services into a single storage account enables you to manage them as a group. 

The settings you specify when you create the account, or any changes that you make after creation, apply to all services in the storage account. 

Deleting a storage account deletes all of the data stored inside it.

A storage account is an **Azure resource** and is part of a **resource group**. 

*The following illustration shows an Azure subscription containing multiple resource groups, where each group contains one or more storage accounts.*

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/bb5d29e3-d98a-416c-acc9-8407e08ac2ae)






Other Azure data services, such as Azure SQL and Azure Cosmos DB, are managed as independent Azure resources and can't be included in a storage account. The following illustration shows a typical arrangement: Blobs, Files, Queues, and Tables are contained within storage accounts, while other services aren't.

Illustration of an Azure subscription showing some data services that cannot be placed in a storage account.

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/ee9f3426-a9b7-40ef-8da6-a0524180569a)


##  Resources

[Learn Microsoft Create an Azure Storage Account](https://learn.microsoft.com/en-us/training/modules/create-azure-storage-account/)

[Learn Microsoft Storage Explorer Blobs](https://learn.microsoft.com/en-us/azure/storage/storage-explorer/vs-azure-tools-storage-explorer-blobs?toc=%2Fazure%2Fstorage%2Fblobs%2Ftoc.json&bc=%2Fazure%2Fstorage%2Fblobs%2Fbreadcrumb%2Ftoc.json)

##  Difficulties

When first I tried to create a Storage Account, I got an error message stating: ' Validation could not be completed due to an error. If this issue persists, please contact support.'

Screen shot of error message:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/227593ac-0cbf-47d1-8fc1-9dd9d0042b0f

I tried again and then it worked.

The second problem I encountered was that I wasnt' able to change my role in order to ensure that only I had access to the resource, so I ended up deleting my first attempt and starting again:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/3611c473-5074-4694-8a4c-7914c4636d92)


[Learn Microsoft Azure Blobs Assign Role Data Access ](https://learn.microsoft.com/en-us/azure/storage/blobs/assign-azure-role-data-access?tabs=portal)

I tried many different ways to give only myself access to the data in my Storage Account.  Eventually I changed the networking settings to give access only to specific IP addresses and this worked.  See 'Results' for details.





##  Results

###  Excercise 1

###  1.1  Screenshot of Create Storage Account :

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/1e59ce72-048b-4f48-bae8-ac28e667ab20)

###  Here my deployment of my Storage Account is complete:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/a6bbe76e-40fe-456a-8528-5d3512121ee8)

###  I was still unable to get access for only me to the data in the account until I changed the network setting as below:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/758b107b-e383-4f1b-b46f-18f1786854f6)

###  Here are the details of the Storage Account Set up:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/e97f124f-5420-4c10-a6c7-425c6ef8e175)

###  Here I added my IP address to the Firewall settings in my Storage Account:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/b8c9317c-527f-4b7d-9fd0-cf8991a8f007)


###  Here I accessed the data in my Storage Account to my computer from the Azure Storage Explorer app:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/e7e6ed4b-c0ad-4e3c-b883-25c04ecf4399)


### Excercise 2

###  Here I created another container called awsdemowebsite:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/66d00caf-0b32-45e4-97cb-2312e6ac69de)

###  Here I turned the Static Web Hosting on:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/1d239f9b-52d5-44b8-a42b-39a826bda6e9)


###  Here I set public read access for blobs only, using Azure Explorer:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/4f6670fa-c27b-4134-aa0e-b22761b9d567)

###  This didn't work, even after I tried refreshing.  The error message details wasn't clear, so I tried to set the access from my Azure portal instead and this worked:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/781c98fb-b4bd-4278-94b7-a6dd3cf5eae8)



###  This is the URL that finally lead to the static web page:

[Amazon Static Webpage](https://elmariesstorageaccount3.blob.core.windows.net/awsdemowebsite/index.html)

###  And here is a screenshot of the Amazon Static Webpage:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/b3f1731a-620d-4dbc-aad5-a3e93e257f9d)














