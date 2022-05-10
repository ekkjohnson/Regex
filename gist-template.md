# Email Match - Regex Tutorial

This gist document will be a written tutorial to explain the use of regex to match emails using the regex expression, /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/. Regex can be useful to validate emails, especially when using applications like Node or MongoDB. 

## Summary

A regex, or regular expression, is a sequence of characters used to define a search pattern in text. Usual used by string-search algorithms and are used to find or find and replace strings or for input validation. This specific tutorial walks through the components of regex and how it can be used to match an email. 

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

Achors are regex tokens that say something about the string or matching process. They aren't used to match characters, instead they are used to tell us the eginine's current position in the string matches a determined location. The anchors used in this regex expression for matching an email are ^ , which indicates the beginning of the string and $to indicate the ending of the string. (m), or multiline is not enabled in our example, so the regex will end at $.

### Quantifiers

Quantifiers specify how many instances of a character, character class, or group must be present for the match to be found. Quantifiers in this regex includes the + operator, which will connect the users email name + email service + .com. Another quantifier in our example includes {2,6}, which will allow a match range of 2-6 characters for the character set of [a-z\.].

### Grouping Constructs

Grouping constructs delineate the subexpressions of a regex and capture the substrings of an input string. You could use grouping constructs to match a subexpression that is repeated in the input string. In our example, capturing group #1 in this expression is ([a-z0-9_\.-]+) that matches the user email name. The second capturing group is ([\da-z\.-]+) which will match the email service. Then lastly, capture group #3 is ([a-z\.]{2,6}) to capture the .com.

### Bracket Expressions

Bracket expressions are either matching list or non-matching list expressions. Brackets indicate a set of characters to match. In our example, bracked expressions for email validation include the character sets of [a-z0-9_\.-], which is matching any letter a-z and is case senstive. It also matches a character 0-9 and matches the characters "_" , "-" , and "."; [\da-z\.-], which is matching a single digit from 0-9, any character a-z (case senstive), and the characters "." and "-".; [a-z\.] matches any character a-z(case senstive) and the character ".".

### Character Classes

Character classes tell the regex engine to match one of several specific characters. These can include digits, words, or whitespace. 

A list of character classes:
"." which represents any character except characters on a new line
"\w" repesents words
"\W" represents not words
"\d" represents digits
"\D" represents not digits
"\s" represents whitespace
"\S" represents not whitespace
"[abc]" represents a,b, or c
"[^abc]" represents not a,b, or c
"[a-z]" represents character between a and z In the expression /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ character classes a-z and "\d" are used. This means that a letter a to z and a digit from 0 to 9 can be in the string.

### The OR Operator

The "OR" operator "|" allows there to be a choice in matching where the expression matches before or after is acceptable. In this example for matching an email, there is no "OR" operator.

### Flags

Flags "/" are optional parameters that we can add to a plain expression to make it search in a different way. Each flag is denoted by a single alphabetic character, and serves different purposes in modifying the expression's searching behavior.

"i" says to ingore capital casing so that "A" and "a" are considered the same when searching.
"g" looks for all matches when there is a search.
"m" affects "^" and "$" behavior across multiple lines when searching.
"s" enables "dotall" to match newline character. Flags were not used in this email regex.


### Character Escapes

Character Escape "\" is known as the escape code and restores the original literal meaning of the following character. 


## Author

Hi, I'm Elizabeth Kissner Johnson and I am a fullstack webdeveloper. 
You can check out my other projects at https://github.com/ekkjohnson. Or contact me at ekkjohnson@gmail.com.
