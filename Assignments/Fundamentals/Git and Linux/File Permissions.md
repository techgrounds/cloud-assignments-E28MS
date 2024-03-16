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

##  Difficulties

##  Results

I created a textfile and used the ls -l command to make a long listing of file permissions, first for the current user, then for the textfile I created:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/4b97f84d-f664-4801-8751-3e293b380bb5)

From this information, I can see that the file's owner 


##  Reflection/Learning
