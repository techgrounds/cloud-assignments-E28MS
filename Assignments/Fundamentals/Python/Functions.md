## Subject
A function is a block of code that only runs when it is called. Functions are recognizable by the brackets () next to the function name. These brackets serve as a place to input data into a function.Functions return data as a result.

Besides the built-in functions, you can also write custom functions, or import functions from a library or package.

## Assignment
### Exercise 1:

Create a new script.

Import the random package.

Print 5 random integers with a value between 0 and 100.

### Exercise 2:
Create a new script.

2.1  Write a custom function myfunction() that prints “Hello, world!” to the terminal. Call myfunction.

2.2  Rewrite your function so that it takes a string as an argument. Then, it should print “Hello, NAME!”.

### Exercise 3:
Create a new script.

Copy the code below into your script.

```
def avg():
# write your code here
# you are not allowed to edit any code below here

x = 128
y = 255
z = avg(x,y)

print("The average of",x,"and",y,"is",z)
```

Write the custom function avg() so that it returns the average of the given parameters. You are not allowed to edit any code below the second comment.

##  Key Terms

random() - Python Random module generates random numbers in Python. These are pseudo-random numbers, which means they are not truly random as they are generated by a determenistic algorythm, however, they are virtually indistuingasble from truly random numbers.

There are several different random functions in the Random Module of Python, including *choice*, *randint*, etc.

This module can be used to perform random actions such as generating random numbers, printing random a value for a list or string, etc. It is an in-built function in Python.

function definition - this is where you create a new function by first 

## Resources

[Geeks for Geeks Python Random Module](https://www.geeksforgeeks.org/python-random-module/)

Pyhon for Everybody by Charles Severance

Team members

[Geeks for Geeks Generat Random Number within Range](https://www.geeksforgeeks.org/python-generate-random-numbers-within-a-given-range-and-store-in-a-list/)

[Digital Ocean 5 Ways to find the mean in Python](https://www.digitalocean.com/community/tutorials/average-of-list-in-python)

##  Difficulties
 I didn't encountern any major difficulties with these excercises and managed to complete them wihtout generating any code with ChatGPT.  I also discsussed some issues with my team mates.

##  Results
My code:
```
import random
for i in range (5):

     rando_numb = random.randint(0, 100)
     print (rando_numb)
```

Output:

```
PS C:\Users\elmar> & C:/Users/elmar/AppData/Local/Programs/Python/Python312/python.exe c:/Users/elmar/Python.py/functionsEx1.py
54
13
94
46
71
PS C:\Users\elmar> 
```

### Excercise 2

2.1 My code:
```
def myfunction():
        print ('Hello World!')

myfunction()
```

2.1.  Ouput:

```
PS C:\Users\elmar> & C:/Users/elmar/AppData/Local/Programs/Python/Python312/python.exe c:/Users/elmar/Python.py/functionsEx2.py
Hello World!
PS C:\Users\elmar>
```
