Python Input Validation Utilities

This project contains a collection of simple Python functions for validating and extracting information from text.

The functions use Python's built-in "re" (regular expression) module to check whether input follows a specific pattern.


 Features

This project provides four main utilities:

- Validate location names
- Validate geographical coordinates
- Extract numbers from text
- Validate dates



Requirements

You only need Python installed.

The project uses Python's built-in "re" module, so no external packages are required.

import re



Functions

1. "is_valid_location_name(text)"

Checks whether a location name contains only:

- Letters
- Spaces
- Commas
- Hyphens

Example

is_valid_location_name("Abuja")

Returns:

True

Another example:

is_valid_location_name("Suleja, Niger")

Returns:

True

An input containing numbers or unsupported symbols will return "False".

is_valid_location_name("Abuja123")

Returns:

False



2. "is_valid_coordinates(text)"

Checks whether text looks like a pair of geographical coordinates.

The expected format is:

latitude, longitude

Example

is_valid_coordinates("9.0765, 7.3986")

Returns:

True

It also accepts negative coordinates:

is_valid_coordinates("-6.5244, 3.3792")

Returns:

True



3. "extract_numbers(text)"

Finds numbers inside a piece of text and returns them as a list.

Example

extract_numbers("The coordinates are 9.0765, 7.3986")

Returns:

['9.0765', '7.3986']

It can also find negative numbers:

extract_numbers("Temperature is -5.5 degrees")

Returns:

['-5.5']


4. "is_valid_date(text)"

Checks whether a date follows the format:

YYYY-MM-DD

Example

is_valid_date("2026-10-07")

Returns:

True

An incorrectly formatted date will return "False".

is_valid_date("07-10-2026")

Returns:

False


Example Usage

You can test all the functions with the following code:

print(is_valid_location_name("Abuja"))
print(is_valid_coordinates("9.0765, 7.3986"))
print(extract_numbers("The coordinates are 9.0765, 7.3986"))
print(is_valid_date("2026-10-07"))

Expected output:

True
True
['9.0765', '7.3986']
True


 What This Project Demonstrates

This project is useful for learning several important Python concepts:

- Functions
- Conditional statements
- Regular expressions
- Strings
- Lists
- Boolean values
- Input validation
- Pattern matching
- The "re" module



Regular Expressions

Regular expressions, also called regex, are patterns used to search, match, and validate text.

For example:

r'^\d{4}-\d{2}-\d{2}$'

is used to check whether a date follows the "YYYY-MM-DD" format.

The "^" means the pattern must start at the beginning of the text.

The "$" means the pattern must end at the end of the text.




