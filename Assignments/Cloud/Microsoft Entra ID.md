
## Subject
From this moment on, you will receive fewer concrete assignments. We will rely more on your independent learning skills. Don't worry, you're not alone. You have each other, and the established structure remains where you can still ask everyone for help.

Some services you only need to know theoretically. Others you should have turned on and configured at least once. Each topic describes whether it is a theoretical or practical subject.

Useful questions to keep in mind during your research on the topics:

What problem does X solve?

What key terms are associated with X?

How does X fit into / replace X in an on-premises setting?

How can I combine X with other services?

What is the difference between X and other similar services?

A handy list of tasks you need to be able to perform practically:

Where can I find this service in the console?

How do I turn on this service?

How can I connect this service to other resources?








## Assignment

Gain practical experience with:

Microsoft Entra ID

##  Key Terms


| Term or concept                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identity                           | A thing that can get authenticated. An identity can be a user with a username and password. Identities also include applications or other servers that might require authentication through secret keys or certificates.                                                                                                                                                                                                                                                                              |
| Account                            | An identity that has data associated with it. You can’t have an account without an identity.                                                                                                                                                                                                                                                                                                                                                                                                 |
| Microsoft Entra account            | An identity created through Microsoft Entra ID or another Microsoft cloud service, such as Microsoft 365. Identities are stored in Microsoft Entra ID and accessible to your organization's cloud service subscriptions. This account is also sometimes called a Work or school account.                                                                                                                                                                                                            |
| Account Administrator              | This classic subscription administrator role is conceptually the billing owner of a subscription. This role enables you to manage all subscriptions in an account. For more information, see Azure roles, Microsoft Entra roles, and classic subscription administrator roles.                                                                                                                                                                                                          |
| Service Administrator              | This classic subscription administrator role enables you to manage all Azure resources, including access. This role has the equivalent access of a user who is assigned the Owner role at the subscription scope. For more information, see Azure roles, Microsoft Entra roles, and classic subscription administrator roles.                                                                                                                                                     |
| Owner                              | This role helps you manage all Azure resources, including access. This role is built on a newer authorization system called Azure role-based access control (Azure RBAC) that provides fine-grained access management to Azure resources. For more information, see Azure roles, Microsoft Entra roles, and classic subscription administrator roles.                                                                                                                          |
| Microsoft Entra Global Administrator | This administrator role is automatically assigned to whomever created the Microsoft Entra tenant. You can have multiple Global Administrators, but anyone with at least Privileged Role Administrator can assign administrator roles to users. For more information about the various administrator roles, see Administrator role permissions in Microsoft Entra ID.                                                                                                                             |
| Azure subscription                 | Used to pay for Azure cloud services. You can have many subscriptions and they're linked to a credit card.                                                                                                                                                                                                                                                                                                                                                                                 |
| Tenant                             | A dedicated and trusted instance of Microsoft Entra ID. The tenant is automatically created when your organization signs up for a Microsoft cloud service subscription. These subscriptions include Microsoft Azure, Microsoft Intune, or Microsoft 365. This tenant represents a single organization and is intended for managing your employees, business apps, and other internal resources. For this reason, it's considered a workforce tenant configuration. By contrast, you can create a tenant in an external configuration, which is used in customer identity and access management (CIAM) solutions for your consumer-facing apps (learn more about Microsoft Entra External ID). |
| Single tenant                      | Azure tenants that access other services in a dedicated environment are considered single tenant.                                                                                                                                                                                                                                                                                                                                                                                          |
| Multitenant                        | Azure tenants that access other services in a shared environment, across multiple organizations, are considered multitenant.                                                                                                                                                                                                                                                                                                                                                                    |
| Microsoft Entra directory          | Each Azure tenant has a dedicated and trusted Microsoft Entra directory. The Microsoft Entra directory includes the tenant's users, groups, and apps and is used to perform identity and access management functions for tenant resources.                                                                                                                                                                                                                                                  |
| Custom domain                      | Every new Microsoft Entra directory comes with an initial domain name, for example domainname.onmicrosoft.com. In addition to that initial name, you can also add your organization's domain names. Your organization's domain names include the names you use to do business and your users use to access your organization's resources, to the list. Adding custom domain names helps you to create user names that are familiar to your users, such as alain@contoso.com.                                                                                                 |
| Microsoft account (also called, MSA) | Personal accounts that provide access to your consumer-oriented Microsoft products and cloud services. These products and services include Outlook, OneDrive, Xbox LIVE, or Microsoft 365. Your Microsoft account is created and stored in the Microsoft consumer identity account system that's run by Microsoft.                                                                                                                                                                                                |


SDK:

A Software Development Kit (SDK) is a collection of tools, libraries, documentation, and samples that developers use to create software applications for a specific platform or framework. 


SDKs are provided by software companies or platform owners to simplify and streamline the development process by providing essential resources and APIs.

##  Resources

[Microsoft External ID Tenant Setup](https://learn.microsoft.com/en-us/entra/external-id/customers/quickstart-tenant-setup)

[Microsoft Troubleshoot App Launch Failures](https://learn.microsoft.com/en-gb/dotnet/core/runtime-discovery/troubleshoot-app-launch?pivots=os-windows)

##  Difficulties

I planned to do the Quickstart for Microsoft Entra ID but when I looked at this, I realizied that in order to follow the Quickstart Guide for this, I would first need to create an external tenant.  So I adjusted my time allocation for this task accordingly and started with this crucial prerequisite.

I had a lot of trouble installing .NET.  From checksum's that didn't match to missing frameworks when I tried to run the app.  I kept troubleshooting and didn't give up and I finally succeeded in running the app.  It took perseverance and determination as I kept having the feeling that I'm spending precious learning time troubleshooting something that should have been simple. However, I chalked it up to learning a lot of cool new stuff and kept going.

##  Results


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/32374905-6d40-47c9-86e8-d16a953b1c1c)


###  First, I created a new tenant with external configurations:

I logged into the Micrsoft Entra Admin center and then I browsed to Identity > Overview > Manage tenants.  I selected the External option:


![alt text](image.png)


I changed the location on the Basics Tab and left the other options as default:


![alt text](image-1.png)


Here I changed the location:


![alt text](image-2.png)


When I tried to Create the tenant, I got an error message:


![alt text](image-3.png)


I was delighted that for once the error was obvious and easy to find and fix: the fields that appeared to me to have default values in were blank:


![alt text](image-4.png)

Once I filled in the missing values, the tenant creation was succesfully validated:


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/6850213a-ed56-44dc-9321-688d91735dac)

And I was able to navigate to my external tenant in the Microsoft Entra Admin Centre:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/dce2c5fc-3112-472d-9411-b4a74f159324)

###  Next, I customized the Sign-In Experience:

In Microsoft Entra Admin Centre, I browsed to Home>Tenant Overview>Start the Guide.

Next, I specified how I would like my customers to sign in and I chose Email and password, and then customised the log in screen by adding a logo and changing the background colour:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/6b426893-fc05-4368-bc51-f23f1fcbbaf6)


###  I tried out the Sign-Up experience and created my first user:

Here is a screenshot of my sign-in page:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/4b840faf-7e5c-47a4-9270-cfde6de0814f)

I received an email with a verification code :

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/0e1656cb-9830-4a54-81e1-d42602cb968a)



And here I've entered my details:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/bd4635c3-e8ed-4b27-bc71-3a26bbf952a7)

##  The following step was to Set Up a Sample App

I chose a Webb application in ASP.NET Core:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/5545f480-df55-45c9-8f03-a4e7140202e9)


Here I had downloaded .NET SDK, downloaded and unzipped the sample app and run the command **dotnet run** in my terminal and the app was being built:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/1bab0e19-26fd-4916-afa4-7f22c40b7da0)

When I tried to navigate to the webb app, I received a **This site can't be reached** error messsage and on inspecting my terminal output, noted that I had to download a missing framework, the version 7 that I skipped over in favour of version 8:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/1fdb6c68-0315-4886-98ac-4b0daaa3696e)

So I followed the prompts in the terminal and downloaded version 7 of .NET, unfortunately,this didn't resolve the issue:

https://learn.microsoft.com/en-gb/dotnet/core/runtime-discovery/troubleshoot-app-launch?pivots=os-windows

I had a look at the Microsoft Troubleshoot App Launch information and then decided to download Version 7 of .NET again and voila! It worked:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/e105e610-816c-46f1-b0d8-2ee546332c0b)

Instead of the error message, I now got a warning when I navigated to  **https://localhost:7274**  and on closer inspection I noted that the app still seemed to be building  :

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/b05dd958-3ea6-4827-9857-31321eca9fc8)

While the app was still building, I clicked through the Next button and got this message:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/ee669fb5-9160-4f17-9eff-272376f5714b)
















