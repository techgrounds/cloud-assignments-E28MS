## Subject

You might have seen a folder in the drive named ‘Pls fix’. This folder contains 16 very small Python scripts that are somehow broken. 

## Assignment
Your job is to fix the mistake by changing only 1 or 2 small things within the script. The expected result for each script is written in the multi-line comment at the top of the script.

This exercise is meant as a little fun puzzle, but also to help you learn to troubleshoot existing code, so even though they are optional, they are recommended to do.


Of course, you can get to the expected results by simply deleting all the code and using a print function, but that would defeat the purpose of this exercise.


The exercises are approximately ordered based on difficulty level, but you might want to skip one if you get stuck and go back to that one later

##  Results

### Excercise 1:

Code provided:
```
The output should be:
hello Casper
hello Floris
hello Esther
'''
foo = 'hello'
ls = ['Casper', 'Floris', 'Esther']
for name in ls:
	print(loo,name)
```

My corrected code:
```
The output should be:
hello Casper
hello Floris
hello Esther
'''
foo = ('hello')
ls = ['Casper', 'Floris', 'Esther']
for name in ls:
	print(foo,name)
```
Output:
```
hello Casper
hello Floris
hello Esther
```

### Excercise 2:

Faulty code provided:
```
'''
The output should be:
100
'''
foo = 20
bar = '80'
print(foo + bar)
```

My corrected code:
```
'''
The output should be:
100
'''
foo = 20
bar = int('80')
print(foo + bar)
```

Output:
```
100
PS C:\Users\elmar>
```

### Excercise 3:

Faulty code provided:
```
The output should be:
30
'''
foo = 20
for i in range(10):
	foo -= 1

print(foo)
```

My code:

'''
The output should be:
30
'''
foo = 20
for i in range(10):
	foo += 1

print(foo)
```

Output:
```
30
PS C:\Users\elmar> 
```

### Excercise 4:

Faulty code:

```
'''
The output should be:
there are 0 kids on the street
there are 1 kids on the street
there are 2 kids on the street
there are 3 kids on the street
there are 4 kids on the street
'''
foo = 0
while foo <= 5:
	print('there are', foo, 'kids on the street')
	foo += 1
 ```

My code:

```
foo = 0
while foo <= 4:
	print('there are', foo, 'kids on the street')
	foo += 1
 ```

Output:

```
there are 0 kids on the street
there are 1 kids on the street
there are 2 kids on the street
there are 3 kids on the street
there are 4 kids on the street
```

### Excercise 5:

Faulty code provided:

```
'''
The output should be:
Star Wars
'''
ls = ['Lord of the rings', 'Star Trek', 'Iron Man', 'Star Wars']
print(ls[4])
```

My code:
```
'''
The output should be:
Star Wars
'''
ls = ['Lord of the rings', 'Star Trek', 'Iron Man', 'Star Wars']
print(ls[3])
```

Output:

```
Star Wars
PS C:\Users\elmar> 
```

### Excercise 6:

Faulty code provided:

```
The output should be:
80
'''
foo = 80
if foo < 30:
	print(foo)
else:
	print('big number wow')
elif foo < 100:
	print(foo)
 ```

My code:

```
foo = 80
if foo < 30:
	print(foo)
elif foo > 100:
	print('big number wow')
else:	
	print(foo)
 ```

### Excercise 7:

```
'''
The output should be:
['Dog', 'Cat', 'Fly']
'''
ln = ['Dog', 'Cat', 'Elephant', 'Fly', 'Horse']
short_names = []

for animal in ln:
	if len(animal) == 3:
		short_names.append(animal)
	short_names = []

print(short_names)
```

### Excercise 8:

```
The output should be:
['Dog', 'Cat', 'Fly']
'''
ln = ['Dog', 'Cat', 'Elephant', 'Fly', 'Horse']
short_names = []

for animal in ln:
	if len(animal) == 3:
		short_names.append(animal)
	short_names = []

print(short_names)
```

My code:
```
ln = ['Dog', 'Cat', 'Elephant', 'Fly', 'Horse']
short_names = []

for animal in ln:
	if len(animal) == 3:
		short_names.append(animal)
	
print(short_names)
```

Output:

```
['Dog', 'Cat', 'Fly']
PS C:\Users\elmar> 
```


