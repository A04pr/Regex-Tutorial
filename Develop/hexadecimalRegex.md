# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

The regex I will be describing matches 3 or 6 digit hexadecimal values (with or without the '#' preceeding the value) to a color.

Regex: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

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

    In this regex there are two anchors, the carat '^' and the dollar sign '$'. They match the beginning and end of the string.

    The carat '^' specifies the beginning of the string.

    The dollar sign '$' specifies the end point of the string. 

### Quantifiers

    There are three instances of quantifiers in the regex. 

        The question mark '?' asks if there is either one or zero of the preceeding character. In this case the pound(hashtag) symbol '#', this allows the user to input a hexadecimal value with or without the '#' at the beginning and get the same match.

        The numerical quantifiers '{6}' and '{3}' specify the allowed amount of characters preceeding each. In this example, there can only be an exact amount of three or six characters within the range of the character class [a-f0-9]. Allowing the user to input both three digit and six digit hexadecimal codes.

        These quantifiers combined allow the user to input either a three or six digit hexadecimal code with or without the '#' and match it to a color, given the user's characters are within the allowed range of letters and numbers.

### Grouping Constructs

    The '()' in '([a-f0-9]{6}|[a-f0-9]{3})' is the only instance of a grouping construct in this regex. The grouping constuct '()' defines '[a-f0-9]{6}|[a-f0-9]{3}' as a group, allowing the '|', which is an OR operator, to correctly seperate the two alternatives. 

### Bracket Expressions

    There are two instances of the same bracket expression.

    The functionality of the bracket expression '[a-f0-9]' will be explained in the character classes section. 

### Character Classes

    The bracket expression '[a-f0-9]' is a character class specifying the allowed range of characters. In this example, it will allow any letter within the range of a-f and any number within the range of 0-9, this is because these are this is the range of characters that are used to describe colors using hexadecimal code. 

### The OR Operator

    There is one OR operator.  

    The OR operator '|' allows either of the alternatives in '([a-f0-9]{6}|[a-f0-9]{3})', so '[a-f0-9]{6}' or '[a-f0-9]{3}' to match. The alternatives, specify the allowed types of characters and number of characters. In this example the user can input either a six digit code with '[a-f0-9]' as characters OR a three digit code with the same characters, either way it will match. 

### Flags

    There are no flags in this regex.

### Character Escapes

    There are no character escapes in this regex.

## Author

Author: Aidan Reed
Github: https://github.com/A04pr
