
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
















