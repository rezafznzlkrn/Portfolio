import random

def guess_the_number():
    print("Welcome to the Number Guessing Game!")
    number_to_guess = random.randint(1, 100)
    attempts = 0
    guessed = False
    
    while not guessed:
        try:
            user_guess = int(input("Guess a number between 1 and 100: "))
            attempts += 1
            
            if user_guess < 1 or user_guess > 100:
                print("Your guess is out of bounds! Try again.")
            elif user_guess < number_to_guess:
                print("Too low! Try again.")
            elif user_guess > number_to_guess:
                print("Too high! Try again.")
            else:
                guessed = True
                print(f"Congratulations! You've guessed the number in {attempts} attempts.")
        except ValueError:
            print("Invalid input. Please enter an integer.")
    
if __name__ == "__main__":
    guess_the_number()
