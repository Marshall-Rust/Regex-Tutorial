# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

HTML Tag: `/^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/`

This tutorial will show you how to analyze and break down an HTML tag

## Table of Contents

- [Anchors](#anchors)
  Anchors
  The $ (dollar symbol) anchor matches the pattern at the end of the string.
  The ^ (carat) anchor matches the pattern at the begining of the string. It also tells the regex what character the pattern should start with. Since it is HTML it will be (<>).

- [Quantifiers](#quantifiers)
  Quantifiers determine how many times the regex matches the set of characters for which it is looking.
  The + (plus sign) tells the regex to match 1 or more of the preceding token.
  The ? (question mark) tells the regex to match 0 or 1 of the preceding token, effectively making it optional.
  The \* (asterisk) tells the regex to match 0 or more of the preceding token.
  Show below is portion of the regex that is using quantifiers.

([^<]+)\*

- [Grouping Constructs](#grouping-constructs)
  In the example regex the portions shown below are all subexpressions.
  [a-z]+
  [^<]+
  ?:>(.\*)<\/\1>|\s+\/>

The () (parenthesis) groups multiple tokens together and creates a capture group for extracting a substring or using a backreference. The text inside the () are considered subexpressions.

- [Bracket Expressions](#bracket-expressions)
  In the example below the bracket expression will match a character having a character code between the two specified characters inclusive.
  [a-z]
  The [] (bracket) matches any character in the set.

- [Character Classes](#character-classes)
  The \s matches any whitespace character (spaces, tabs, line breaks).
  The . (period) matches any character except linebreaks.
  The \w Matches any word character (alphanumeric & underscore). Only matches low-ascii characters (no accented or non-roman characters). Equivalent to [A-Za-z0-9_]
- [The OR Operator](#the-or-operator)
  The | (vertical line) acts like a boolean OR. Matches the expression before or after the |. It can operate within a group, or on a whole expression. The patterns will be tested in order.

- [Flags](#flags)
  There are no flags present in the example HTML but below are the types of flags you might see in other regex.
  The (m) matches each the beginning and end of every new line
  The (u) allows matching outside the UTF-16 character set
  The (y) allows matching from a different starting position
  The (s) allows matching of everything including new lines
  The (i) ignores case sensitivity
  The (g) matches for all occurences

- [Character Escapes](#character-escapes)
  The \ (backslash) is used to indicate whether a character should be literally interpreted.
  Shown below is an example of character escapes from the HTML regex
  \1 - searches for matches of the first grouping construct

## Author

Howdy, my names Marshall! Github Marshall-Rust
