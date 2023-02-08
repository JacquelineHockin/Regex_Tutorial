# Understanding Regex

A regular expression, or a regex, is a set of characters that forms a pattern. The search pattern allows you to describe what you are looking for when you search for data in a text. In addition to performing text searches, a regex can perform text replace operations. A regex can be anything from a complex pattern to a single character, using numbers, letters, special characters, and quantifiers. 

Completing a search is essentially all about finding patterns because at the core of a search engine (which uses search algorithms), are searches for patterns in text. Most commonly, a regex is used in pattern matching for an email address, username, id, url, etc. So, if you wanted to check the validity of a username when completing an online form, a regex can tell you fairly immediately if the username matches a valid pattern. 

## Summary

The following is the regular expression for validating a user's email. We will be examining the components of the regex in this tutorial. 

The regex:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

This regular expression contains a string of characters that each represents a specific parameter in the search pattern. Each character's parameters and their usage will be covered here.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Bracket Expressions](#bracket-expressions)
- [Grouping and Capturing](#grouping-and-capturing)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors

Our regex is enclosed by anchor symbols on either end, ^ to represent the beginning of the string and $ to represent the end of the string. 

### Quantifiers

Quantifiers specify how many instances of a charactor(s) must be present. 
Our expression contains two quantifiers, located to the right of the expression. We have {2,6} at the end of the expression, indicating that the string can be no less than 2 and no more than 6 characters. To indicate that the preceding element may repeat or match one or more times, we also have two (+) near the middle of the expression.

### Character Classes

In our expression we have \d which indicates any character that is a digit [0-9]. 
Character classes simply define commonly used character classes using convenient shorthands. 

### Bracket Expressions

Any expression found within brackets ([]) that indicates character groups to match is called a bracket expression. Our expression has three:
`[a-z0-9_\.-], [\da-z\.-], and [a-z\.]`

[a-z] indicates any lower case letter from a-z.
[0-9] indicates any number between 0 and 9. 
[_\.-] indicates what special characters can be used.

### Grouping and Capturing

Regular expressions are commonly broken up into subsections (substrings) using parenthesis. Our expression is made up of three groups that make up the regular expression. 

`([a-z0-9_\.-]+) followed by and @ sign ([\da-z\.-]+) followed by a period ([a-z\.]{2,6})`

Each group has it's own set of parameters.

### Greedy and Lazy Match

A greedy match is a quantifier that will match the longest possible string while lazy will match the shortest possible string.
Our expression only has greedy matches + and {}. If our quantifiers were lazy then they would look like +? and {}?.

A greedy match will match as large of a group as possible in your expression. A lazy match will match as small of a group as possible in your expression string. 
Our expression only contains greedy quantifiers (+ and {}). 
Lazy quatifiers are +? or {}?

## Author

This Regex tutorial was created by Jacqueline Cashman [My Github](https://github.com/jacquelinehockin). 
Thank you for tuning in! Hope this helps.