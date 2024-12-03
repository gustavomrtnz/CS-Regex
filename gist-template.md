# Regex Email Validation

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
Email regex components are as follows: `/^([a-zA-Z0-9_.-]+)@([\da-zA-Z.-]+).([a-zA-Z.]{2,})$/.`
1. [`a-zA-Z0-9._%-]+ - Matches one or more of the following characters: letters (both uppercase and lowercase), numbers, periods, underscores, percent signs, and hyphens.
2. [a-zA-Z0-9.-]+ - Matches one or more of the following characters: letters (both uppercase and lowercase), numbers, periods, and hyphens.
3. [a-zA-Z]{2,} - Matches two or more letters (both uppercase and lowercase).





### Anchors
The Anchos `^` signifiex the beginning of the string, `$` which matches the end of the string, or the end of a line if the multiline flag (m) is enabled. This matches a position, not a character.

### Quantifiers
Quntifiers included in this regex are `+` which matches 1 or more of the preceding token, `*` which matches 0 or more of the preceding token, `{2 ,4}` which matches allows a match range of 2-6 characters for the chracters set of `[a-z\.]`

### Grouping Constructs
Grouping constructs are written using parentheses (). In the first grouping construct ([a-z0-9_\.-]+) means that the email address must start with a letter, number, underscore, or period, in other words, the email address must start with a valid username. In the second grouping construct ([\da-z\.-]+) means that the email address must contain a domain name eg. gmail, yahoo, etc. In the third grouping construct ([a-z\.]{2,6}) means that the domain name must end with a period followed by between 2-6 letters for example .com, .net, .org, etc. Grouping constructs are used to make sure that the email address contains the correct structure.


### Character Classes
Bracked expressios for email validation includes the character sets of `[a-z0-9_\.-]`, which is matching any letter a-z and is case senstive. It also matches a character 0-9 and matches the characters "_" , "-" , and "."; `[\da-z\.-]`, which is matching a single digit from 0-9, any character a-z (case senstive), and the characters "." and "-".; `[a-z\.]` matches any character a-z(case senstive) and the character ".". 

### The OR Operator
From my understanding `[|]` is the alternative operator

### Flags
Regular expressions have six optional flags that allow for functionality like global and case insensitive searching. These flags can be used separately or together in any order, and are included as part of the regular expression.
-Ignore Case: Makes the whole expression case-insensitive. For example, /aBc/i would match AbC.

-Global Search: Retain the index of the last match, allowing subsequent searches to start from the end of the previous match.
Without the global flag, subsequent searches will return the same match. RegExr only searches for a single match when the global flag is disabled to avoid infinite match errors.

-Multiline: When the multiline flag is enabled, beginning and end anchors (^ and $) will match the start and end of a line, instead of the start and end of the whole string.P atterns such as `/^[\s\S]+$/m` may return matches that span multiple lines because the anchors will match the start/end of any line.

-Unicode: When the unicode flag is enabled, you can use extended unicode escapes in the form `[\x{FFFFF}.]`
It also makes other escapes stricter, causing unrecognized escapes (ex. \j) to throw an error.

-Sticky: The expression will only match from its lastIndex position and ignores the global (g) flag if set. Because each search in RegExr is discrete, this flag has no further impact on the displayed results.

Dotasll: Dot (.) will match any character, including newline.


### Character Escapes
When validating an email address using a regular expression, you need to escape certain characters like periods (.), plus signs (+), and underscores (_) with a backslash (`\`) to ensure they are interpreted literally as part of the email address, not as special regex characters.

## Author
thank you for reading!
