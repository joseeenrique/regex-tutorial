# Regex 101

Regular expressions are patterns used to match character combinations in strings. In JavaScript, regular expressions are also objects. In this document we'll go over a specific type of regular expression used for email vailidation. 

## Summary

Email validation is very important to a page due to it's ability for data collection and adding features like email verification will reduce the amount of fraud the page will run into which leads to real customers.

regular expression email validation:
/^[a-zA-Z0-9.!#$%&'*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*$/.


Javascripts version for email validation:

function ValidateEmail(inputText)
{
var mailformat = /^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/;
if(inputText.value.match(mailformat))
{
alert("Valid email address!");
document.form1.text1.focus();
return true;
}
else
{
alert("You have entered an invalid email address!");
document.form1.text1.focus();
return false;
}
}


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

 A single character with no special significance represents that character in the target string.

### Anchors

- ^  Start of string, or start of line in multi-line pattern

- \A  Start of string

- $  End of string, or end of line in multi-line pattern

- \Z  End of string

- \b  Word boundary

- \B  Not word boundary

- \<  Start of word

- \>  End of word

### Quantifiers

- *  0 or more


- {3}  Exactly 3

- +  1 or more

- {3,}  3 or more

- ?  0 or 1

- {3,5}  3, 4 or 5

### Grouping Constructs

- (expr)	Captures the information that matches the expression in parentheses

- (?:expr) Groups the contained expressions together

- (?=expr)	Captures information that is followed by the expression if the expression is true

- (?<>)	Named capture group.*

- \k<>	Named back reference. *

### Bracket Expressions

- [abcd] Matches character in  square brackets.

- [a-d]  Matches character in  range separated by (-).

- [^abcd]  Matches character except the in the square brackets

- [^a-d]  Matches characters separated by (-).

### Character Classes

- \c   Control character

- \s   White space

- \S   Not white space

- \d   Digit

- \D   Not digit

- \w   Word

- \W   Not word

- \x   Hexade­cimal digit

- \O   Octal digit

### The OR Operator

You can compose regular expressions from operators.One type of operator is the OR operator or the alternation operator.In a regular expression it is denoted with a vertical line character ' | '.

### Flags

- i   search in case-insensitive.

- g  looks for all matches.

- m  Multiline mode.

- s  Enables “dotall” mode, that allows a dot . to match newline character.

- u  Enables full Unicode support.

- y  earching at the exact position in the text

### Character Escapes

- \\  single backslash

- \A  start of a string

- \b  word boundary. The zero-length string between \w and \W or \W and \w.

- \B  not at a word boundary

- \cX  ASCII control character

- \d  single digit [0-9]

- \D  single character that is NOT a digit [^0-9]

- \E  stop processing escaped characters

- \l  match a single lowercase letter [a-z]

- \L  single character that is not lowercase [^a-z]

- \Q  ignore escaped characters until \E is found

- \r  carriage return

- \s  single whitespace character

- \S  single character that is NOT white space

- \u  single uppercase character [A-Z]

- \U  single character that is not uppercase [^A-Z]

- \w  word character [a-zA-Z0-9_]

- \W  single character that is NOT a word character [^a-zA-Z0-9_]

- \x00-\xFF  hexadecimal character

- \x{0000}-\x{FFFF}  Unicode code point

- \Z  end of a string before the line break

## Author

Jose Martinez is 27 years old and is currently working in Human Resources in a Colorado based start up. He is originally from Puerto Rico and has been in the US for 6 years. He is a proud husband and catdad.

Github https://github.com/joseeenrique