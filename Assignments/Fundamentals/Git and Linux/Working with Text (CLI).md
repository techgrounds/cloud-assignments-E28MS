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

ChatGPT





##  Difficulties
I realised that during my first attempt at this assignment, I only added one sentence to the textfile.  So I added another sentence to textfile using input redirection in order to be able to complete the final parts of the assignment.


##  Results

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/0cef6fac-3528-427d-98cc-053d87b86695)


##  Reflection/Learning

I noted two additional things of interest during my research for completing this assignment:  

1.  If you use output redirection to send 'output' (information) to a file and there is already a file present with the same name, the existing file will be overwritten.  If you want to add content to an existing file, you need to use the >> operator instead.  I also note that you can also redirect standar output to devices eg cat music.mp3 > /dev/audio
I did not realise yet so this is interesting, while not immediately useful for this assignment.

   
2.  Error redirection is apparently a very popular feature in Linux - so worth taking not of as I'll probably find use for this in the future.  




