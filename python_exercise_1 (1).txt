# Exercise:01:Write a program to find the lenght of the variable name Variable,
# name="Hello there"
import random

name = "Hello there"
print(len(name))

# Exercise:02:Write a program to find the type of the variable name,
# name="Hello there"

name = "Hello there"
print(type(name))


# Exercise:03:: Write a function that takes 2 numbers as arguments (age of two brothers)
# and find who is elder
def elder(age_bro1, age_bro2):
    if age_bro1 > age_bro2:
        return "Bro 1 is elder."
    elif age_bro1 < age_bro2:
        return "Bro 2 is elder."
    else:
        return "Both brothers are of the same age."


age_brother1 = 25
age_brother2 = 20
print(elder(age_brother1, age_brother2))

# Exercise 04: Write a program to find the index of 7
# numbers=[3, 5, 1, 9, 7, 2, 8 ]

numbers = [3, 5, 1, 9, 7, 2, 8]

print(numbers[6])

# Exercise:05: Write a program to sort the numbers in Ascending order
# numbers=[3, 5, 1, 9, 7, 2, 8 ]

number = [3, 5, 1, 9, 7, 2, 8]
number.sort()
print(number)

# ,Exercise:06:: Write a function named “isLandscape” that takes 2 numbers (image width
# and height) as arguments and the function returns Landscape if the image width has a
# higher value than height. Returns Portrait otherwise
# Hints: Use condition inside the function

from random import *


def islandscape(image_width, image_height, Landscape="Landscape", Portait="Portait"):
    if image_width > image_height:
        return Landscape
    elif image_height > image_width:
        return Portait
    else:
        print("Square box")


width = randint(500, 1000)
height = randint(500, 1000)

print(islandscape(width, height))


# Exercise:07:Exercise 07: FizzBuzz Exercise
# Write a function that takes 1 number as argument. The function should return “Fizz” if
# the number is divisible by 3, the function should return “Buzz” if the number is divisible
# by 5, the function should return “FizzBuzz” if the number is divisible by both 5 and 3,
# otherwise return “Not a Fizz-buzz number”
# Hints: Use condition inside the function

def Fizzbuzz(number, Fizz="fizz", Buzz="Buzz"):
    number = int(input("Enter number :"))
    if number % 3 == 0:
        return Fizz
    elif number % 5 == 0:
        return Buzz
    if number % 3 == 0 and number % 5 == 0:
        return Fizz, Buzz
    else:
        Not_fizz_buzz = "Not a Fizz-buzz number"
        return Not_fizz_buzz


print(Fizzbuzz(number))

"""OR"""


def Fizzbuzz(number, Fizz="fizz", Buzz="Buzz"):
    if number % 3 == 0:
        return Fizz
    elif number % 5 == 0:
        return Buzz
    if number % 3 == 0 and number % 5 == 0:
        return Fizz, Buzz
    else:
        Not_fizz_buzz = "Not a Fizz-buzz number"
        return Not_fizz_buzz


number = randint(1, 10000000000)

print(Fizzbuzz(number))


# Exercise 08: Guessing game
# Write a function that takes a number 1 to 9 from the user input (use input function inside
# a function). Store a number in a variable (let’s assume 6). If the input value is less than
# the variable, print (your guess is almost there), if the input value is greater than the
# variable, print - your guess is higher, if the input value and variable are equals, print -
# Your Guess Is Correct!

def Gussing_game():
    while True:
        variable = 6
        chose_number=int(input("Guess the number"))
        chose_num=chose_number
        if chose_num < variable:
          print("You are almost there")
        elif chose_num > variable:
           print("Your guess is higher")
        elif chose_num == variable:
          print("Your guess is correct")
        else:
             print("Enter a integer number")
        if chose_num!=variable:
            continue
        else:
            break

print(Gussing_game())



#Exercise 09: Find if 6 available in the list [‘4, 8, 7, 4,3,6,2,1,9’]

list=['4,8,7,4,3,6,2,1,9']

string=''.join(list)

for i in string:
    if i =='6':
        print("6 found")

