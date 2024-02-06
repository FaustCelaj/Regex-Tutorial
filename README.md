## Regex Tutorial: Matching an email

Regular expressions (Regex) serve as templates to identify specific sequences of characters within text. This guide dissects the components of an email regex to detail how it validates email addresses.

## Summary
Here's an expression we use to make sure the email address someone gives us is valid:
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/i
```

## Table of Contents

1. [Anchors](#anchors)
2. [Quantifiers](#quantifiers)
3. [OR Operator](#or-operator)
4. [Character Classes](#character-classes)
5. [Flags](#flags)
6. [Grouping and Capturing](#grouping-and-capturing)
7. [Bracket Expressions](#bracket-expressions)
8. [Greedy and Lazy Match](#greedy-and-lazy-match)
9. [Boundaries](#boundaries)
10. [Back-references](#back-references)
11. [Look-ahead and Look-behind](#look-ahead-and-look-behind)


### Anchors
Anchors ensure a regex match is fixed at a specific point within the text. The `^` symbol matches the position right before the string's first character, while `$` aligns with the position immediately after the string's last character.

### Quantifiers
Quantifiers set the scope of characters or expressions to be matched. The `{2,6}` notation specifies a range, indicating the email domain ending should have between 2 to 6 letters.

### OR Operator
The OR Operator `|` represents a logical "or" within the pattern matching. It is crucial for constructing expressions that match one of the multiple possible conditions.

### Character Classes
Character classes differentiate types of characters. The dot `.` typically requires a preceding `\` to denote an actual period; otherwise, it acts as a wildcard. `\d` serves as a concise representation for any digit from 0 through 9.

### Flags
Flags modify the search behavior of a regex. The `i` flag, for instance, renders the search case insensitive.

### Grouping and Capturing
Parentheses `()` are used to define groups within a regex, capturing domains of specified lengths with the `[a-z\.]{2,6}` pattern.

### Bracket Expressions
Bracket expressions `[]` match any of the contained characters, common elements in email addresses include lowercase letters, digits, and certain symbols.

### Greedy and Lazy Match
Quantifiers like `*`, `+`, and `{}` are greedy by default. The addition of `?` makes them lazy, minimizing their reach to the nearest possible match.

### Boundaries
The boundary marker `\b` highlights positions where a word character is adjacent to a non-word character, facilitating searches that focus on complete words only.

### Back-references
Back-references, such as `\1`, point back to previously matched segments within the regex, allowing for repeated pattern matching based on earlier captures.

### Look-ahead and Look-behind
For conditional pattern matches, look-ahead and look-behind assertions are used to find patterns that are either followed by or preceded by another specified pattern.

Gists Link: https://gist.github.com/FaustCelaj/a4e5c819fec1b80a41efeee8a27f4638
