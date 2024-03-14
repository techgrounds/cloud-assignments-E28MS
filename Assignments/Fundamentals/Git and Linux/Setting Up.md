# Subject: Setting Up
This assignment is about the Linux Operating System.  Using Linux is mostly done in the Command Line Interface(CLI),which means that it doesn't have a Graphical User Interface (GUI). This assignment is to firstly introduce connecting to a remote virutal machine through SSH and secondly to introduce the Linux Operating System Command Line Interface. 

## Key-terms


**SSH** - Secure Shell: This is a protocol for securely sending commands to a computer over an unprotected network.  It is used for controlling infrastructure, managing servers remotely and sending files.


**Linux VM** - Linux Virtual Machine

**Pem Key** - Privacy Enhanced Mail files are a type of Public Key Infrastructure file that is used for security and certificates.  They are an internet security standard.

**Web port** - A port is a number uniquely identifiying a logical endpoint of a network and to direct data to a specific service.


## Assignment
Make an SSH-connection to your virtual machine. SSH requires the key file to have specific permissions, so you might need to change those.
When the connection is successful, type whoami in the terminal. This command should show your username.


### Resources
[Microsoft Learn]{https://learn.microsoft.com/en-us/azure/virtual-machines/linux/ssh-from-windows}


ChatGPT


My team mates and learning coach provided some useful tips about the correct order of the command and also suggested I re-check the Public IP address.

{https://www.cloudflare.com/en-gb/learning/access-management/what-is-ssh/)

{https://docs.microfocus.com/SM/9.51/Hybrid/Content/security/concepts/what_are_pem_files.htm#:~:text=Privacy%20Enhanced%20Mail%20(PEM)%20files,now%20an%20Internet%20security%20standard.}

{https://en.wikipedia.org/wiki/Port_(computer_networking)}


### Difficulties
-Repeated error message 'publickey'


-Repeated 'connection timed out' error message

### Results
I managed to log into my container in the VM after resolving the above errors by fixing the order of the credential information and by identifiying and fixing an error in the VM Public IP that I had mistyped.
See SettingUpShots for screenshots

### Reflection/Learning
On reflection, this task was much easier than it felt like at the time, as I had done this before multiple times.  A reminder to myself to take a step back, take a deep breath and check the details.  Also a reminder that I enjoy the process of solving the problem by trying different things.







