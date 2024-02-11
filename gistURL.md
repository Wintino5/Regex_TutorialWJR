# A Regex matching a URL

A regular expression, or regex is a series of special characters that define a search pattern. In this gist, we will be diving into a regex that matches a URL.

## Summary
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

The regex example used in this tutorial is one that is used to match a URL. The regex includes anchors, a quantifier, grouping constructs, bracket expressions, character escapes and character classes. All of these terms will be explained in this .md file.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

The anchors in regular expressions are used to specify the position in the string where a match should occur. There's `^` and `$`. When a `^` is used at the beginning it means that the characters that follow have to appear at the start of the string. When a `$` appears at the end of a string the preceding characters must appear at the end.

Here is an example in the URL regex: `^(https?:\/\/)` and `([\/\w \.-]*)*\/?$`

### Quantifiers

Qualifiers set the limits of the string that the regex matches. They include the minimum and maximum number of the the regex is looking for.

- `*` matches the pattern zero or more times
- `?` matches the pattern zero or one time
- `{ n, x }` matches the pattern from a minimum of `n` number of times to a maximum of `x` number of times

Examples: `{2,6}` , `*\/?`

### Grouping Constructs

Grouping Constructs are used to break sections up to ensure that each section fulfills different requirements. The primary way to group a section is by using parentheses `()`. This is known as a subexpression.

Examples: `(https?:\/\/)` , `([\da-z\.-]+)` , `([a-z\.]{2,6})` , `([\/\w \.-]*)`

### Bracket Expressions

Bracket Expressions which are also known as a positive character group use brackets `[]` to represent a range of characters that we want to match. They outline the characters that are to be included in the regex.

- `[a-z]` the string can contain any lowercase letter between a-z
- `[0-9]` the string can contain any number between 0-9
- `[_-]` the string can contain an underscore or hypen

Examples: `[\da-z\.-]` , `[a-z\.]` , `[\/\w \.-]`

### Character Classes

Character classes define a set of characters that can occur in an input string to fulfill a match.

- `.` matches any character except the newline character `\n`
- `\w` matches any alphanumeric character from the basic Latin alphabet, including the underscore `_`

Examples: `\.` , `\w`

### Character Escapes

Character Escapes are used to represent characters with special meaning or to match characters that might otherwise be interpreted as part of the syntax. The backslash `\` characterizes escapes.

Examples: `\/\/` , `\da-z\.-` , `\.([a-z\.` , `\/\w \.-` , `\/`

## Author

My name is Winston James Jr, and I am a Rutgers New Brunswick Web Development/Coding Bootcamp student. My GitHub is [Wintino5](https://github.com/wintino5)
