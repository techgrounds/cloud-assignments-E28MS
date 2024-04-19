## Subject
The mini project incorporates several of the concepts we have worked at over this week to put some of them together.

## Assignment

### Number Guessing:

Generate a random number between 1 and 100 (or any other range).

The player guesses a number. For every wrong answer the player receives a clue.

When the player guesses the right number, display a score.

##  Key Terms

Initializing variables: This is when you assign a value to a variable before it get's used in a  program in order to ensure that they have a valid starting point.

Global and local variables: Global variables exist outside of functions. Local variables exist within functions.

##  Resources

[Digital Ocean - Using Variables in Python](https://www.digitalocean.com/community/tutorials/how-to-use-variables-in-python-3)

##  Results

My code:
```
# Generate a random number between 1 and 100:
import random
number = random.randint(1,100)
guess = 0 # initialise guess
tries = 0 # initialise tries
while guess != number:
    guess = int(input('What number would you like to guess?'))
    tries = tries +1
    if guess > number:
        print ('Guess lower!')
    elif guess < number:
        print ('Guess higher!')
    else:
        print('Tadaaaa! We have a winner')
        print ('Number of tries:',tries)
```
Output Game 1:
```
What number would you like to guess?50
Guess lower!
What number would you like to guess?25
Guess lower!
What number would you like to guess?20
Guess higher!
What number would you like to guess?24
Guess lower!
What number would you like to guess?23
Guess lower!
What number would you like to guess?22
Guess lower!
What number would you like to guess?21
Tadaaaa! We have a winner
Number of tries: 7
```

Output Game 2:

```
What number would you like to guess?75
Guess lower!
What number would you like to guess?50
Guess lower!
What number would you like to guess?25
Guess lower!
What number would you like to guess?20
Guess lower!
What number would you like to guess?15
Guess higher!
What number would you like to guess?17
Guess higher!
What number would you like to guess?18
Guess higher!
What number would you like to guess?19
Tadaaaa! We have a winner
Number of tries: 8
```
