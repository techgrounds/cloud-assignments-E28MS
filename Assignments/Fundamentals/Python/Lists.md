## Subject

Lists are one of the six fundamental data types in the Python programming language. 

To work effectively with Python, you need to know the functions and methods that work with lists.  In this assignment we do some excercises with lists.

## Assignment

### Exercise 1:
Create a new script.

Create a variable that contains a list of five names.

Loop over the list using a for loop. Print every individual name in the list on a new line.

### Exercise 2:
Create a new script.

Create a list of five integers.

Use a for loop to do the following for every item in the list:

Print the value of that item added to the value of the next item in the list.

If it is the last item, add it to the value of the first item instead (since there is no next item).

##  Key Terms

## Resources

[W3 Schools Lists in Python](https://www.w3schools.com/python/python_lists.asp

[Codecademy Python Fundamentals](https://www.codecademy.com/learn/dacp-python-fundamentals/modules/dscp-python-lists/cheatsheet)

Python for Everybody by Charles Severance


##  Difficulties
I had to spend some time understanding how the position of an item in the list is indicated and learn about the len function and how this can be used to loop through a list.

##  Results

Excercise 1:

My code:

```
nameslist = ['Annabel', 'Emma', 'Ben', 'Liam', 'Clara']
for names in nameslist:
    print (names)
print ('Done')
```

Output:

```
Annabel
Emma
Ben
Liam
Clara
Done
PS C:\Users\elmar>
```

Excercise 2:

My code:
```
for i in range(len(x)):
    # If it's the last item in the list
    if i == len(x) - 1:
        result = x[i] + x[0]  # Add it to the first item
    else:
        result = x[i] + x[i + 1]  # Add it to the next item
    print(result)
```

Output:

```
48
48
31
26
51
```

