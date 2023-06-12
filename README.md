gi#THE CONCEPT OF THIS PROJECT
#This project is strictly for fun. The aim is to make a creative guess between
#1-10. Have fun!!!!!!

import random #An inbuilt function that aids this process

def guess(x):
    random_number = random.randint(1 , x )
    guess = 0
    while guess != random_number:
        guess = int(input(f"Guess a number between 1 and {x}: "))
        print(guess)
        if guess < random_number:
            print("Oops!!, Too low, try again")
        elif guess > random_number:
            print("Oops!!!, Too high, try again") 
    print(f"You guessed correctly!! {random_number} proceed for you cashout")   

 def computer_guess(x):
     low = 1
     high = x
     feedback = ''
     while feedback != 'c':
         if low !=high:
             guess = random.randint(low, high)
         else:
             guess = low
         feedback = input(f" is {guess} too high (H), too low (L), or correct (C)??").lower()
         if feedback == 'h' :
             high = guess - 1
         elif feedback == "1":
             low = guess + 1

     print(f"The computer guessed your number, {guess}, correctly")
guess(10)
