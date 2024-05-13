
## Subject

Azure SQL Database is a cloud-based relational database service provided by Microsoft Azure. It allows users to create, manage, and scale relational databases in the cloud without worrying about the underlying hardware or infrastructure.


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/bc286fc9-ec82-48a6-925d-7877e5dfb371)


Useful questions to keep in mind during your research on the topics:

1.  What problem does X solve?
2.  What key terms are associated with X?
3.  How does X fit into / replace X in an on-premises setting?
4.  How can I combine X with other services?
5.  What is the difference between X and other similar services?
6.  Where can I find this service in the console?
7.  How do I turn on this service?
8.  How can I connect this service to other resources?
    


## Assignment

Get some practical experience with Azure SQL Database.

I decided to the Quickstart excercise as below:

1.  Create a single database in Azure SQL Database using either the Azure portal, a PowerShell script, or an Azure CLI script. 

2.  You then query the database using Query editor in the Azure portal.

##  Key Terms

**What are Relational Databases?**

Imagine you have a bunch of data. This data could be anything: names, ages, addresses, orders, products, etc. 

Now, let's say you want to organize this data in a way that makes sense and is easy to manage. 

A relational database is like a super organized filing cabinet for your data. 

Instead of throwing everything into one big drawer, you divide your data into different tables. Each table is like a separate drawer, and each drawer holds related information.

For example, you might have a table for storing information about customers, another table for storing products, and another for storing orders. 

Each table has columns (like labels on folders) to specify what kind of information goes in each row (like pieces of paper inside the folder).

The magic of relational databases is that you can connect these tables together using relationships. 

For instance, you can link a customer to their orders by using a unique identifier, like a customer ID. This way, you can easily see which orders belong to which customers.

So, in simple terms, a relational database is like a structured way of organizing and connecting pieces of information, making it easier to store, manage, and retrieve data for various purposes.


**Azure Portal:** This is the web-based interface where you can access and manage your Azure services, including Azure SQL Database. You'll use the Azure Portal to create, configure, and monitor your SQL databases.


**SQL Database:** In the context of Azure, this refers to a managed relational database service based on Microsoft SQL Server. It supports SQL queries and transactions, making it suitable for storing and retrieving structured data.


**Server:** In Azure SQL Database, a server is a logical container that hosts one or more databases. When you create a SQL database on Azure, you'll need to specify or create a server to host it.


**Elastic Pool:** An elastic pool is a collection of databases with a shared set of resources (such as CPU and memory). It's useful when you have multiple databases with varying and unpredictable resource usage patterns, as it allows you to optimize resource utilization and cost.


**Performance Tiers:** Azure SQL Database offers different performance tiers to cater to various workload requirements. These tiers are categorized based on factors like compute power, storage size, and features. Common tiers include Basic, Standard, and Premium.


**DTU (Database Transaction Unit):** DTU is a unit of measure for the performance level of an Azure SQL Database. It combines CPU, memory, and I/O into a single metric to simplify performance tuning. Different performance tiers offer varying numbers of DTUs.


**vCore:** In addition to DTU-based pricing, Azure SQL Database also offers a vCore-based pricing model. vCore represents a virtual CPU core in the underlying hardware infrastructure. With vCore-based pricing, you have more flexibility in configuring and scaling compute resources.


**Backups and Restore:** Azure SQL Database automatically performs backups of your data, allowing you to restore your database to a specific point in time or to a specific backup. This feature helps protect your data against accidental deletions or corruptions.


**Security:** Azure SQL Database provides various security features to protect your data, including network security, encryption at rest and in transit, role-based access control, and threat detection.


**High Availability:** Azure SQL Database ensures high availability by replicating your database across multiple servers and datacenters. This helps minimize downtime and ensures that your application remains accessible even in the event of hardware failures or maintenance activities.






##  Resources

[Learn Microsoft Quickstart : Create a single databse - Azure SQL Database](https://learn.microsoft.com/en-us/azure/azure-sql/database/single-database-create-quickstart?view=azuresql&tabs=azure-portal)


[Quickstart Azure SQL Database](https://learn.microsoft.com/en-us/azure/azure-sql/database/single-database-create-quickstart?view=azuresql&tabs=azure-portal)


[What is the Azure SQL Database?](https://learn.microsoft.com/en-us/azure/azure-sql/database/sql-database-paas-overview?view=azuresql)


[Azure SQL for Beginners](https://learn.microsoft.com/en-us/shows/azure-sql-for-beginners/)

[Azure SQL Database Connect](https://learn.microsoft.com/en-us/azure/azure-sql/database/connect-query-content-reference-guide?view=azuresql#libraries)



##  Difficulties

It was difficult to decide how much to do on this excercise, as there were several other things I would have liked to play around with including connecting the SQL DB to other resources like an Azure SQL Managed Instance.  

I would also have liked to have queried the DB with Python.

However, in the interest of time, I only completed the basic excercises in the Quickstart guide and I didn't have any difficulties with these.

##  Results

1.  Creating a single SQL Databse:

This is the Basic's Tab of creating my SQL Database

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/1ceb29b8-ab3f-4fc3-a44d-13dd256ff9be)


Here are the settings of the Configure option on the Basics Tab:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/3d1fc418-961b-4543-bfee-965dc5ebe061)


Networking Tab details:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/91c0a7f2-d97a-43c9-a7de-64ff01e9a5f0

Additional Settings:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/c7b1f3b6-892e-4da1-b1c2-61998706251b)

2.  Query the Database using Query Editor (preview):

I entered the following in the Query 1 screen:


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/0f6a0ffd-bab0-47f1-ab8b-84f0def426e3)


And it returned the data below:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/e4b208da-deb7-449f-aa06-ff400558c184)







##  Additional information:

The Azure portal provides a Workload environment option that helps to preset some configuration settings. 

These settings can be overridden. This option applies to the Create SQL Database portal page only. 

Otherwise, the Workload environment option has no impact on licensing or other database configuration settings.

*Choosing the development workload environment sets a few options, including:*

Backup storage redundancy option is locally redundant storage. 

Locally redundant storage incurs less cost and is appropriate for pre-production environments that do not require the redundance of zone- or geo-replicated storage.

Compute + storage is General Purpose, Serverless with a single vCore. By default, there is a one-hour auto-pause delay.

*Choosing the Production workload environment sets:*

Backup storage redundancy is geo-redundant storage, the default.
Compute + storage is General Purpose, Provisioned with 2 vCores and 32 GB of storage. This can be further modified in the next step.

##  Libraries

You can use various libraries and frameworks to connect to Azure SQL Database or Azure SQL Managed Instance. 

You can then build an app by using SQL Server on Linux or Windows, or a SQL Server container on Linux.

The following table lists connectivity libraries or drivers that client applications can use from a variety of languages to connect to and use SQL Server running on-premises or in the cloud. 

You can use them on Linux, Windows, or in containers, and use them to connect to Azure SQL Database, Azure SQL Managed Instance, and Azure Synapse Analytics.

