## Subject

Azure Functions is a serverless computing service provided by Microsoft Azure that allows developers to build and deploy event-driven applications without the need to manage infrastructure. 

With Azure Functions, developers can focus solely on writing code to handle specific events, leaving the underlying infrastructure and scaling aspects to the Azure platform. 

This enables faster development, reduced operational costs, and enhanced scalability.

### Key Features of Azure Functions

**Event-driven Computing:**

Azure Functions are triggered by various events, such as HTTP requests, timers, messages in queues, file uploads, or changes to data in databases. This event-driven approach allows developers to respond to specific events in real-time without the need to maintain persistent server instances.


**Serverless Architecture:**

Azure Functions follows the serverless computing paradigm, meaning there are no servers to provision or manage. The platform automatically handles infrastructure scaling, ensuring resources are allocated based on the actual demand, making it highly cost-efficient.


**Language and Platform Support:** 

Azure Functions supports multiple programming languages, including C#, JavaScript, Java, Python, and TypeScript. This flexibility allows developers to work with their preferred language and leverage existing codebases seamlessly.


**Pay-as-You-Go Pricing:** 

Azure Functions offer a pay-as-you-go billing model. You only pay for the compute resources used during the execution of your functions. This cost-effective approach ensures you are charged only for the actual usage without any upfront commitments.


**Integration with Azure Services:** 

Azure Functions seamlessly integrate with various Azure services like Azure Storage, Azure Cosmos DB, Azure Service Bus, Azure Event Grid, and more. This integration allows developers to build sophisticated applications by combining the power of different services.

### Benefits of Using Azure Functions

**Faster Time to Market:**

With the ability to focus solely on business logic and event handling, developers can quickly build and deploy applications, reducing development time and accelerating time to market.

**Cost Savings:** 

As Azure Functions automatically scales based on demand, there’s no need to pay for idle server resources, resulting in cost savings, especially for applications with varying workloads.


**Scalability and Elasticity:** 

Azure Functions scales automatically to handle a large number of events concurrently. This elasticity ensures that your applications can handle high traffic and sudden spikes without any performance degradation.


**Serverless Management:** 

Microsoft Azure handles all the server management, including updates, security patches, and scaling, freeing developers from operational overhead and allowing them to focus on code development.


**Event-Driven Architecture:** 

The event-driven nature of Azure Functions enables the decoupling of application components, making it easier to build scalable and resilient microservices architectures.


##Types of Azure Functions##

**HTTP Trigger:** 

This type of function is triggered by an HTTP request. It can be used to build web APIs and handle HTTP-based interactions.


**Timer Trigger:** 

A timer trigger executes a function on a predefined schedule or at regular intervals. It is useful for performing tasks such as data synchronization, periodic processing, or generating reports.


**Blob Trigger:** 

This type of function is triggered when a new or updated blob is added to an Azure Storage container. It enables you to automate processes based on changes in storage blobs.


**Queue Trigger:** 

A queue trigger is triggered when a message is added to an Azure Storage queue. It provides a way to process messages in a queue-based architecture, allowing you to build event-driven applications.


**Event Grid Trigger:** 

An event grid trigger is invoked when an event is published to an Azure Event Grid topic or domain. It enables reactive processing of events and can be used to build event-driven architectures.


**Cosmos DB Trigger:** 

This type of function is triggered when there are changes to a document in an Azure Cosmos DB container. It allows you to build real-time data processing and synchronization scenarios.


**Service Bus Trigger:** 

A service bus trigger is invoked when a new message arrives in an Azure Service Bus queue or topic subscription. It is suitable for building decoupled messaging-based systems.


**Event Hub Trigger:** 

An event hub trigger is invoked when new events are published to an Azure Event Hub. It enables high-throughput event ingestion and processing scenarios.

## Assignment

Gain some practical experience with Azure Functions.  

I decided to do the Quickstart Guide from Microsoft Learn: Create your First Function in VS Code.



##  Key Terms

##  Resources


[Getting Started with Azure Functions: Step by Step Guide](https://mohan-balaji.medium.com/getting-started-with-azure-functions-a-step-by-step-guide-e18f16764017)

[Microsoft Learn : Create your First Function VS Code C#]](https://learn.microsoft.com/en-us/azure/azure-functions/create-first-function-vs-code-csharp)

[Micrsoft Learn App Configuration references for App Service and Azure Functions](https://learn.microsoft.com/en-us/azure/app-service/app-service-configuration-references)

##  Difficulties

When I tried to call my function this first time, I had to re-download the Functions Core Tools as my first attempt wasn't succesful.

Part 3:

When trying to Deploy to Function App, the operation was aborted:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/9a2ae9b5-df80-4fac-bc2d-297f76e30456)

And this error message was supplied:

*Failed to detect running Functions host within "60" seconds. You may want to adjust the "azureFunctions.pickProcessTimeout" setting.*

And so the inevitable troubleshooting began! :-) 

[Troubleshooting](https://media.giphy.com/media/dyF6DUAHJ2sS1h1CMu/giphy.gif)

##  Results

#  Part 1:  Creating local project

###  First, I needed to configure my environment to ensure I have all the requirements in place:

1.  *An Azure account with an active subscription.*  I have this 

2.  *.NET 6.0 SDK, and optionally .NET 7.0 SDK when targeting .NET 7.0.*  I have this from previous excercises.

3.  *Visual Studio Code on one of the supported platforms.*  I have this

4.  *C# extension for Visual Studio Code.*  I installed this as I didn't have it yet

5.  *Azure Functions extension for Visual Studio Code.*  I installed this as I also didn't have this yet.

###  Next, I installed/updated Core Tools in VS Code:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/c296fa38-63bc-42be-b860-e63e07aec170)

###  I then created my local project

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/3f4f36f2-4783-45b0-9e7b-bea37a4e7825)


##  And used the table below to populate the relevant fields:

| Prompt                                         | Selection                                   |
|-----------------------------------------------|---------------------------------------------|
| Select a language for your function project   | Choose C#.                                  |
| Select a .NET runtime                         | Choose .NET 8.0 Isolated (LTS).             |
| Select a template for your project's first function | Choose HTTP trigger.                     |
| Provide a function name                      | Type HttpExample.                           |
| Provide a namespace                          | Type My.Functions.                          |
| Authorization level                          | Choose Anonymous, which enables anyone to call your function endpoint. To learn about authorization level, see Authorization keys. |
| Select how you would like to open your project | Select Open in current window.            |




###  VS Code then used the information in the above table to generate an Azure Functions project with an HTTP trigger:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/f84f1e4f-b484-4351-8eb5-27577f53a3ef)



###  Executing function:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/de33bda1-0a73-4341-84ad-36a11bd57f63)


###  Function executed locally as evidenced by  the noticaion raised in VS Code:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/6c831193-298c-4d8d-9eab-b82cd8459cd4)

###  I then stopped Core Tools and disconnected debugger by Pressing Ctrl + C 

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/fdbc370d-a7e5-409c-a265-d81b4372ceb1)

# Part 2:  Create the function app in Azure:

### Firstly, I created the function app in Azure:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/83d78826-d21f-4978-b172-319496c0331d)


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/a00321ab-d9df-44c5-81d6-ca173d0bee4b)


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/3f114835-a22f-460d-a213-f69da67e9ca0)



![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/8540a916-a9f4-4b53-9e44-d10f86f581b9)

#  Part 3:  Deploy the Project to Azure:

I located the Function App in my Resources and selected 

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/42d42545-041c-4fe0-9809-fc8cb821e6dc)


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/2a393fbf-5f9a-4d72-8cd4-bd28c545f019)

I selected Deploy when this warning popped up:


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/9987b21c-6a23-4043-be83-5819b136c2cd)

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/25078b64-1d0e-4e3e-8faa-4bfea837493a)

Success! Deployment succesful!

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/95d94d98-475e-4dbc-9d56-48946b6f8067)

Here I navigated to the function app:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/07830cd2-45fc-4cd9-8dea-236089df7ac5)

###  Part 4:  Run the Function in Azure

I executed the function :

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/b280dae1-0e51-420b-8ed6-59fda5e01ce2)

And received the notification that it has been succesfully executed:


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/e6990ea5-4faf-4c30-81f2-656dd00cf4fd)


###  Part 5:

Delete resources to avoid unnecesary expenditure

First, I naviagred to the Azure Portal and selected the relevant resource group to view all resources within Azure Portal:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/0b260089-b311-45d6-8c72-c2202fb1ccd0)

Next, I deleted the Resource Group :




## Learning/Reflection:

This was the first excercise where I completed a (for me!) complicated process in Azure via VS Code.  I really enjoyed it as it's so responsive and I learnt a lot more about VS Code and the interface with Azure.  

After completing the Quickstart Guide for Azure App Service and the theoretical knowledge file for Azure App Configuration, I realised that these subjects are interrelated.  Here is a summary of what I've found.

### Azure App Service

**Overview**:  
Azure App Service is a cloud platform that allows you to build, deploy, and scale web apps and APIs quickly and easily. Think of it as a managed environment where your web applications can live and run without you having to worry about the underlying infrastructure.

**Key Points**:
- **Host Web Apps**: You can host websites, RESTful APIs, and mobile backends.
- **Scalable**: Easily scale your apps up or down based on demand.
- **Managed Environment**: Azure handles the servers, networking, and storage, so you can focus on your app.

**Relation to Other Services**:
- **Azure App Configuration**: Use Azure App Configuration to manage and store configuration settings for your web apps, keeping configuration separate from your code.
- **Azure Functions**: You can call Azure Functions from your web app to execute small pieces of code (functions) in response to events or HTTP requests, extending the capabilities of your web app without deploying additional infrastructure.

### Azure App Configuration

**Overview**:  
Azure App Configuration is a service that helps you manage application settings and feature flags centrally. It allows you to keep your configuration settings separate from your code, making it easier to manage and update them.

**Key Points**:
- **Central Management**: Store all your application settings in one place.
- **Dynamic Configuration**: Update settings without redeploying your application.
- **Feature Flags**: Enable or disable features in your application easily.

**Relation to Other Services**:
- **Azure App Service**: Use Azure App Configuration to provide configuration settings for your web apps hosted on Azure App Service, ensuring that your apps can retrieve and use these settings dynamically.
- **Azure Functions**: Azure Functions can also retrieve configuration settings from Azure App Configuration, allowing for consistent configuration management across different types of applications.

### Azure Functions

**Overview**:  
Azure Functions is a serverless compute service that lets you run small pieces of code (called functions) without managing any infrastructure. You write the code, and Azure Functions takes care of running it when triggered by events like HTTP requests, timers, or messages.

**Key Points**:
- **Event-Driven**: Functions run in response to events.
- **Scalable**: Automatically scales to handle the number of events.
- **Cost-Effective**: Pay only for the compute resources you use.

**Relation to Other Services**:
- **Azure App Service**: Azure Functions can be used to extend web apps hosted on Azure App Service by adding serverless functionality. For example, a web app can trigger a function to process a form submission or handle background tasks.
- **Azure App Configuration**: Store and manage settings for your functions in Azure App Configuration, allowing your functions to access these settings dynamically, ensuring consistency and ease of management.

### Combined View

When you use these services together, you get a powerful combination for building modern, scalable, and manageable applications. Azure App Service hosts your web apps, Azure Functions provides serverless compute for event-driven tasks, and Azure App Configuration manages and stores your app settings centrally. This separation of concerns makes your applications more flexible, easier to manage, and more resilient to changes.

