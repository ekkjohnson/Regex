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

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

You can check out my other projects at https://github.com/ekkjohnson. Or contact me at ekkjohnson@gmail.com.
