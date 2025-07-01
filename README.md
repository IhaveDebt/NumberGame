🎮 Guess the Number Game
Author: Rainers Vid (https://github.com/IhaveDebt)

A simple terminal game where you try to guess a number between 1 and 100.
Features:
- Random number generation
- User input validation
- Attempts counter
- Fun terminal experience

To play: Run this file with Python and follow the instructions!
"""

import random

def main():
    print("🎲 Welcome to the Number Guessing Game!")
    print("I'm thinking of a number between 1 and 100...")
    number = random.randint(1, 100)
    attempts = 0

    while True:
        try: 
            guess = int(input("Enter your guess: "))
            attempts += 1

            if guess < number:
                print("Too low! Try again.")
            elif guess > number:
                print("Too high! Try again.")
            else:
                print(f"\n🎉 Correct! The number was {number}.")
                print(f"You guessed it in {attempts} tries. Great job, Rainers!")
                break
        except ValueError:
            print("❌ Please enter a valid number.")

if __name__ == "__main__":
    main()
