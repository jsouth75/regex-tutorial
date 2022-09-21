# Regex-tutorial

Regex is short for regular expressions. The special characters can be confusing and/or intitmidating at first, but are used to define a specific search pattern. Regex is a sequence of characters that define a search pattern and can be used to find certain patterns and replace a character or sequence of characters within a string. It can also be used to validate input such as emails.

## Summary

We will break down the following regex, which is to validate the input of a user's email address. 
 ` /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

The sequence of characters must be wrapped with slash characters `/`.  Also, any special character inside bracket notations looses it's special meaning and becomes the actual character. 

### Anchors

Anchors or position characters are `^` and `$` and are used at the beginning and end of the pattern of characters.  Also, `\b` is used as a word boundry.  
- `^` searches the beginning of the string
- `$` searches the end of the string
- `\b` searches complete/whole words

### Quantifiers

Quantifiers search the preceding characters and set minimum and maximum limits of characters to match.
- `*` 0 or more times
- `+` 1 or more times
- `?` 0 or one time
- `{}` provide 3 different ways to search characters 
    1.  { a } exact number of times
    2.  { a, } at least (minimum) number of times
    3.  { a, b } minimum and maximum number of times

### OR Operator

- `|` is the OR operator and is used as either/or instead of an absolute.  
For example, (123):(abc) will only match "123:abc" and (1|2|3):(a|b|c) could match "321:cba", "a:2", "213:cba", "3:a", etc. 

### Character Classes

Character classes defines a set of characters
- `.` matches any single character except for newline character (\n)
- `\d` matches numerical digits (0-9)
- `\w` matches alphanumeric characters such as (a-zA-Z0-9)
- `\s` matches single white space characters
- `\D` oppostie of `\d`, which matches any non numerical digit
- `\W` opposite of `\w`, which matches any non alphanumerical characters

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
