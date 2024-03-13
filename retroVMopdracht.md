#Subject
#Logging into Linux VM Remotely
I was provided with some credential information and then I had to log into my remote Linux VM

## Key-terms
[Schrijf hier een lijst met belangrijke termen met eventueel een korte uitleg.]
SSH - Secure Shell 
Linux VM


## Opdracht

Make an SSH-connection to your virtual machine. SSH requires the key file to have specific permissions, so you might need to change those.
When the connection is successful, type whoami in the terminal. This command should show your username.
### Gebruikte bronnen
[Microsoft Learn]{https://learn.microsoft.com/en-us/azure/virtual-machines/linux/ssh-from-windows}
ChatGPT
My team mates and learning coach provided some useful tips about the correct order of the command and also suggested I re-check the Public IP address.




### Ervaren problemen
-Repeated error message 'publickey'
-Repeated 'connection timed out' error message

### Resultaat
[Omschrijf hoe je weet dat je opdracht gelukt is (gebruik screenshots waar nodig).]
I managed to log into my container in the VM after resolving the above errors by fixing the order of the credential information and by identifiying and fixing an error in the VM Public IP that I had mistyped.


