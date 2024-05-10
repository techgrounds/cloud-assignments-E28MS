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


##  Assignment:

Gain practical experience with:

A)  Azure Files



##  Key Terms

In the context of Azure Files, NFS, SMB, and FTP are protocols or technologies used for accessing and managing files stored in Azure file shares. Here's a brief explanation of each:

1. **NFS (Network File System)**:
   - NFS is a distributed file system protocol commonly used in Unix-like operating systems for sharing files and directories over a network. It allows multiple clients to access files stored on a remote server as if they were local files. While Azure Files primarily supports the SMB protocol, NFS 3.0 and NFS 4.1 support for Azure Files is available in preview. NFS access allows Unix-based clients to access Azure file shares directly using NFS protocols.

2. **SMB (Server Message Block)**:
   - SMB is a network file sharing protocol primarily used in Windows-based environments. It enables clients to access shared files, printers, and other resources on a network. Azure Files natively supports the SMB protocol, allowing Windows-based clients to mount Azure file shares as network drives and access files and folders stored in Azure Storage.

3. **FTP (File Transfer Protocol)**:
   - FTP is a standard network protocol used for transferring files between a client and a server on a computer network. It provides a simple and efficient way to upload, download, and manage files across a network. While Azure Files does not support FTP natively, it's possible to use third-party FTP clients or solutions to access files stored in Azure file shares by mounting them as network drives or using Azure Blob Storage's FTP support in conjunction with Azure Files.

The above 3 protocols serve as communication channels between clients and Azure Files, enabling users and applications to access and manipulate files stored in Azure file shares according to their specific requirements and compatibility with different operating systems and applications.

4. **Azure Files**:
   - Azure Files is a fully managed file share service in Microsoft Azure, providing shared file storage in the cloud.
    
5. **Storage Account**:
   - A storage account is a Microsoft Azure resource that provides a unique namespace to store and access data objects in Azure Storage. Azure Files are stored within storage accounts.

6. **File Share**:
   - A file share is a container within a storage account that provides SMB (Server Message Block) access to files and folders. Azure Files are organized into file shares.

7. **SMB (Server Message Block)**:
   - SMB is a network protocol used for file and printer sharing in Windows-based environments. Azure Files support SMB, allowing access to file shares from Windows, macOS, and Linux operating systems.

8. **Mounting**:
   - Mounting refers to the process of connecting and making a file share accessible as a network drive on a local machine or virtual machine. Azure Files can be mounted on various platforms for easy access.

9. **Access Control**:
   - Access control involves defining permissions and security settings to regulate who can access Azure file shares and what actions they can perform (e.g., Read, Write, or both).

10. **Storage Redundancy**:
   - Storage redundancy refers to the replication and distribution of data across multiple storage nodes to ensure data durability and availability. Azure Files offer options for redundancy, including locally redundant storage (LRS) and zone-redundant storage (ZRS).

11. **REST API**:
   - The REST API (Representational State Transfer Application Programming Interface) is a set of rules and conventions for building web services that allow clients to interact with cloud storage resources programmatically. Azure Files can be managed and accessed using the Azure Storage REST API.

12. **Azure Active Directory (AAD) Integration**:
   - Azure Active Directory integration enables authentication and authorization of users and applications accessing Azure Files. It allows organizations to leverage their existing identity management infrastructure for accessing file shares securely.

13. **Storage Explorer**:
    - Azure Storage Explorer is a standalone application that enables users to manage Azure Storage resources visually. It provides a user-friendly interface for browsing, uploading, downloading, and managing files and folders in Azure Files.

14.  ** Port 445**

Port 445 is a Microsoft networking port which is also linked to the NetBIOS service present in earlier versions of Microsoft Operating Systems. 

It runs Server Message Block (SMB), which allows systems of the same network to share files and printers over TCP/IP.

This port shouldn't be opened for external network. All microsoft devices mostly have port 445 open as the port is used for LAN communication.


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




First I created a Storage Account:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/7447f148-9afa-4c5e-a145-949f207b06f5)


Next I created an Azure File Share:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/46fd9122-fe50-4850-80ca-ce25fd7042fc)


Followed by creating a Directory:








