
# Mastermind Game

The original Mastermind game with a slight variation.

## Problem Statement

In this code, we will implement the classic [Mastermind](https://twitter.com/) game.
We are going to play it with a slight variation, using numbers instead of colors. Thus each guess will be a 4 digit number, and the key (the number being decoded) will be a 4 digit number. We will also stipulate that no number will repeat in the key. Thus 1234 is a legal key but 1123 is not legal and should not be used in this game.

In our game, you provide the key to be guessed at the start of the program, and then the program allows a player to try and guess the entered key. The program does not generate a random key so you can more easily test your program. Your program does not try to play mastermind, it simply enforces the rules and provides feedback to the player.

On each guess, your program provides two numbers. How many of the 4 numbers in the guess are exactly correct (the correct number in the correct position of the key) and how many of thee guess numbers are in the key but not in the correct position.

The player gets twelve guesses and if they do not get the key in 12 guesses, they lose.

## Program Specifications

Your program will play the mastermind game as follows:

1. Prompt for the 4 digit key we will play with. No error checking here.
2. Prompt the user for a guess.
- check to see if the guess is exactly of length 4
- check to see if the guess contains all numbers
- check to see if the guess has no repeats
3. Any violations of these rules prints out an error message and prompts out for a guess again. Bad input does not count as a guess.
4. End the game if :
- the guess is correct. Print out a winner message
- it was the last guess (the twelfth) and the guess is incorrect. Print out a loser message and the value of the key
5. If no end condition occurs, print out how many of the guess numbers are exactly right (correct number in the correct position) and how many of the guess numbers are correct but not in the correct position.

    **Example.** The key is 1234 and the guess is 4256. The feedback would be 1 number exactly correct (2) and 1 number in the wrong position (4). That is, each digit in the guess produces at most one result (exact or wrong position).

6. You should keep a history of guesses so that the user can see how they are progressing.
7. Continue the game until an end condition occurs.

## Sample Run

Here,
- _exist_ are those numbers that are in the key but not in the right position.
- _position_ are those numbers that are correct and in the right position.

The key will be defined before as **1234** for practice session.


```
Enter guess: 4321
4321 : exist: 4, position: 0

Enter guess: 5678
4321 : exist: 4, position: 0
5678 : exist: 4, position: 0

Enter guess: 1243
4321 : exist: 4, position: 0
5678 : exist: 4, position: 0
1243 : exist: 4, position: 0

Enter guess: 123
Guess must be of 4 digits!

Enter guess: 12345
Guess must be of 4 digits!

Enter guess: 1b34
Invalid input. Try again.

Enter guess: 1123
Guess must not have duplicate digits!

Enter guess: 1234
4321 : exist: 4, position: 0
5678 : exist: 4, position: 0
1243 : exist: 4, position: 0
1234 : exist: 4, position: 0
You guessed it right!
You did it in 4 guesses.
```

