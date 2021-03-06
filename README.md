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

- Capturing groups create a sub-expression by placing an expression inside matching open and close parentheses. Quantifiers and optionality can be applied to sub-expressions. Each set of parentheses creates a capture number that is used to identify capturing groups, ranging from 1 to 9 (\1 to \9). Capturing groups can be referenced later by their capture number in the regular expression or the replacement string in REGEXP_REPLACE.
Note: While only 9 can be referenced, Yellowbrick supports patterns that contain up to 16 capturing groups. Using more than 16 capturing groups will result in an error.
Non-capturing groups create a sub-expression without creating a capturing group. Non-capturing groups are indicated by including the question mark ( ? ) and colon ( : ) after the opening parenthesis.

EXAMPLE:

- (\w+)     Sub-expression and noted as a capturing group.
- (?:\w+)   Sub-expression in the non-capturing group.

### Bracket Expressions

- Brackets indicate a set of characters to match. Any individual   character between the brackets will match, and you can also use a hyphen to define a set.

EXAMPLE:

- 'elephant'.match(/[abcd]/) // -> matches 'a'


### Character Classes

- Character classes distinguish kinds of characters such as, for      example, distinguishing between letters and digits.

EXAMPLE:
- let text = "Give 100%!"; 
let pattern = /\d/g;
let result = text.match(pattern); // --> 1,0,0

- let text = "Give 100%!"; 
let pattern = /\D/g;
let result = text.match(pattern); // --> G,i,v,e, ,%,!  NO digits!

- const chessStory = 'He played the King in a8 and she moved her Queen in c2.';
const regexpCoordinates = /\w\d/g;
console.log(chessStory.match(regexpCoordinates));
// expected output: Array [ 'a8', 'c2']

### The OR Operator

- The OR operator allows you to add same logic inside the bracket expression to the outside. Works best with grouping construct or between two different grouping constructs.


### Flags

- Flags are placed at the end of a regex, after the second slash, and they define additional functionality or limits for regex. There are 6 operational flags but the most commonly used ones are as follows:

### Character Escapes

- The backslash in a regular expression precedes a literal character. You also escape certain letters that represent common character classes, such as \w for a word character or \s for a space.

## Author

- I'm a student at UCI bootcamp [full stack web development]

[MY GIT HUB REPO](https://github.com/scorpion77777)
