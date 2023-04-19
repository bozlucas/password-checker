Password Checker
================

Description
-----------

This Python code checks if a password has been exposed in data breaches by consulting the Pwned Passwords API. The Pwned Passwords API contains a database of over 500 million passwords that have been compromised in data breaches.

The code takes in a password as input and calculates its SHA-1 hash. It then sends the first 5 characters of the hash to the Pwned Passwords API to retrieve a list of password hashes that match the prefix. The code then searches the list for the full hash of the input password and returns the number of times it appears in the database. If the password is found in the database, the code recommends the user to change it.

Dependencies
------------

This code requires the following modules:

-   `requests`
-   `hashlib`
-   `sys`

These modules can be installed using pip.

Usage
-----

The code can be run from the command line using the following syntax:

Copy code

`python password_checker.py password1 password2 password3 ...`

The code will check each password in turn and return whether it has been compromised in a data breach. If a password is found in the database, the code recommends changing the password to a more secure one.