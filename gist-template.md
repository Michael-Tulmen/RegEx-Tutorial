# RegEx Tutorial

Regular Expression (regex for short) is a character sequence that specifies search patterns in text normally employed in string-searching algorithms or in find/find-and-replace operations on strings or for input validation. Invented in the 1950's by Stephen Cole Kleene, nowadays regular expression is used in search engines, word processors,text-editors, and text processing in lexical analysis supported by most general-purpose programming languages.

## Summary

This tutorial will cover - Anchors - Quantifiers - Character Classes - Flags as listed in the below table of contents to give a holistic view of the uses and method surrounding understanding regular expression for use in general computer science.

## Table of Contents

- [RegEx Tutorial](#regex-tutorial)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [Character Classes](#character-classes)
    - [Flags](#flags)
  - [Author](#author)

## Regex Components

- Anchors
- Quantifiers
- Character Classes
- Flags

### Anchors

Anchors match the POSITION of characters in a string:
^ matches at the beginning of a string
$ matches at the end of a string
In application this is significant because it allows "anchoring" regex matches to a certain position.  
For example:
^a matches to abc whereas ^b does not, because the position of b is not right after the start of the string
Similarly c$ would match with abc whereas a$ would not due to a not being before the ending of the string.

### Quantifiers

Quantifiers define how many instances of a character must be present in the input for a match to occur.
There exists two subset of quantifiers in the form of Greedy quantifiers and Lazy Quantifiers
Whereas Greedy quantifiers and attempting to match as much of the string as possible, the ? quantifier type (lazy)
will make the quantifier stop as soon as it finds a match.

Reference Table:

| Quantifier       | Meaning                                                                                                        |
| ---------------- | -------------------------------------------------------------------------------------------------------------- |
| \*               | Matches the preceding item 0 or more times i.e. /bo\*/ = booooooo                                              |
| +                | Matches the preceding item 1 more more times i.e. /a+/ matches a and aaaaaaaa                                  |
| ?                | Matches the preceding item 0 or 1 times i.e /e?le?/ matches e in "angel" and le in "angle"                     |
| {n,}             | Where n is positive, matches n occurrences of the preceding item                                               |
| {n,m}            | Where n is 0 or positive and m is positive, matches at least n and at most m occurrences of the preceding item |
| \*?; +?; ??; etc | Will stop as soon as a match is found                                                                          |

### Character Classes

With character classes / character sets you can tell regex only to match one out of several characters by placing both characters
between square brackets:

For example:

Gr[ea]y would match both Grey and Gray.

This same logic can be applied to numbers where [0-9] would match any character ranging between 0 and 9 and similarly with hexadecimal notation [0-9a-fxA-FX]

### Flags

Regular expression can have flags that will affect searches:

| Flag | Meaning                                                                 |
| ---- | ----------------------------------------------------------------------- |
| i    | Case sensitive search                                                   |
| g    | Searches for all matches, without this only the first match is returned |
| m    | Multiline mode                                                          |
| s    | Dotall mode, allows a dot (.) to match a newline character              |
| u    | Enables full Unicode support                                            |
| y    | Sticky mode, searches an exact position in text                         |

## Author

My name is Michael Tulmen aspiring software developer, I hope this was beneficial to your overall understanding of regular expression.
To read more about me or see my coding history, feel free to browse my personal GitHub profile listed here: https://github.com/Michael-Tulmen
