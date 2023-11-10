# RegexMastery_HexadecimalValueMatching

## . Summary

Regular expressions (regex) are a sequence of characters that define a search pattern. They can be used to search, edit, or manipulate text. Regex is a powerful tool that can be used in a variety of programming languages and text editors.

## . Table of Contents

- [Introduction](#Introduction)
- [Regex Pattern](#RegexPattern)
- [Regex Components](#RegexComponents)
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Special Characters](#specialCharacters)

## Introduction

Hexadecimal (hex) values are frequently used in web development to represent colors and other data. This tutorial will guide you through the process of using regular expressions to match hex values in text, ensuring precise matches with boundary markers.

## . Regex Pattern

The regex pattern for matching hexadecimal values with boundary markers is as follows:

\b#?([0-9A-Fa-f]{3}|[0-9A-Fa-f]{6})\b

### . Anchors

Anchors are regex components that match the beginning or end of a string. The most common anchors are:

- ^: Matches the beginning of a string.
- $: Matches the end of a string.
- \b: Matches the beginning or end of a word.

### . Quantifiers

Quantifiers are regex components that specify how many times a pattern can match. The most common quantifiers are:

- +: Matches one or more times.
- ?: Matches zero or one times.
- \*: Matches zero or more times.
- {n}: Matches exactly n times.
- {n,m}: Matches at least n times and at most m times.

We can also use quantifiers to match specific hexadecimal values. For example, the following regex pattern matches the hexadecimal value 0xFFFFFFFF:

const hexFRegex = /^0xFFFFFFFF$/;

The ^ and $ anchors ensure that the pattern matches the entire string.

Here is an example of how to use the hexFRegex pattern to match the hexadecimal value 0xFFFFFFFF:

### . OR Operator

The OR Operator is a regex component that matches either the pattern before or after it. The OR Operator is represented by the pipe character (|).
[a-f0-9]{6}|[a-f0-9]{3} the | in the middle is representing that it will either be 6 characters or 3

### . Character Classes

Character classes in regular expressions allow you to define a set of characters from which the regex engine will match a single character. For example, the character class [aeiou] matches any vowel.

Example:

Regex Pattern: ^[aeiou]$

This pattern will match a string that contains only a single vowel, such as "e" or "o".

^ matches the beginning of the string.
[aeiou] matches any vowel.
(dollar$) matches the end of the string.

### . Flags

gi
Flags are regex components that modify the behavior of a regex.

g is the Global flag and tells Regex not to return anything after the first match.

i is the Ignore Case flag, allowing for upper- or lower-case results.

m is for Multiline Search, which treats a mulitline input string as one line.

### . Grouping and Capturing

Parentheses () are used to group multiple characters into a single data point. The output of a regex search is an array, and the data between the parentheses is available at each index in the array.

Regex pattern is:

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/
The part of the pattern that is enclosed in parentheses (...) is called a capturing group. A capturing group captures the matched characters and makes them available in the output array.

In this case, the capturing group matches either a hexadecimal value that is six characters long ([a-f0-9]{6}) or a hexadecimal value that is three characters long ([a-f0-9]{3}).

For example, if we search for the above regex pattern in the string #abcdef, the output array will be:

["abcdef"]
The first element in the array is the matched hexadecimal value, abcdef.

If we search for the above regex pattern in the string #fff, the output array will be:

["fff"]
The first element in the array is the matched hexadecimal value, fff.

### . Bracket Expressions

Bracket expressions are regex components that match a single character from a set of characters. For example, the bracket expression [0-9a-fA-F] matches any hexadecimal digit.

## . Special Characters

\n Newline

\r Carriage return

\t Tab

\0 Null character

\YYY Octal character YYY

\xYY Hexadecimal character YY

\uYYYY Hexadecimal character YYYY

\cY Control character Y

### . Boundaries

\b
The \b markers are word boundary anchors that ensure the matched hex value is not part of a larger word or surrounded by alphanumeric characters.

### . Back-references

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_expressions

## . Author

Nina Mahdawe, I am an aspiring FullStackDeveloper. I have always had the passion for software development and computer science. I enjoy programming and learning new skills.
Thanks for reading my regex tutorial! Learning regex can be a bit daunting, but it's worth it for the power and flexibility it gives you as a coder. Just keep practicing, and you'll be a regex master in no time.
