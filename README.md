# Regular Expressions: Matching a URL (/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/)

Regular expressions, or Regex, is a string of literal and meta characters that is used to search for a specific pattern in text. These expressions are particularly useful when the developer wants a field in a form, such as a password, to meet a criteria.  

## Summary

The expression I chose to decipher is this: "/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/", a pattern is used to match a URL. Each character in this expression specifies a specific pattern that is used to verify if the URL a user inputs is a valid one.

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
Anchors are characters that are not used to match characters, rather, they are used to specify a position before, after, or inbetween characters. Anchor characters include: ^, $. In our regex example, we want the inputted string to begin with 'http'.

### Quantifiers
Quantifiers include '{}' (matches a specific number/range of times), '*' (0 <= occurances of pattern matching), '+' (1 <= occurances of pattern matching), '?' (1 >= occurances of matching). 

In our example '{3,6}', indicates that the top level domain must be 3 to 6 characters long. the '?' indicates that 'https://' portion of the URL and  the 's' in 'http' is optional. This is so when a user types in a URL, they can still navigate to the website by only using the second and the top level domain. The '+' part allows the user to input a subdomain as well as a second level domain. 

### Grouping Constructs
Grouping contructs include '()'. Because each part of a URL has differing requirements, parentheses are used to group sections together. The contents within the '()' are called subexpressions. ':' are used to separate grouped sections that are next to each other. 

In our example, '(https?:\/\/)', '([\da-z\.-]+)', '([a-z\.]{2,6})', and '([\/\w \.-]*)' are grouped sections. The first group matches the scheme of a URL. The second searches for a domain. The third matches a top level domain, like '.com'. The last group matches an endpoint after the '.com/', and is optional.

### Bracket Expressions
Bracket expressions are characters that specifies a set of characters that is included in the pattern. Bracket expression characters include'[]'. You could put a range of characters, such as '[a-z]', or specific characters like '[dog]' which will search for a string that has the characters 'd', 'o', or 'g' regardless of length and if the string only has one repeating specified character. It is also case-sensitive.

In our example above, '[\da-z.-]' is a pattern a domain name. The expression translates to a range of characters that can be any digit, characters from lowercase a to z, dots and hypens. 

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
