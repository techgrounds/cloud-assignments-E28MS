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

[Quora](https://www.quora.com/Why-does-input-always-return-a-string-in-Python#:~:text=There%20are%20a%20few%20reasons,using%20the%20appropriate%20conversion%20function.)





##  Difficulties

##  Results

# Excercise 1

1.1   My code:

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

1.2.  Here is the error when trying to add an integer to a string:

```
a = 'int'

b = 7

c = False

d = "18.5"

print (type (a))
print (type (b))
print (type (c))
print (type (d))

x = (b + d)
print (x)
```
1.3  Here is the above code fixed, by removing the double quotes that indicates a string so that variable d is now a floating point number instead of a string:

```
a = 'int'

b = 7

c = False

d = 18.5

print (type (a))
print (type (b))
print (type (c))
print (type (d))

x = (b + d)
print (x)
```

Here is the output for the above code, indicating the new data class for d:

```
PS C:\Users\elmar> & C:/Users/elmar/AppData/Local/Programs/Python/Python312/python.exe c:/Users/elmar/Python.py/datatypesEx1.py
<class 'str'>
<class 'int'>
<class 'bool'>
<class 'float'>
25.5
```

1.4. My code with lines of text describing the code:

```
#  Four data types listed below in variables named a,b,c,d:

a = 'int'

b = 7

c = False

d = 18.5

# built in function 'type' used to express types of data for each variable and to print this:

print (type (a))
print (type (b))
print (type (c))
print (type (d))

# adding b and d to produce x
x = (b + d)

#output
print (x)
```

Here is the output of the above code:

```
PS C:\Users\elmar> & C:/Users/elmar/AppData/Local/Programs/Python/Python312/python.exe c:/Users/elmar/Python.py/datatypesEx1.py
<class 'str'>
<class 'int'>
<class 'bool'>
<class 'float'>
25.5
```
#  Excercise 2

2.1.  My code:

```
# ask for user's name 
whats_your_name = input ('What is your name?')

# ask user for current year

current_year = input ('Which year is it?')

# ask user to insert a random 3 digit number

random_number = input ('Please enter a random 3 digit number')

# print data types of user input

print (type (whats_your_name))

print (type (current_year))

print (type (random_number))
```

Here is the output of my code:

```
What is your name?Elmarie
Which year is it?2024
<class 'str'>
<class 'str'>
PS C:\Users\elmar> & C:/Users/elmar/AppData/Local/Programs/Python/Python312/python.exe c:/Users/elmar/Python.py/datatypesEx2.py
What is your name?Elmarie
Which year is it?2024
Please enter a random 3 digit number486
<class 'str'>
<class 'str'>
<class 'str'>
PS C:\Users\elmar>
```

The output of the user input is always classified as a string, regardless of whether it is an integer or a string.  Looking this up online indicates that this allows the programmer flexibility in handling this data.



##  Learning/Reflection
