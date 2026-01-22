# romannumeralconverter

Roman Numeral Converter

Software Development Life Cycle (SDLC) Documentation

Project Overview

This project is a command-line Roman Numeral Converter implemented in Python.
It supports two modes of operation:

1. Integer to Roman numeral


2. Roman numeral to Integer



The system validates all inputs, follows standard Roman numeral rules, and uses no external libraries.


---

1. Planning Phase

Project Requirements

A command-line tool with a simple, user-friendly interface.

Two conversion modes:

Integer → Roman numeral

Roman numeral → Integer


Input validation:

Integers must be between 1 and 3999.

Roman numerals must follow valid Roman numeral rules.


No external libraries allowed.

Accurate and reliable conversions.


Project Goal

To build a lightweight and accurate Roman numeral converter that is easy to use, error-resistant, and follows standard Roman numeral conventions.


---

2. Analysis Phase

Roman Numeral Rules

Roman numerals are based on the following symbols:

Symbol	Value

I	1
V	5
X	10
L	50
C	100
D	500
M	1000


Subtractive notation is supported:

IV = 4

IX = 9

XL = 40

XC = 90

CD = 400

CM = 900


Conversion Logic

Integer to Roman:

Use a list of value–symbol pairs in descending order.

Repeatedly subtract values and append symbols.


Roman to Integer:

Map Roman symbols to values.

Iterate through the string.

If a symbol is smaller than the next, subtract it; otherwise, add it.



User Interaction Flow

1. User selects conversion mode.


2. User enters a value.


3. Program validates input.


4. Conversion result is displayed.




---

3. Design Phase

Program Structure

Main Function

main()

Handles menu display

Accepts user input

Calls appropriate conversion functions

Manages program loop and error handling



Functions

int_to_roman(num)

Input: Integer

Output: Roman numeral string

Uses the following mapping:


roman_map = [
    (1000, 'M'), (900, 'CM'), (500, 'D'), (400, 'CD'),
    (100, 'C'), (90, 'XC'), (50, 'L'), (40, 'XL'),
    (10, 'X'), (9, 'IX'), (5, 'V'), (4, 'IV'), (1, 'I')
]

roman_to_int(s)

Input: Roman numeral string

Output: Integer

Uses:


roman_values = {
    'I': 1, 'V': 5, 'X': 10,
    'L': 50, 'C': 100,
    'D': 500, 'M': 1000
}

Iterates through the string and applies subtractive logic.


is_valid_roman(s)

Checks:

Valid characters

Proper Roman numeral ordering and rules



Interface Design

Menu-driven command-line interface

Clear prompts and error messages

Continuous loop until user exits



---

4. Implementation Phase

The project is implemented in Python using the following functions:

main()

int_to_roman(num)

roman_to_int(s)

is_valid_roman(s)


All function names and variables match the design specification exactly.


---

5. Testing Phase

Manual Test Cases

Test Case	Expected Output

int_to_roman(1990)	MCMXC
roman_to_int("MCMXC")	1990
int_to_roman(1)	I
int_to_roman(3999)	MMMCMXCIX
Invalid Roman "IIX"	Error / Validation Failure


The program was tested in a loop with multiple valid and invalid inputs.


---

6. Maintenance Phase

Future Improvements

Support for larger numeric ranges

Graphical User Interface (GUI)

Improved Roman numeral validation logic

Performance optimizations


Maintenance Activities

Bug fixes for edge cases

Input validation improvements

Feature enhancements based on user feedback



---
