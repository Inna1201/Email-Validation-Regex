# Matching an Email Regex Tutorial

Regular expressions or Regex, are a set of characters which are used to create patterns that can be used to search, find, replace, or validate text. Regular expressions use both basic and special characters. Basic characters are standard letters, numbers, and general keyboard characters, while all other characters are considered special.


## Summary

Regular expressions provides the ability to validate the structure of an email address.
In this tutorial, we will take a look at how to validate an email address by using the below regex:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

Let's go through each character one by one to define what does it do.


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

Anchors are metacharacters that help us to declare the position.

The `^` and `$` meta-characters are anchors that used in above regular expression to indicate the beginning `(^)` and ending `($)` of the string.

### Quantifiers

Quantifiers are used to quantify how many times a part of your regular expression should be repeated.

 The `+` quantifier means "one or more", the same as `{1,}`.

 The `{n,m}` means that quantifier matches an element at least n times, but no more than m times.

 In the above regex the `+` quantifier used twice (`[a-z0-9_\.-]+` and `[\da-z\.-]+`) and means that any character that matches the conditions inside the brackets should present one or more times. 

 And `{2,6}` quantifier means that (`([a-z\.]{2,6})`) characters that matches the conditions inside the brackets should present at least 2 times, but no more than 6 times.

 

### Grouping Constructs

Grouping constructs captures everything enclosed within the parenthesis `()`. This allows to treat multiple characters as a single unit. They are useful for creating blocks of patterns to apply all kind modifiers (e.g quantifiers) to them as a whole.

Everything inside a pair of parentheses is taken as a single group(unit). In the above regex there are three groups `([a-z0-9_\.-]+)`, `([\da-z\.-]+)`, and `([a-z\.]{2,6})`.


### Bracket Expressions

The expression inside the square brackets `[]` indicates a set of characters that is used to match a single character. Brackets `[]` are used to create a matching list that will match on any one of the characters in the list. 

In the above regex there are three bracket expressions `[a-z0-9_\.-]`, `[\da-z\.-]`, and `[a-z\.]`.

As example, in `[a-z0-9_\.-]`, the character in the brackets can be any lowercase letter from a-z, or any number from 0-9, or it can be a underscore, or a single period, or a hyphen.


### Character Classes

A character class is a set of characters enclosed within square brackets, a special notation that matches any symbol from a certain set.

There are also several built-in character classes e.g.:
- "." matches any single character except a new line (\n)
- "\w" matches any alphanumeric character
- "\W" matches any character that is not a word character
- "\d" matches any decimal digit
- "\D" matches any character that is not a decimal digit

In the above regex we have a digit class `\d` and it corresponds to any single digit. The backslash is used to separate the digit class from a plain letter d. Also we have `[a-z]` character class that corresponds to any single letter from a to z, and `[0-9]` class that corresponds to the same as `\d`.


### Character Escapes

All characters in regex matches themselves except those having special meaning.
Special Regex Characters: ., +, *, ?, ^, $, (, ), [, ], {, }, \ and |.

In the above regex we are using grpouping oerators `()`, character class sets `[]`, quantifiers `+` and repetition modifiers `{}`.

Also we are using the escape character `\` , a backslash before character negates any specialized function it might serve. As example in our regex   because of the backslash `\.` represents literally a period!

## Author

My name is Inna and I am on the way to becoming a Full-Stack Junior Wed developer.
GitHub: https://github.com/Inna1201.
