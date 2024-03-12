# Creating an SSH Connection to a Linux VM 
I was provided with some credential information and then I had to log into my remote Linux VM


## Key-terms
1. SSH - Secure Shell 
2. Linux VM
3. Web port
4. PEM Key


## Assignment
Make an SSH-connection to your virtual machine. SSH requires the key file to have specific permissions, so you might need to change those.
When the connection is successful, type whoami in the terminal. This command should show your username.


## Resources
1. [Microsoft Learn]{https://learn.microsoft.com/en-us/azure/virtual-machines/linux/ssh-from-windows}
2. ChatGPT
3. My team mates and learning coach provided some useful tips about the correct order of the command and also suggested I re-check the Public IP address.

## Difficulties 
1. Repeated error message 'publickey'
2. Repeated 'connection timed out' error message

## Results
I managed to log into my container in the VM after resolving the above errors by fixing the order of the credential information and by identifiying and fixing an error in the VM Public IP that I had mistyped.
