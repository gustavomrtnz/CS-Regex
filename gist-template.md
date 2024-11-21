# Regex Email Validation

The tutorial is going to explaing the use of regex to validate an email using the expression `^[\w-\.]+@([\w-]+\.)+[\w-]{2,4}$`

## Summary

An email regex validartion can be broken down into three main parts
1. The Local Part -This part contains alphanumeric and specific special characters.
2. The Domain - The domain follows the '@' symbol and usually includes alphanumeric characters and possibly hyphens.
3. And The Top-Level Domain (TLD) - The TLD is typically two or more alphabetic characters.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
The Anchos `^` signifiex the beginning of the string, `$` which matches the end of the string, or the end of a line if the multiline flag (m) is enabled. This matches a position, not a character.

### Quantifiers
Quntifiers included in this regex are `+` which matches 1 or more of the preceding token, `*` which matches 0 or more of the preceding token, `{2 ,4}` which matches allows a match range of 2-6 characters for the chracters set of `[a-z\.]`

### Grouping Constructs


### Bracket Expressions

### Character Classes
Bracked expressios for email validation includes the character sets of `[a-z0-9_\.-]`, which is matching any letter a-z and is case senstive. It also matches a character 0-9 and matches the characters "_" , "-" , and "."; `[\da-z\.-]`, which is matching a single digit from 0-9, any character a-z (case senstive), and the characters "." and "-".; `[a-z\.]` matches any character a-z(case senstive) and the character ".". 

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
