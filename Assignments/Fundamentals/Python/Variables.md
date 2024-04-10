##  Subject
Python is a high level programming language used for web and internet development, data management, education, sicentific and numeric computing and more.

##  Assignment

Exercise 1:
Create a new script.

Create two variables x and y. 

Assign a numerical value to both variables.

Print the values of x and y.

Create a third variable named addup.

The value of addup should be the sum of x and y.

Print the value of addup.

 Exercise 2:
Create a new script.

Create a variable called name. 

The value of name should be your name.

Print the text “Hello, YOURNAME!”. 

Use the variable name in the print statement. 


 Exercise 3:
Create a new script.

Create a variable and assign a value to it.

Print the text “Value 1: VALUE1”.

Change the value of that same variable.

Print the text “Value 2: VALUE2”.

Change the value of that same variable.

Print the text “Value 3: VALUE3”.

Example output:


##  Key Terms

Python reserved words:
These are words that has a meaning to Python and if you use them as variables, it will cause confusion and the code won't work

Concatenation - String concatenation is a common operation in programming. It involves joining two or more strings to create a single new string. 

F-strings - An f-string is prefixed with the letter 'f' or 'F' before the opening quote of the string literal.

Inside an f-string, you can embed Python expressions and variables by placing them within curly braces {}.They are very flexible and can handle various expressions and formatting options. You can even call functions and methods inside f-strings. They offer a concise and readable way to compose strings with dynamic content in Python.


##  Resources

[Hacker Earth](https://www.hackerearth.com/practice/python/getting-started/string/tutorial/)

[Real Python](https://realpython.com/python-string-concatenation/#:~:text=String%20concatenation%20is%20a%20common,its%20own%20pros%20and%20cons.)

[Python.org](https://www.python.org/doc/essays/blurb/)

ChatGPT

##  Difficulties

Excercise 2:

When I tried to print my name, I got an error:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/7285db2e-9a6b-4042-9334-a309b627f25d)

I had to research the different ways to get the correct output and learned about formatting strings. 

I chose the simplest way to do this by concatenating the string with the name variable.

I added different code blocks to demonstrate the different ways to do this excercise for my own learning.




##  Results

#  Excercise 1:

My code:
```
x = 5
y = 10
print (x)
print (y)

addup = (x + y)
print (addup)
```

Output:

```
PS C:\Users\elmar> & C:/Users/elmar/AppData/Local/Programs/Python/Python312/python.exe "c:/Users/elmar/Python.py/name = Elmarie.py"
5
10
15
```

#  Excercise 2:

My code:
A) Using Concatenation:

```
name = 'Elmarie'
print ('Hello,' + name +('!'))
```
Output:

```
PS C:\Users\elmar> & C:/Users/elmar/AppData/Local/Programs/Python/Python312/python.exe "c:/Users/elmar/Python.py/name = Elmarie.py"
Hello,Elmarie!
```

B) f strings method:

Code:
```
name = 'Elmarie'
print(f'Hello, {name}!')
```
Output:

```
PS C:\Users\elmar> & C:/Users/elmar/AppData/Local/Programs/Python/Python312/python.exe "c:/Users/elmar/Python.py/name = Elmarie.py"
Hello, Elmarie!
```

# Excercise 3

My code:

```
first_value = 'Good'
print ('Value 1:', first_value)
first_value = 'day'
print ('Value 2:', first_value)
first_value = 'to you all'
print ('Value 3:', first_value)
```

Output:
```
PS C:\Users\elmar> & C:/Users/elmar/AppData/Local/Programs/Python/Python312/python.exe "c:/Users/elmar/Python.py/value1 = Good.py"
Value 1: Good
Value 2: day
Value 3: to you all
```




##  Learning/Reflection
The many different ways to do things makes it difficult to retain the information.  With practice I will improve, so I need to ensure that I spend time every day coding with Python.  I will use ChatGPT to give me assignments but solve them without using ChatGPT or find some online resources with beginner projects for Python.
