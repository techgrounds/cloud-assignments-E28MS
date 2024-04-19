## Subject

You might have seen a folder in the drive named ‘Pls fix’. This folder contains 16 very small Python scripts that are somehow broken. Your job is to fix the mistake by changing only 1 or 2 small things within the script. The expected result for each script is written in the multi-line comment at the top of the script.

This exercise is meant as a little fun puzzle, but also to help you learn to troubleshoot existing code, so even though they are optional, they are recommended to do.


Of course, you can get to the expected results by simply deleting all the code and using a print function, but that would defeat the purpose of this exercise.


The exercises are approximately ordered based on difficulty level, but you might want to skip one if you get stuck and go back to that one later

## Assignment

##  Key Terms

##  Resources

##  Difficulties

##  Results

Excercise 1:

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


