##  Subject:  Cron Jobs
Cron jobs are used to schedule and automate repetetive tasks like writing available memory to a log or checking regularly for updates.

Cron is a background service(daemon) that will run commands as they are scheduled. 

Cron jobs are set up in the Crontab for streamlining routine maintenance activities.



##  Assignment
a)  Create a Bash script that writes the current date and time to a file in your home directory.


b)  Register the script in your crontab so that it runs every minute.


c)  Create a script that writes available disk space to a log file in ‘/var/logs’. Use a cron job so that it runs weekly.


##  Key Terms

**Basic Crontab syntax**:  MIN HOUR DOM MON DOW CMD
Minute of the hour (0-59)

Hour of the day(0-23), 

Day of the Month (0-31), 

Day of the Week (0-7) and 

CMD (Command - usually a path to a script or system command)

[*] in Cronjobs this operator means that it needs to be executed for all possible values of that field. 

##  Resources

[HostDime](https://www.hostdime.com/kb/hd/command-line/working-with-cron-jobs#:~:text=Cron%20jobs%20are%20a%20standard,configuration%20file%20called%20a%20crontab.)

Phoenix ](https://phoenixnap.com/kb/set-up-cron-job-linux)


##  Difficulties
I didn't know which one to choose when presented with a choice and went for the suggested - easiest with a big arrow:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/d748cd85-813a-4992-92bc-75cd831cc2ae)

I got a 'bad hour' error message when I tried to run my cronjob:

The code looked like this and I noticed the green highlights:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/153cdefc-f25e-4af3-94a8-6e6a21570453)

I then added spaces between the fields but the error persisted, although it was now a 'bad minute', which I thought may be pointing me in the direction of the problem but no idea what else to try:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/edb8e3e4-8b3a-49d1-bd87-17355cdab62a)


I realised that I had caused the cronjob to fail as I moved the script file without updating the script, so it was working all along but writing to a file in my home directory instead of to a file in my logs directory.  I moved it back and this solved the problem.  Job done!




##  Results

Here is the code I used to write datetime script:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/6a83cf73-3063-44ab-97dc-6779161d9feb)


Here are the results of datetime script:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/2a4fd006-efaa-4f30-8160-5534327a79b6)


Here I registered the cronjob succesfully in the crontab, executed it succesfully (I thought!), created a new folder called 'logs', moved the current_datetime.txt folder into this and displayed the content of the current_datetime.txt folder, proving that my cronjob works by printing every minute:

Here I checked all the above by and realised that my cronjob was not working correctly and appears to have only printed the date and time once as it kept repeating the same date and time.  So back to toubleshooting I went...


Here is the proof of my datetime cronjob working:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/57d83b6a-5cf7-468b-a00c-9ca17b89db30)










##  Reflection/Learning
I've started noticing that the CLI is actually user friendly in pointing you in the right direction for instance when you open a crontab for a user for the first time, it clearly indicated which one is the easiest to use.  Also, once I then chose the nano, it had an introduction to cron with useful information.

I got a 'bad hour' error and then didn't change anything and tried running it again and then got a 'bad minute error'.  I'm not sure what this means but I'm curious as to why the error message changed while nothing else did.  Or did I do something without realising it?

I was utterly delighted when I found the problem with my datetime cronjob was (as usual)my error in moving the file without updating the script to reflect the new location that the datetime should be written to.  So it created a new file in my home directory and was updating there all along.


