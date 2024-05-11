##  Subject

Azure App Service is a fully managed platform for building, deploying, and scaling web apps and APIs. 

Whether you're a seasoned developer or just starting your journey in cloud computing, Azure App Service offers a seamless experience to host your applications without worrying about infrastructure management. 



Key Terms and Definitions:

Azure App Service: 

A platform-as-a-service (PaaS) offering from Microsoft Azure that enables developers to build, deploy, and scale web applications and APIs.

**Web App:**

A type of application hosted on Azure App Service that is accessible over the internet via a web browser.

**API App:**

An application hosted on Azure App Service specifically designed to serve APIs, allowing other applications to interact with it programmatically.

**Deployment Slot:** 

A separate instance of your web app or API app where you can deploy and test changes before swapping it with the production slot.

**Scale Up/Down:** 

Adjusting the resources allocated to your app, such as CPU and memory, to handle varying levels of traffic.

**Scale Out/In:** 

Increasing or decreasing the number of instances running your app to distribute the load and improve performance.

**Continuous Deployment:**

Automating the deployment process by linking your Azure App Service to a source control repository, such as GitHub, to deploy changes automatically whenever new code is pushed.

**Custom Domain:** 

Assigning a custom domain name to your Azure App Service instead of using the default azurewebsites.net domain.


**SSL Certificate:** 

Secure Socket Layer certificate used to enable HTTPS for your custom domain, ensuring secure communication between the client and the server.


Application Insights:

A monitoring and analytics service provided by Azure for applications hosted on Azure App Service, offering insights into application performance, usage, and issues.


Exercise:

Deploying a Simple Web App:

1.  Create a new Azure App Service instance.
2.  Deploy a simple HTML/CSS/JavaScript web application to the Azure App Service using Azure Portal or Azure CLI.
3.  Access the deployed web app through the provided URL.
   Configuring Continuous Deployment:

4.  Link your Azure App Service to a GitHub repository.
5.  Make changes to your application code in the repository and push them to GitHub.
6.  Verify that Azure App Service automatically deploys the changes from the repository to the deployed web app.





##  Assignment:

Gain practical experience with:

*  Azure App Service

Keep the following questions in mind during this assignment:

1.  What problem does X solve?
2.  What key terms are associated with X?
3.  How does X fit into / replace X in an on-premises setting?
4.  How can I combine X with other services?
5.  What is the difference between X and other similar services?
6.  A handy list of tasks you need to be able to perform practically:

7.  Where can I find this service in the console?
8.  How do I turn on this service?
9.  How can I connect this service to other resources?

##  Resources

[Azure for Everyone - Video of Azure App Service Overview](https://www.youtube.com/watch?v=4BwyqmRTrx8&ab_channel=AdamMarczak-AzureforEveryone)

ChatGPT

[Learn Microsoft Getting Started with App Service Python](https://learn.microsoft.com/en-us/azure/app-service/getting-started?pivots=stack-python)

##  Difficulties

It was very confusing in the beginning trying to follow along with Microsoft's Quickstart Guide for Azure App service as there was a lot of information presented for people already familiar with creating webb apps (or it certainly seemed that way to me).

I first read through the guide, tried to identify the specific bits I was didn't understand how to do and then tried to phrase good questions for tutorial help from ChatGPT.

When I tried to create a virtual environment as per the instructions, I got the following error message:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/dbb1553f-3ef2-43ed-919f-7c627976b887)

I troubleshooted with ChatGPT, who suggested the following code instead to circumnavigate the PowerShell restrictions that were preventing me from creating the virtual environment:

```
.venv\Scripts\activate.bat
```




##  Results

I created a webb app in Azure:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/cfbdf138-c9c8-4eb2-8cff-5c4c6e65624d)

Next I installed the Azure VS Code Extention, then I navigated to the VS Code Terminal and cloned the sample application repository:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/f70b6ba4-a5da-44df-a364-c60bcc04018e)


I could then see the folder with the Quickstart project:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/40043a83-0054-4646-8edc-76bcce230b81)







