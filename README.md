# Guess_The_Number

import random

# Create variables
input_number = 0
check_number = 0
generate_random_number = 0
result = 0

# Check input:
def check_number_input():
    global input_number
    global check_number
    while True:
        try:
            input_number = int(input())
            break
        except ValueError:
            print('Please use digits')

# Create random number
def create_random_number():
    global input_number
    global check_number
    global generate_random_number
    generate_random_number = random.randint(0, check_number)
    print(generate_random_number)

# Try to guess the number
def guess_the_number():
    global input_number
    global check_number
    global result
    global generate_random_number
    guess_the_num = int(input())
    while True:
        if generate_random_number == guess_the_num:
            print('You win')
            break
        else:
            if generate_random_number > guess_the_num:
                print('Try UP')
                guess_the_num = int(input())
            else:
                print('Try Down')
                guess_the_num = int(input())
                
# Start the functions
check_number_input()
create_random_number()
guess_the_number()
