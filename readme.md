🐍 Day 25 – NATO Phonetic Alphabet Project

This project is part of the 100 Days of Code: The Complete Python Pro Bootcamp by Angela Yu on Udemy.

📌 Project Overview

In this project, we learn and apply

✅ List Comprehension

✅ Dictionary Comprehension

✅ Reading CSV files using Pandas

✅ Data transformation

✅ Exception handling

The goal is to convert any user-input word into its corresponding NATO phonetic alphabet code words.

📂 Project Structure
Day-25-NATO-Alphabet/
│
├── main.py
├── nato_phonetic_alphabet.csv
└── README.md
🧠 How It Works

The program reads a CSV file containing NATO phonetic codes.

It creates a dictionary mapping letters to their phonetic code words.

The user inputs a word.

The program converts each letter into its NATO equivalent.

If the user enters invalid characters (numbers/symbols), it asks them to try again.

📊 Example NATO CSV Format
letter	code
A	Alfa
B	Bravo
C	Charlie
💻 Example Run
Enter a word: GAURANG
['Mike', 'Oscar', 'Hotel', 'India', 'Tango']
🧾 Core Code Logic
import pandas

data = pandas.read_csv("nato_phonetic_alphabet.csv")
phonetic_dict = {row.letter: row.code for (index, row) in data.iterrows()}

def generate_phonetic():
    word = input("Enter a word: ").upper()
    try:
        output_list = [phonetic_dict[letter] for letter in word]
    except KeyError:
        print("Sorry, only letters in the alphabet please.")
        generate_phonetic()
    else:
        print(output_list)

generate_phonetic()
🎯 Concepts Practiced
🔹 List Comprehension
new_list = [new_item for item in list]
🔹 Dictionary Comprehension
new_dict = {new_key:new_value for item in list}
🔹 Data Handling with Pandas

Reading CSV files

Iterating through DataFrame rows

🚀 How to Run

Install Python 3

Install Pandas (if not installed)

pip install pandas

Run the program:

python main.py
📚 Learning Outcome

By completing this project, you will:

Understand Python comprehensions deeply

Work with external CSV data

Handle exceptions properly

Improve problem-solving skills

Author - Gaurang Sharma
