##  Subject: Users and Groups
This introduces how to create users and groups and to add users to groups, provide sudo priveliges to users etc.

##  Assignment
Create a new user in your VM.
The new user should be part of an admin group.
The new user should have a password.
The new user should be able to use ‘sudo’
Locate the files that store users, passwords, and groups. Find your newly created user’s data in there.

##  Key Terms

Hashed password: This means that the password is encrypted

##  Resources

I decided *not* to use ChatGPT for this assignment.

[Digital Ocean Tutorials](https://www.digitalocean.com/community/tutorials/how-to-create-a-new-sudo-enabled-user-on-ubuntu)

[Geeks for Geeks](https://www.geeksforgeeks.org/how-to-check-the-groups-a-user-belongs-to-in-linux/)

[Linux Simply](https://linuxsimply.com/ubuntu-create-group-and-add-user/)

[Ubuntu Man Pages](https://manpages.ubuntu.com/manpages/focal/en/man5/shadow.5.html)

[Cyberciti FAQ](https://www.cyberciti.biz/faq/understanding-etcshadow-file/)


##  Difficulties

First try to add Binky to sudo group :

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/dead0c4c-f06f-4b58-ae4d-26864f724e26)


##  Results : Part 1

New user added, as I didn't have root permissions, I used the sudo command to create a new user with a password:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/6a9eada0-7cd3-44ae-8e61-0074d45f7d56)

I then used the usermod command to add Binky to the sudo group:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/dff24137-76e2-42be-8844-3821984c90aa)

Testing to see if Binky had sudo access by trying to list contents of root directory:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/61b07143-9116-4bac-baf2-006a03d3ddd2)

I tried a different command: 'groups' and it listed binky's groups as sudo.  

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/960e72f2-d6ba-403e-9f49-2d72ef720fb4)

I then created an admin_group (this didn't go smoothly but I got there)

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/0f33778d-00b6-4f5c-a766-e2660dd7686c)


And then used the getent group command to see if my admin group was created:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/920f5eda-5038-4c26-8b0d-eb3c9e0222f4)

Next I located the file that stores passwords using the cat /etc/passwd command:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/aae561b3-7f11-43c2-a270-91b49f5442cf)

Here I created a new group called 'admingroup' and added my new user Binky to it:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/2bd9d26b-2582-4eea-a444-83b7c582e004)

I used the getent group command again and noted that my two admin groups have been created and then used the groups (username) command to check if Binky was in an admin group:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/a3a3f636-1fee-4730-aaef-7a1bb05adad3)

## Part 2:

Here I used the /etc/passwd command to see all the users, but I cut out all the unneccassary information using 
cut command to split on colon delimiters (-d :):
![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/d4c75e19-1f76-45bb-8edf-a5a4863fb7f7)

This is the /etc/shadow file that contains passwords, including Binky's:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/1feb3960-8221-4212-ab17-90efa1ead1bc)












