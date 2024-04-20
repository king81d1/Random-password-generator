# Random-password-generator
#
import random
import string

print("Welcome \nThis is an application for generating random passwords")

length = int(input("What is the length of the password? "))
characters = int(input("How many characters are there in the password? "))
num = int(input("How many numbers do you want? "))
codes = int(input("How many symbols do you want? "))

if num + codes + characters != length:
    print("Password length doesn't make sense")
else:
    char = string.ascii_letters
    random_characters = ''.join(random.choices(char, k=characters))
    nu = string.digits
    random_num = ''.join(random.choices(nu, k=num))
    cod = string.punctuation
    random_codes = ''.join(random.choices(cod, k=codes))
    
    password = random_characters + random_codes + random_num
    password = list(password)
    random.shuffle(password)
    password_str = ''.join(password)
    print(password_str)
