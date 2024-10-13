##  Subject:  Processes
This assignment introduce the concept of processes, how they are interrelated and demonstrates amply the many difficulties encountered if you can't start a process.


##  Assignment
Start the telnet daemon.
Find out the PID of the telnet daemon.
Find out how much memory telnet daemon is using.
Stop or kill the telnet daemon process.

## Key Terms

*daemon*:  this is a background process used to supervise the system or provide functionality to other processes (like the inetd provides to the telnetd?)

*PID*: Process ID is a unique identifyer assigned when the process is created

*inetd*: internet daemon, who as it turned out, manages the telnet daemon and was the key to doing this assignment



##  Resources

[Web Hosting Geeks](https://webhostinggeeks.com/howto/how-to-install-telnet-on-ubuntu/)

[IBM Docs](https://www.ibm.com/docs/en/aix/7.3?topic=t-telnetd-daemon)

[Its Foss](https://itsfoss.com/start-stop-restart-services-linux/)

ChatGPT

[Manpages Ubuntu](https://manpages.ubuntu.com/manpages/bionic/man7/daemon.7.html#:~:text=A%20daemon%20is%20a%20service,scheme%20originating%20in%20SysV%20Unix.)





##  Difficulties

When I tried testing the connection as suggested by the instructions I found, I got an error message saying Connection refused.

I had difficulty finding a command to check what the telnet daemon was listed as in the system, as I thought maybe this was part of why I couldn't start it. I found *It's Foss* and they had clear information, explained well,  that seemed to be more appropriate to what I needed to do for this assignment.

I went back and tried installing the telnet daemon again. This worked, but then I still couldn't start it.  So having confimred that it was now installed, I focussed my troubleshooting efforts on why I couldn't get it started.  As part of the process, I checked the status of inetd and this gave me an idea of what it would look like when I got the telnet daemon started.

Somewhere along my process I lost track of the fact that I was using Ubuntu and started searching for the wrong information.  This was a huge mistake as it cost me a significant amount of time and frustration but I'm glad it happened in week 1 of my course as I will certainly not make this mistake again.






##  Results

Several sources suggested that I first update my system so I used *sudo apt update* as my first step:


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/033b0e11-e2bf-48c4-9dac-41127475ff9b)

I then installed telnet and tried to test the connection.  The information I received stated that 'telnet is already the newest version', which confirmed that telnet was already installed.

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/e0e82780-ddd4-45fb-b10f-1d70b59308a2)



Next I tried starting telnet daemon but I kept getting error messages.  I then tried *ls -al*  and this happened:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/a88feaa9-21bb-4a46-8dac-10f80850a642)

Which looked super interesting but didn't get me closer to goal (or at least not that I could understand)

So I kept on trying to trouble shoot on how to start telnet daemon.

Next I tried *sudo systemctl list-unit-files --type service -all* which felt like a step in the right direction:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/23a2d7c5-501d-4a84-92d9-4a909adea6ca)

I couldn't see anything with telnet in the title so tried a modified command to provide only the relevant information that I was looking for: *sudo systemctl list-unit-files --type service --all | grep telnet* but this returned no results, which I took to mean that the telnet deamon was not after all installed.  

So next I used *sudo apt install telnetd* and low and behold:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/9f526f0c-bb0e-4cea-8b24-88b16148f932)

But I still couldn't get the telnet daemon started so I checked the status of *inetd*, which also gave me an idea of what I was looking for in establish the telnet daeomon's PID and memory usage:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/5d44a381-5ed9-4ba4-b897-bc557ffac68f)

I then tried to see if I could find the file where the telnet daemon was stored, using the file information listed in the installation information, but this did not go well:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/14ef4128-4342-42ad-8e3e-27dcaae3e02b)



I decided to run another command to check service status, and didn't see any listing for telnet:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/5c606526-8447-4bb2-9301-24174c334245)

And then I think I found the correct command as I finally had an option to start the telnet service:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/fffad448-b417-490e-be8d-e2a93e0b84e7)


I first tried authenticating with user Binky Pinky as I had that password at hand and couldn't remember receiving or creating a password for elmarie_ but this didn't work, so I created a password for elmarie_ but again I couldn't start telnet as telnet-service.service not found

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/eb0c37b2-acff-4709-9aed-709ec69e0c24)

So I started from scratch again:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/6986eedc-8ba4-402c-95a0-810cbc06ebbb)

I then proceeded to move the telnetd file to a more appropriate location, tried to start it again and then decided that I needed help to solve this one:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/0d9a6d9b-9e44-4d98-91b6-9074c053aa00)

I tried to give myself permission to execute the telnet daemon but I got the same error message, No such file or directory:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/dcac5bad-183f-4335-abf3-7f21b989365c)

I installed telnet and tried to start it but got the same message: Unit telnet.service not found

Then I asked ChatGPT a better question, and consequently got another clue to solving this assignment:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/39215df9-c439-420f-a4f3-198ae432dd5a)


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/1ff3d4ed-3db7-4a05-95bc-82ba45a7ee3d)

Here is the proof of starting and stopping telnet daemon,including the memory used and PID:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/0476226f-c0bd-43d2-99de-07cf6cd7f320)


##  Reflection/Learning
I didn't understand the information I received when I ran the first update, but it tweaked my curiosity.  I'm also interested as I noted in the apt list that Python is installed and I'm keen to learn more about this.

The main thing that I learned from this excercise was that the telnet daemon is managed by the inetd.  I came accross this information early on in my search but didn't make the connection.  

I have a lot more learning to do about processes and how they work, including  their *interconnectedness*

Dirk Gently was right!
