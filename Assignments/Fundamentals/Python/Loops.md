## Subject
You can use loops when you want to run a block of code multiple times. 

For example, you might want to do an operation on every item in a (large) list, or you want to write an algorithm that follows the same set of instructions for multiple iterations.

There are two types of loops in Python: the while loop and the for loop.The while loop runs while a condition is true. 

The for loop runs for a predetermined number of iterations. 

This number can be hard coded using the range() function, or dynamically assigned (using a variable, the size of a list, or the number of lines in a document).

## Assignment

###  Exercise 1:
Create a new script.
Create a variable x and give it the value 0.
Use a while loop to print the value of x in every iteration of the loop. After printing, the value of x should increase by 1. The loop should run as long as x is smaller than or equal to 10.Example output:

 ### Exercise 2:
 
Create a new script.

Copy the code below into your script.

```
for i in range(10):
# do something here
```

2.1  Print the value of i in the for loop. You did not manually assign a value to i. Figure out how its value is determined.

2.2  Add a variable x with value 5 at the top of your script.

2.3  Using the for loop, print the value of x multiplied by the value of i, for up to 50 iterations.


### Exercise 3:
Create a new script.
Copy the array below into your script.
arr = ["Shikha", "Casper", "Bart", "Ruben", "Ulviye"]

Use a for loop to loop over the array. Print every name individually.




##  Key Terms

range() - The range() function returns a sequence of numbers, starting from 0 by default, and increments by 1 (by default), and stops before a specified number.


##  Resources

[Stack Overflow](https://stackoverflow.com/questions/63942568/creating-an-addition-loop-that-stops-when-it-hits-a-certain-number)

[W3 Schools Range Function](https://www.w3schools.com/python/ref_func_range.asp#:~:text=Definition%20and%20Usage,stops%20before%20a%20specified%20number.)



##  Difficulties

Excercise 1:  
I had muliple difficulties trying to write this code.  I first tried to look at Stack Overflow for some help but this wasn't useful.  Then I consulted my textbook but the I only found the bits that I was already able to code.  I then drafted a question to ChatGPT, stating expliclitly that I did not want any sample code in the answer as I was trying to figure out the problem myself.  It gave me a great answer with some suggestions of what I should consider without giving me the solution.

This was an excellent way to move forward without getting the answer given to me.  A great learning experience and I managed to figure it out by myself without resorting to getting the code from ChatGPT.

Excercise 2 and 3 proved remarkably easy as I've done similar excercises before.


##  Results


### Excercise 1:

My code:

```
x = 0
while x < 10:
      x = x + 1
      print (x)
if x == 10:
    print ('All Done!')

```

The output:

```
1
2
3
4
5
6
7
8
9
10
All Done!
PS C:\Users\elmar>
```

### Exercise 2:

2.1.  My code

```
for i in range(10):
# do something here
    print (i)
```

2.1 Output:

```
PS C:\Users\elmar> & C:/Users/elmar/AppData/Local/Programs/Python/Python312/python.exe c:/Users/elmar/Python.py/loopsEx2.py
0
1
2
3
4
5
6
7
8
9
PS C:\Users\elmar>
```

The value of *i* is determined by the *range* function, which is a built in function in Python that returns a sequence of numbers, starting from 0 by default, and increments by 1 (by default), and stops before a specified number.

2.3  My code:

```
x = 5
for i in range(50):
# do something here
    print (i * x)
```

2.3 Output:

```
0
5
10
15
20
25
30
35
40
45
50
55
60
65
70
75
80
85
90
95
100
105
110
115
120
125
130
135
140
145
150
155
160
165
170
175
180
185
190
195
200
205
210
215
220
225
230
235
240
245
PS C:\Users\elmar>
```
Excercise 3:

My code:

```
for learning_coach in ["Shikha", "Casper", "Bart", "Ruben", "Ulviye"]:
    print (learning_coach)
```

Ouput:

```
Shikha
Casper
Bart
Ruben
Ulviye
PS C:\Users\elmar>
```


