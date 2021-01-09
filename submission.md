# pythonchallengeteam1
Python challenge submission for team 1

# Title: Intro to Python Challenge 1
# Modified By: Memma Uponi, Grace Gong, Khushi Adukia 
# Team: 1
# Date: 01/09/21

# Program randomly generates a number from user's given range and prompts the user to guess the number until a correct guess is given

import random

#User prompts to determine variables
user_range1 = input(" Choose the starting value of your range: ")
user_range2 = input(" Choose the ending value of your range: ")

#Converting values to integers
user_range1 = int(user_range1)
user_range2 = int(user_range2)


#Computer generating random number
if user_range1 < user_range2:  #processes the possibility of the starting value being greater than ending value
            comp_guess = random.randint(user_range1, user_range2 + 1) 
else:
            comp_guess = random.randint(user_range2, user_range1 + 1)


#Processing user guesses
while True:
            try:
                        guess = input("Guess a number from your chosen range: ")
                        
                        if guess.isdigit():
                                    guess = int(guess)
                                    if guess == comp_guess:
                                                print("Congratulations! You guessed the number")
                                                break
                                    
                                    else: 
                                                if guess > comp_guess:
                                                            print("Incorrect. The number is higher")
                                                
                                                elif guess < comp_guess:
                                                            print("Incorrect. The number is lower")
                        else:
                                    print("Error.Only integers are allowed")
            except ValueError:
                        print("Invalid Input")
#end
