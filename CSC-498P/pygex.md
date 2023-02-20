# Using regex in python
## Introduction
Regular expressions are a powerful tool for matching patterns in text. They are used in many programming languages, and are often used in text editors and other programs to search for text.

Python has a built-in module for regular expressions, called `re`. This module is very powerful, and can be used to do a lot of different things. In this tutorial, we will cover the basics of using regular expressions in Python.

### Steps
1. Import the `re` module
2. Create the regex patern and store it in a string
3. use the `re.match()` function to match the pattern to a string and store it in a var
4. Manipulate the var to get the desired output

### Functions
> Use r"pattern" in the method because some characters have special meaning in regex that can be escaped with a backslash.

- `re.match()` - matches a pattern to a string returns a match object
- `re.findall()` - finds all instances of a pattern in a string returns a list of matches
- `re.split()` - splits a string into a list of substrings where the pattern matches
- `re.sub()` - replaces all instances of a pattern in a string with a replacement string
- `re.subn()` - same as `re.sub()` but returns a tuple with the new string and the number of replacements
- `re.search()` - searches a string for a pattern and returns a match object
### Manipulating the match object
- `match.group()` - returns the string matched by the pattern
- `match.start()` - returns the starting index of the match
- `match.end()` - returns the ending index of the match
- `match.span()` - returns a tuple containing the start and end index of the match
- `match.string` - returns the string passed into the function
- `match.re` - returns the regex pattern used to create the match object