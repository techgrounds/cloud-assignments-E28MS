## Subject
Dictionary in Python is an unordered collection of data values, used to store data values like a map, which unlike other Data Types that hold only single value as an element, Dictionary holds key:value pair.

While using Dictionary, sometimes, we need to add or modify the key/value inside the dictionary.

Some examples of where you will find them are NoSQL databases or AWS/Azure resource tags. 

Dictionaries (dict) in Python also use key-value pairs to store information. 

In Python, a dictionary can be created by placing a sequence of elements within curly {} braces, separated by a ‘comma’.

The dictionary holds pairs of values, one being the Key and the other corresponding pair element being its Key:value.

Values in a dictionary can be of any data type and can be duplicated, whereas keys can’t be repeated and must be *immutable.*

## Assignment

### Exercise 1:
Create a new script.

Create a dictionary with the following keys and values:

Key

Value

First name

Casper

Last name

Velzen

Job title

Learning coach

Company

Techgrounds

Loop over the dictionary and print every key-value pair in the terminal.

### Exercise 2:
Create a new script.

Use user input to ask for their information (first name, last name, job title, company). Store the information in a dictionary.

Write the information to a csv file (comma-separated values). The data should not be overwritten when you run the script multiple times.

##  Key Terms

*Dictionaries in Python* - Dictionaries in Python is a data structure, used to store values in key:value format. This makes it different from lists, tuples, and arrays as in a dictionary each key has an associated value.

*immutable* - In Python, an object is considered immutable if its value cannot be changed after it has been created. This means that any operation that modifies an immutable object returns a new object with the modified value.

##  Resources

[Free Code Camp Python Dictionaries](https://www.freecodecamp.org/news/create-a-dictionary-in-python-python-dict-methods/)

[Data Science Dojo Mutable and Immutable Objects in Python](https://datasciencedojo.com/blog/mutable-and-immutable-objects-in-python/)

[Geeks for Geeks Python Dictionaries](https://www.geeksforgeeks.org/python-dictionary/)

## Results

Excercise 1:

My code:
```
#keyvalueEx1.py
# Python program to add a key:value pair to dictionary
# create new dictionary (empty)

first_dict = dict()
print(first_dict) 
#add key:value pairs to dictionary
first_dict['First Name:'] = 'Casper'
first_dict['Last Name:'] = 'Velzen'
first_dict['Job Title:']= 'Learning Coach'
first_dict['Company:']= 'Techgrounds'
#print dictionary
print (first_dict)
# print key: value pairs
for key in first_dict:
    print (key, first_dict[key])
```

Output:
```
PS C:\Users\elmar> & C:/Users/elmar/AppData/Local/Programs/Python/Python312/python.exe c:/Users/elmar/Python.py/#keyvalueEx1.py
{}
{'First Name': 'Casper', 'Last Name': 'Velzen', 'Job Title': 'Learning Coach', 'Company': 'Techgrounds'}
First Name Casper
Last Name Velzen
Job Title Learning Coach
Company Techgrounds
PS C:\Users\elmar> & C:/Users/elmar/AppData/Local/Programs/Python/Python312/python.exe c:/Users/elmar/Python.py/#keyvalueEx1.py
{}
{'First Name:': 'Casper', 'Last Name:': 'Velzen', 'Job Title:': 'Learning Coach', 'Company:': 'Techgrounds'}
First Name: Casper
Last Name: Velzen
Job Title: Learning Coach
Company: Techgrounds
```

