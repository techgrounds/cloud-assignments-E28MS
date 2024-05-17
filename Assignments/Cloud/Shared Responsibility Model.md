## Subject

If you manage your own data center, you are sure that you are responsible for everything: from physical security to the security and encryption of your data. But also the maintenance and management of the building where your data center is located and all the personnel needed for that.

In the Cloud, many of these responsibilities are taken over. The Cloud Provider is then responsible for the physical aspects of your infrastructure. You, as a customer, can rent this infrastructure without having to worry about it.

However, this is not a free pass. You, as a customer, are still responsible for what you do on this rented infrastructure. These responsibilities include access management to data and software, encryption of data at rest and data in transit.

The number of responsibilities that lie with the customer also depends on the type of service being used. However, there are still responsibilities that always lie with the customer.

The Cloud provider offers additional services to make it easier for you to manage your own responsibilities.

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/7c38817d-93bc-4cb2-b486-6c54e92c2bb8)


## Assignment

Study the Azure Shared Responsbility Model

##  Key Terms

##  Resources

[Azure Security Shared Responsibility](https://learn.microsoft.com/en-us/azure/security/fundamentals/shared-responsibility)

##  Difficulties

##  Results

The Shared Responsibility Model is a fundamental concept in cloud computing, outlining the division of responsibilities between the cloud service provider (CSP) and the customer. For Azure specifically, understanding this model is crucial, especially for those preparing for the AZ-900 exam, as it forms the basis for ensuring the security and compliance of cloud deployments.

### Overview:

In Azure's Shared Responsibility Model, responsibilities are divided between Microsoft as the cloud service provider and the customer. Microsoft manages the security *of* the cloud, while customers are responsible for security *in* the cloud.

### Key Points:

1. **Microsoft's Responsibilities:**
   - Physical security of data centers.
   - Network infrastructure security.
   - Availability of services.
   - Compliance certifications.

2. **Customer's Responsibilities:**
   - Data protection and encryption.
   - Identity and access management.
   - Application-level security.
   - Compliance with regulatory requirements.

### Questions & Answers:

1. **Q: What aspects of security does Microsoft manage in Azure?**
   - A: Microsoft manages physical security, network security, and availability of services.

2. **Q: What are some examples of customer responsibilities in Azure?**
   - A: Customer responsibilities include data encryption, identity management, and application security.

3. **Q: Why is it important for customers to understand their responsibilities in Azure?**
   - A: Understanding responsibilities ensures that customers implement necessary security measures to protect their data and comply with regulations.

### Use Cases:

1. **Data Encryption:**
   - Example: A company stores sensitive customer information in Azure. Implementing encryption ensures that even if unauthorized users gain access to the data, they cannot read it without the encryption key.

2. **Identity Management:**
   - Example: By configuring Azure Active Directory correctly, a company can ensure that only authorized employees have access to Azure resources, reducing the risk of unauthorized access.

3. **Compliance Requirements:**
   - Example: A healthcare organization using Azure must ensure compliance with regulations like HIPAA. Understanding their responsibilities helps them implement the necessary controls to maintain compliance.

### Conclusion:

Understanding the Shared Responsibility Model in Azure is essential for ensuring the security and compliance of cloud deployments. By knowing what Microsoft manages and what customers are responsible for, organizations can effectively secure their data and applications in the cloud.

This overview should provide you with a solid foundation for studying the Shared Responsibility Model in Azure as you prepare for the AZ-900 exam.
