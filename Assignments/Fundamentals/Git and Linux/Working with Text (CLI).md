##  Subject: Working with text (CLI)

This assignment introduces the concept of standard input and standard output, input and output redirection and working with text in the command line interface.

##  Assignment

Use the echo command and output redirection to write a new sentence into your text file using the command line. The new sentence should contain the word ‘techgrounds’.
Use a command to write the contents of your text file to the terminal. Make use of a command to filter the output so that only the sentence containing ‘techgrounds’ appears.
Read your text file with the command used in the second step, once again filtering for the word ‘techgrounds’. This time, redirect the output to a new file called ‘techgrounds.txt’.

##  Key Terms

*  standard input (stdin): entering a command with your keyboard


*  standard output (stdout): the information received once you've excecuted a command, displayed on your terminal


*  redirection:  this lets you change the standard input/output 


*  input redirection: this is when your input gets redirected for instance by attaching a file to an email.  The < sign is used to achieve this.


*  output redirection: this command can be used to redirect output to a file instead of your screen, for instance.  The > sign is used for this is 


*  pipe

## Resources

[Linux Journal](https://www.linuxjournal.com/content/everything-you-need-know-about-linux-input-output-redirection#:~:text=In%20Linux%2C%20when%20you%20enter,change%20the%20standard%20input%2Foutput.)

[Linux Simply](https://linuxsimply.com/cheat-sheets/ubuntu-commands/)

[Echo Command in Linux](https://linuxsimply.com/echo-command-in-linux/)

ChatGPT

[Geeks for Geeks](https://www.geeksforgeeks.org/filters-in-linux/)


What I've learn in Summary
I've included this section at this point of my learning form for reasons of saving you time.  If you do decide to be brave and scroll down, you will find that I recorded all of my mistakes.


##  Difficulties
I realised that during my first attempt at this assignment the previous day,  I only added one sentence to the textfile.  So I added another sentence to textfile using input redirection in order to be able to complete the final parts of the assignment.

I got into a muddle and created another textfile in the techgrounds directory, then added another sentence to this using the echo command and redirecting the text to my secondtextfile.txt file.  However, things didn't go according to plan and I ended up with this:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/9abfb623-2adc-4072-a0ba-1a95b03237f4)


After a bit of confused head scracthing, I realised that I didn't close the double quotes encapsulating my text and I continued.

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/7ea6a5bb-6990-44cb-9c8b-9b0dd6a56c97)


Then I accidentally created a second file called secondtextfile.txt:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/94f7c615-a56b-4974-a562-9b80b238062f)

While at the same time realising that I didn't finish the second part of the assignment with regards to filtering, which made me realise that one file contained several sentences but not the word techgrounds, and another file contained the word techgrounds but only one sentence, which meant that neither file was appropriate for filtering.  So then I made use of this learning opportunity to add more text to both files, and promptly put a great sentence in the wrong file.  Then I decided to have a cup of tea and consider my options...

This is what it now looked like:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/fd0be5a8-aa6e-4a1e-b32d-c457ba27e155)


1. Fix the mess
2. Start from scratch

I decided to do both for maximum practice time, but first I would finish in my messy session to go through all the assignments and also figure out what a pipe in Linux is, as I presumably couldn't smoke it.

I first tried the grep command: grep techgrounds secondtextfile.txt

This recalled all the content of the file, so I kept looking.


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/b891eb67-fd18-4485-b99c-b7f6a35991af)

I then tried the following variations on grep, with the same result:

cat secondtextfile.txt | grep techgrounds

cat secondtextfile.txt | grep -w techgrounds

Then I read the assignment again and thought that maybe a line in Linux does not mean a sentence as I (unknowingly) assumed.  And indeed, it turns out that sentences need to be literally on seperate lines in order to be considered seperate. 








##  Results

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/0cef6fac-3528-427d-98cc-053d87b86695)

Then I tried this :  cat secondtextfile.txt | grep techgrounds

Which again just highlihgted the word techgrounds and produced both sentences on the screen. Mmmmmmhhhhhhh.....


##  Reflection/Learning

I noted two additional things of interest during my research for completing this assignment:  

1.  If you use output redirection to send 'output' (information) to a file and there is already a file present with the same name, the existing file will be overwritten.  If you want to add content to an existing file, you need to use the >> operator instead.  I also note that you can also redirect standar output to devices eg cat music.mp3 > /dev/audio
I did not realise yet so this is interesting, while not immediately useful for this assignment.

   
2.  Error redirection is apparently a very popular feature in Linux - so worth taking not of as I'll probably find use for this in the future.  




