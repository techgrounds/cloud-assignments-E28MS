##  Subject

##  Assignment

#  Exercise 1:

Create a new script.

Copy the code below into your script.

a = 'int'

b = 7

c = False

d = "18.5"

Determine the data types of all four variables ( a, b, c, d) using a built-in function.

Make a new variable x and give it the value b + d. 

Print the value of x. This will raise an error. Fix it so that print(x) prints a float.

Write a comment above every line of code that tells the reader what is going on in your script.

# Exercise 2:

Create a new script.

Use the input() function to get input from the user. Store that input in a variable.

Find out what data type the output of input() is. See if it is different for different kinds of input (numbers, words, etc.).


##  Key Terms

*Data types in Python*

*int (integer)*

*str (string)*

*bool (boolean expression)*






##  Resources

[Software Carpentry](python.exe c:/Users/elmar/Python.py/datatypesEx1.py <class 'str'> <class 'int'> <class 'bool'> <class 'str'>)



##  Difficulties

##  Results

# Excercise 1

My code:

```
a = 'int'

b = 7

c = False

d = "18.5"

print (type (a))
print (type (b))
print (type (c))
print (type (d))
```

Output:

```
PS C:\Users\elmar> & C:/Users/elmar/AppData/Local/Programs/Python/Python312/python.exe c:/Users/elmar/Python.py/datatypesEx1.py
<class 'str'>
<class 'int'>
<class 'bool'>
<class 'str'>
```



Excercise 2

Here is the error when trying to add an integer to a string:

```
Traceback (most recent call last):
  File "c:\Users\elmar\Python.py\datatypesEx1.py", line 14, in <module>
    apples_and_pears = (b + d)
                        ~~^~~
TypeError: unsupported operand type(s) for +: 'int' and 'str'
PS C:\Users\elmar>
```

##  Learning/Reflection
