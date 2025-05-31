import random
import string

print("Welcome to Password Picker")

def generate_password(length, use_numbers, use_special_chars, use_uppercase, use_lowercase):
    characters = ""
    if use_lowercase:
        characters += string.ascii_lowercase
    if use_uppercase:
        characters += string.ascii_uppercase
    if use_numbers:
        characters += string.digits
    if use_special_chars:
        characters += string.punctuation

    if not characters:
        print("Error: You must select at least one character type.")
        return None

    password = ''.join(random.choice(characters) for _ in range(length))
    return password

while True:
    try:
        desired_length = int(input("Enter desired password length: "))
        if desired_length <= 0:
            print("Password length must be a positive number.")
            continue
    except ValueError:
        print("Invalid input. Please enter a number for length.")
        continue

    use_numbers_input = input("Include numbers? (Y/N): ").upper()
    use_numbers = use_numbers_input == 'Y'

    use_special_chars_input = input("Include special characters? (Y/N): ").upper()
    use_special_chars = use_special_chars_input == 'Y'

    use_uppercase_input = input("Include uppercase letters? (Y/N): ").upper()
    use_uppercase = use_uppercase_input == 'Y'

    use_lowercase_input = input("Include lowercase letters? (Y/N): ").upper()
    use_lowercase = use_lowercase_input == 'Y'

    password = generate_password(desired_length, use_numbers, use_special_chars, use_uppercase, use_lowercase)

    if password:
        print("Your Password is: %s" % password)

    response = input("Would you like another password? Type Y or N: ").upper()
    if response == 'N':
        break

print("Thank you for using Password Picker!")
