##  Subject

This assignment is about firewalls and understanding the first concepts of how to prevent unwanted or unauthorised access from the web into your machine.  It draws on previously covered topics like SSH, ports and the Linux command line.

##  Assignment

Install a web server on your VM.

View the default page that is installed with the web server via your browser on your PC/laptop.

Set the firewall so that you block web traffic, but allow SSH traffic.

Check whether the firewall is doing its job.

##  Key Terms

firewall - in this case, the firewall is a piece of software that is available on the Linux machine.  It allows you to set up rules for which ports are open to which type of traffic.

ufw - 

##  Resources

[Amazon Tutorials](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Tutorials.WebServerDB.CreateWebServer.html)

##  Difficulties

I couldn't connect with with my VM on the first try:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/78a6be34-df6a-410d-a964-6f06b062b76a)

So I checked the status of appache, confirmed that it was running now and tried again, with the same result.  Next , I troubleshooted the port access.

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/efc1a89b-34e2-4c0c-8ae1-7c4df0699b5d)



##  Results

##  *Here I found the open ports on my VM:*

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/d0ccdc34-130b-4dc9-a145-9844dec7b0eb)

## *Here I viewed the default page that is installed with the web server via my browser:*

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/f23e6508-d0de-4559-ba86-87f7d01d548d)

## *Install Firewall on VM that allows SSH traffic but blocks web traffic*

Here are the commands I used to allow SSH traffic to standard SSH port 22 as well as my SSH Port 52200.  I then blocked web traffic by denying access to port 443 (https) and port 80 (http):

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/696f51ee-6103-4b2e-984e-2b1229697b71)

I then checked to see if the rules were applied before trying to enable the firewall again:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/b0ef7080-dcbe-4c5f-9e9a-d0713eb82f5d)

And finally enabled the firewall using ufw :

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/d6c00883-d352-4d93-8d54-564c0dc4adff)



Here I tested if I could connect to the webserver on my machine and I couldn't connect

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/f2e5ba94-88c7-42f2-9021-be0228623031)




##  Learning/Reflection
Finding out which port to use was key here, I needed to use my webport to view the webpage. 


