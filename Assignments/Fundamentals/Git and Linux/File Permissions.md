##  Subject:

##  Assignment
Create a text file.
Make a long listing to view the file’s permissions. Who is the file’s owner and group? What kind of permissions does the file have?
Make the file executable by adding the execute permission (x).
Remove the read and write permissions (rw) from the file for the group and everyone else, but not for the owner. Can you still read it?
Change the owner of the file to a different user. If everything went well, you shouldn’t be able to read the file unless you assume root privileges with ‘sudo’.
Change the group ownership of the file to a different group.

##  Key Terms
*Permissions*: Different users have different permissions to read, write and execute files.  This is key to managing systems safely.
*Read* (r): Allows users to read files that they have permissions for
*Write* (w): Allows users to write files in the directories they have permission for
*Execute* (x): Allows authorised users to execture script files or in the case of directories, execute allows user to access subdirectores and files 



##  Resources

[Hostman Tutorials](https://hostman.com/tutorials/how-to-create-a-text-file-in-linux-terminal/)

[Linux Simply](https://linuxsimply.com/ubuntu-file-permissions-command/)

ChatGPT

##  Difficulties
I couldn't easily located how to iterpret the information that I received from the long list of the file permissions on my favourite resource, Linux Simply.  The only information that was clear to me at first glance was that elmarie_ only had read/write permission.  I guessed that elmarie_ was also the owner and the group but I wasn't sure which instance of elmarie_ indicated which.  So I asked ChatGPT to break the information into the relevant bits to identify where I find the owner and the group and what the 1 meant.  It's explanation didn't make sense as it indicated that both the group and the owner was indicated by the first instance of elmarie_ in the string.  I challenged that and then it said that the first instance of elmarie_ indicates the owner of the file and the second instance of elmarie_indicates the group.  
**Learning**: This was an obvious and easy mistake to catch and confirmed again that information from ChatGPT should always be double checked, however, I find it useful to give me a starting point when I'm lost.

When I tried to removew *rw* permissions for the group, it seemed to only remove the write permission.



##  Results

I created a textfile and used the *ls -l* command to make a long listing of file permissions, first for the current user, then for the textfile I created.  From this information, I can see that the file's owner is elmarie_, and that I only have read/write permission

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/4b97f84d-f664-4801-8751-3e293b380bb5)

In the image below, I made the file executable by giving the owner permission using the *chmod u+x* command

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/4b2bc6da-b844-41f5-9d1c-549e81aa7093)


Owner changed to *binky*, checked if *elmarie_* could read it, unable to read file without using *sudo*

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/9b8c1f67-8bf9-44d2-a257-3c29f8d90251)

Group changed to *binky*
![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/497b088c-8222-4553-b96a-bbef6d443b07)





##  Reflection/Learning
