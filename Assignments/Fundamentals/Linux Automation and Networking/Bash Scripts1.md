## Subject:  Bash Scripts



##  Assignment 1

1.  Create a directory called ‘scripts’. Place all the scripts you make in this directory.
2.  Add the scripts directory to the PATH variable.
3.  Create a script that appends a line of text to a text file whenever it is executed.
4.  Create a script that installs the httpd package, activates httpd, and enables httpd. Finally, your script should print the status of httpd in the terminal.

##  Key Terms

**scripts** :lines of codes that can be executed to automate processes, like appending text to a textfile so it doesn't have to be done manually in every instance

1. **bashrc file**:
   - The bashrc file, often named `.bashrc`, is a script file executed by the Bash shell when it starts in an interactive mode. It stands for "Bourne Again Shell run commands".
   
   - This file typically contains commands, aliases, functions, and other configurations that customize the behavior of the Bash shell for a particular user.
   
   - Users can edit their `.bashrc` file to set environment variables, define aliases, customize the prompt, and perform other tasks to tailor their shell environment to their preferences.

2. **PATH variable**:
   - The PATH variable is an environment variable used by the operating system to determine the locations of executable files.
   
   - When a user types a command into the shell, the system searches through the directories listed in the PATH variable in order, looking for an executable file with a matching name.
   
   - If it finds one, it executes that file. The PATH variable is crucial for the functioning of the command-line interface, as it allows users to run commands without specifying the full path to the executable file.
   
   - Users can modify the PATH variable to include additional directories where their custom scripts or executables are located.

3. **httpd package**:
   - The httpd package typically refers to the Apache HTTP Server package, which is a popular open-source web server software used to serve web pages and applications over the internet.
   
   - Apache HTTP Server, often simply called Apache, is highly configurable and extensible, supporting various modules for additional functionalities such as handling dynamic content, authentication, URL rewriting, and more.
   
   - It is widely used across the internet to host websites and web applications on various platforms, including Linux, Unix, and Windows. The httpd package usually includes the core Apache server binaries, configuration files, documentation, and possibly additional modules or utilities.

**apt** : 
Advanced Package Tool is used to manage packages (like httpd) in Debian based Linux distrubutions like Ubuntu

##  Resources

[Tech Republic](https://www.techrepublic.com/article/linux-101-how-to-add-directories-to-your-linux-path/)

[Digital Ocean](https://www.digitalocean.com/community/tutorials/how-to-view-and-update-the-linux-path-environment-variable)

[IO Flood](https://ioflood.com/blog/bash-append-to-file/#Appending_Data_Within_a_Script)

ChatGPT - which explained that process of creating scripts step by step, this helped my understanding of this essential process


##  Difficulties
I had trouble running the script in 1.4 but it turned out the problem was a typo. 

I needed to research the key terms before I could understand what was expected of me.


##  Results
1.1.  Create a directory called 'scripts'

Created and checked that it is created:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/2cb912b6-393f-497a-ab89-37683cdd0c99)

1.2.  Add the scripts directory to the PATH variable:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/c68adb49-54a4-4e7d-9982-53a23f07b02c)

1.3.  Create a script that appends a line of text to a textfile whenever it is executed

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/845308d4-9428-4017-8e6f-ce551018f11f)


1.4 Created script that installs, activates and enables httpd, and then prints status to terminal:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/66336a93-aa62-4122-bb23-ba34c922e033)

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/5215e25b-eacf-45ef-a717-680cea6cfdef)

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/545f127e-1efe-47d8-8b64-7287e191a84c)



## Learning/Reflection

1.  I found this on my first search for how to complete this assignment and it highlighted the purpose and future use of this assignment: 

*Your Linux PATH is how you define the directories for which commands can be run globally. In other words, if you have an executable file in a directory that is configured to be in your PATH, you can run that executable from anywhere in the Linux file structure. This is what makes it possible to run commands in /usr/bin from your home directory (or anywhere, for that matter).*

2.  Check, check and check again for typos or other human errors if something doesn't work 

