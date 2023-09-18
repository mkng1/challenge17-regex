# How to use Regex to validate Credit Card Numbers

I will introduce Credit Card Number Validation regex code and explain its components.

## Summary

Credit Card Number Validation seemed like an easy choice for regex since it is from 0-9 and 16 digits.
There seems to be more complexities with validations as individual Credit Card Companies have different rules to help validate the numbers without contacting their servers.

## Table of Contents

- [Visa](#visa)
- [Mastercard](#mastercard)
- [American Express](#american-express)

## Regex Components

### Visa

`^4[0-9]{12}(?:[0-9]{3})?$`

All Visa card numbers start with a 4. New cards have 16 digits. Old cards have 13.

^ starts the code, starts with number 4, checks from 0 to 9 twelve times. Optionally it again checks from 0 to 9 three times.
Closes with $

### Mastercard

`^(?:5[1-5][0-9]{2}|222[1-9]|22[3-9][0-9]|2[3-6][0-9]{2}|27[01][0-9]|2720)[0-9]{12}$`

MasterCard numbers either start with the numbers 51 through 55 or with the numbers 2221 through 2720. All have 16 digits.

^ starts the code, checks the first four digits from 5100 up to 5599, or from 2221 up to 2720. Remaining block of numbers is from 0 to 9 twelve times.
Closes with $

### American Express

`^3[47][0-9]{13}$`

American Express card numbers start with 34 or 37 and have 15 digits.

^ starts the code, checks the starting number to be either 34 or 37. Remaining block of numbers is from 0 to 9 thirteen times.


## Author

My name is Michael King and I am studying JavaScript/Full Stack development