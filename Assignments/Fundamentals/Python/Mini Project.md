## Subject

## Assignment

### Number Guessing:

Generate a random number between 1 and 100 (or any other range).

The player guesses a number. For every wrong answer the player receives a clue.

When the player guesses the right number, display a score.

##  Key Terms

Initializing variables: 

##  Resources

[Digital Ocean - Using Variables in Python](https://www.digitalocean.com/community/tutorials/how-to-use-variables-in-python-3)

##  Difficulties

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
