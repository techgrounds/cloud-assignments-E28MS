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

##  Resources

[Learn Microsoft Create an Azure Storage Account](https://learn.microsoft.com/en-us/training/modules/create-azure-storage-account/)

##  Difficulties

##  Results
