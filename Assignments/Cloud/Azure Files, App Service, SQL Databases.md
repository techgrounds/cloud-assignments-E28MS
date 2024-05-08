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


##  Key Terms

### Files

In the context of Azure Files, NFS, SMB, and FTP are protocols or technologies used for accessing and managing files stored in Azure file shares. Here's a brief explanation of each:

1. **NFS (Network File System)**:
   - NFS is a distributed file system protocol commonly used in Unix-like operating systems for sharing files and directories over a network. It allows multiple clients to access files stored on a remote server as if they were local files. While Azure Files primarily supports the SMB protocol, NFS 3.0 and NFS 4.1 support for Azure Files is available in preview. NFS access allows Unix-based clients to access Azure file shares directly using NFS protocols.

2. **SMB (Server Message Block)**:
   - SMB is a network file sharing protocol primarily used in Windows-based environments. It enables clients to access shared files, printers, and other resources on a network. Azure Files natively supports the SMB protocol, allowing Windows-based clients to mount Azure file shares as network drives and access files and folders stored in Azure Storage.

3. **FTP (File Transfer Protocol)**:
   - FTP is a standard network protocol used for transferring files between a client and a server on a computer network. It provides a simple and efficient way to upload, download, and manage files across a network. While Azure Files does not support FTP natively, it's possible to use third-party FTP clients or solutions to access files stored in Azure file shares by mounting them as network drives or using Azure Blob Storage's FTP support in conjunction with Azure Files.

These protocols serve as communication channels between clients and Azure Files, enabling users and applications to access and manipulate files stored in Azure file shares according to their specific requirements and compatibility with different operating systems and applications.



## Resources

###  Azure Files Resources

[Microsoft Learn Introduction to Azure Files](https://learn.microsoft.com/en-us/azure/storage/files/storage-files-introduction)

ChatGPT

[Azure Files ](https://www.youtube.com/watch?v=BCzeb0IAy2k&ab_channel=AdamMarczak-AzureforEveryone)

###  


##  Difficulties

It proved challenging to make a decision about how to structure this .md file to reflect my learning and what I have achieved.  

It felt like a lot of information to try and replicate in a logical and tidy order.  I decided to structure it as much as possible for ease of reference and to ensure that I cover all the areas I wanted 


##  Results

###  Files

I decided to complete the following 2 excercises to familiarise myself with Azure Files:

Certainly! Here are two beginner-level exercises to complete with Azure Files, covering practical aspects that will help you understand the basics:

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

By completing these exercises, you'll gain hands-on experience with creating, accessing, and managing Azure file shares, as well as implementing backup and restore procedures to ensure data resilience and recoverability.

##  Reflection/Learning

It was interesting to have to chart my own course and determine what I wanted to learn about each aspect that was specified in the assignment.  As the learning coach pointed out, this is to prepare for working in a team where you are responsible for your own learning.  

I enjoyed the challenge of it and from the beginning tried to set clear time goals per subject for myself.  I also built in a buffer for the inevevitable things that will require troubleshooting and that takes more time than estimated but I tried to be strict with the limits I set myself. 
