
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

##  Resources

[Microsoft External ID Tenant Setup](https://learn.microsoft.com/en-us/entra/external-id/customers/quickstart-tenant-setup)

##  Difficulties

I planned to do the Quickstart for Microsoft Entra ID but when I looked at this, I realizied that in order to follow the Quickstart Guide for this, I would first need to create an external tenant.  So I adjusted my time allocation for this task accordingly and started with this crucial prerequisite.

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

