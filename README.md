# data_saver.py

import json

# User input
name = input("Enter your name: ")
address = input("Enter your address: ")
debit_card = input("Enter your debit card number: ")
credit_card = input("Enter your credit card number: ")
password = input("Enter your password: ")

# Data dictionary
data = {
    "name": name,
    "address": address,
    "debit_card": debit_card,
    "credit_card": credit_card,
    "password": password
}

# Save to JSON file
with open("my_secure_data.json", "w") as file:
    json.dump(data, file)

print("Your data has been saved locally in 'my_secure_data.json'")
