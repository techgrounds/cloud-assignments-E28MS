##  Subject

These excercises are about using conditional statements (if, else and elif).  This will be crucial to ensure scripts are run appropriately.

##  Assignment

### Exercise 1:

Create a new script.

Use the input() function to ask the user of your script for their name.

If the name they input is your name, print a personalized welcome message. 

If not, print a different personalized message.



###  Exercise 2:

Create a new script.

Ask the user of your script for a number. Give them a response based on whether the number is higher than, lower than, or equal to 100.

Make the game repeat until the user inputs 100.


##  Key Terms

##  Resources

[Python Org](https://discuss.python.org/t/input-in-if-else-statements/41197)

[Stack Overflow](https://stackoverflow.com/questions/26695649/creating-if-else-statements-dependent-on-user-input)

[Tutorials Teacher](https://www.tutorialsteacher.com/articles/convert-input-to-number-in-python)



##  Difficulties
Excerxise 1:  Using if/else and elif with numbers seemed straightforward but I had to research how to get the strings into an else/if statement without syntax errors.  Once I figured out to use == to ensure the correct statements, everything else fell into place.

Excercise 2:  The key bit here was to remember that all user input are read as strings and to convert the strings to integers. 

##  Results

### Excercise 1:

My code:
```
# ask user for their name:
who_are_you = input('What is your name?')

# if the user is Elmarie, print personalised message:
if who_are_you == 'Elmarie':
    print ('Welcome, Queen Elmarie!')
# if user is not Elmarie, print alternative messsage:
else: 
    print ('You are not the Queen! Off with your head!')
```

Output:

```
What is your name?Elmarie
Welcome, Queen Elmarie!
PS C:\Users\elmar> & C:/Users/elmar/AppData/Local/Programs/Python/Python312/python.exe c:/Users/elmar/Python.py/ConditionsEx1.py
What is your name?Bobby
You are not the Queen! Off with your head!
```

### Excercise 2:

My code:
```



##  Learning/Reflection
