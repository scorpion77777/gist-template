# Regular Expression

Regular expression is a pattern describing a certain amount of text. That makes them ideally suited for searching, text processing and data validation.

## Summary

- The above pattern matches Password123#, but does not match   Passsword123.

  <strong>^(?=.*?[A-Z])(?=(.*[a-z]){1,})(?=(.*[\d]){1,})(?=(.*[\W]){1,})(?!.*\s).{8,}$</strong>

- This regex will enforce these rules:
- At least one upper case English letter, (?=.*?[A-Z]).
- At least one lower case English letter, (?=.*?[a-z]).
- At least one digit, (?=.*?[0-9]).
- At least one special character, (?=.*?[#?!@$%^&*-])
- Minimum eight in length .{8,} (with the anchors).

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
- (^) Matches the beginning of the string, or the beginning of a line if the multiline flag (m) is enabled. This matches a position, not a character.

### Quantifiers
- Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found. 
- (?) Makes the preceding item optional. Greedy, so the optional item is included in the match if possible. (Example: abc? matches abc or ab)
- (*) Quantifier matches the preceding element zero or more times. It is equivalent to the {0,} quantifier. * is a greedy quantifier whose lazy equivalent is *?.

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes



## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
