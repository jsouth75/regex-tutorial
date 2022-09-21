# Regex-tutorial

Regex is short for regular expressions. The special characters can be confusing and/or intitmidating at first, but are used to define a specific search pattern. Regex is a sequence of characters that define a search pattern and can be used to find certain patterns and replace a character or sequence of characters within a string. It can also be used to validate input such as emails.

## Summary

We will break down the following regex, which is to validate the input of a user's email address. 
 - ` /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

    * `^` starts the beginning search of our first "group" of characters.
    * `()` the first capturing group
    * `[a-z0-9_\.-]` characters inside a bracket expression, which is searching for lowercase letters and numbers between 0-9 and special characters _ \ . -
    * `+` which is a quantifier to match 1 or more characters
    * `@` matches the @ symbol 
    * `()` the second capturing group
    * `[\da-z\.-]` characters inside this bracket expression need to match any numerical digit 0-9, lowercase letters, and special characters \ . - `+` which is a quantifier to match 1 or more characters
    * `\.` character that is looking for an actual period
    * `()` the third capturing group
    * `[a-z\.]` characters inside the third bracket expression need to match lowercase letters and special characters \ . 
    * `{2,6}` this quantifier is looking for a match of a minimum of 2 characters and a maximum of 6 characters
    * `$` searches the end of the string, which is the curly braces

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

The sequence of characters for an email verification must be wrapped with slash characters `/`.  Also, any special character inside bracket notations looses it's special meaning and becomes the actual character. 

### Anchors

Anchors or position characters are `^` and `$` and are used at the beginning and end of the pattern of characters.  
- `^` - searches the beginning of the string
- `$` - searches the end of the string

### Quantifiers

Quantifiers search the preceding characters and set minimum and maximum limits of characters to match.
- `*` - 0 or more times
- `+` - 1 or more times
- `?` - 0 or one time
- `{}` - provide 3 different ways to search characters 
    1.  { a } exact number of times
    2.  { a, } at least (minimum) number of times
    3.  { a, b } minimum and maximum number of times

### OR Operator

- `|` is the OR operator and is used as either/or instead of an absolute.  
For example, (123):(abc) will only match "123:abc" and (1|2|3):(a|b|c) could match "321:cba", "a:2", "213:cba", "3:a", etc. 

### Character Classes

Character classes defines a set of characters
- `.` - matches any single character except for newline character (\n)
- `\d` - matches numerical digits (0-9)
- `\w` - matches alphanumeric characters such as (a-zA-Z0-9)
- `\s` - matches single white space characters
- `\D` - oppostie of `\d`, which matches any non numerical digit
- `\W` - opposite of `\w`, which matches any non alphanumerical characters
- `\b` - searches complete/whole words
- `\.` - the period is literal

### Flags

Regex is considered a literal and must be wrapped in slash `/` characters, but the flags are an exception to the rule.  Flags are to be placed at the end after the second slash `/` character and define addtional limits.  Here are 3 of the most common ones. 
- `g` - global search, which matches against all possible matches
- `i` - case-insensitive
- `m` - multi-line search 

### Grouping and Capturing

Regex can grow more complex and have mulitple parts of a string, so to break these up we use grouping or capturing with parentheses, which is known as subexpressions

### Bracket Expressions

The square brackets are used to represent a range of characters to search, such as 
- `[a-z0-9_\.-]` will match all lower case letters, numbers between 0-9, and special characters _ \ . -

### Greedy and Lazy Match

We discussed quantifiers earlier, which are naturally greedy.  This means they match as many occurences of a pattern as possible, but we can make these quantifiers lazy by adding the `?` symbol at the end of the quantifier.  This will cause the regex to match as few occurences as possible.  

### Boundaries

We discussed word boundaries in the character section. The symbols `\b` is used to search for complete and whole words.  For example...
`\b\w{6}\b` will search for any alphanumeric characters 6 characters long. 

### Back-references

Remember we discussed grouping and capturing above with parentheses.  Back-reference can match the previous capturing groups by referencing the capturing group at the end of your regex with a backslash and the referency number.  For instance, scan to the regex from left to right and count the capturing groups.  The first capturing group is back-reference one and so forth down the line.  
### Look-ahead and Look-behind

These are also called lookaround, and only assert if a match is possible or not. They allow you to create expressions that may otherwise be impossible to create otherwise without them. 

## Author
- Jason South <br/>
- GitHub username: jsouth75 <br/>
- Email: jason.south@me.com

