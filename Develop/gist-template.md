# Regular expression Tutorial
For this homework assignment I will be explaining how the regex theory works. I will also explain in detail what the regular expression is. 

## Summary

A regular expression (shortened as regex sometimes referred to as rational expression) is a sequence of characters that specifies a search pattern in text. Usually such patterns are used by string algorithms for "find" or "find and replace" operations on strings, or for input validation. Regular expression techniques are developed in theoretical computer science and formal language theory.


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

Single characters. A single character with no special significance represents that character in the target string. The characters with special significance (i.e. operator characters) are these:
^ . [ $ ( ) | * + ? { \
A non-alphanumeric character acts as the literal character (whether special or not) by escaping it, namely, adding \ in front of it.
Wild card. The . (period) special character matches any single character except \n (newline).
Bracket Expressions. A bracket expression represents a character set via a list of characters enclosed by the square brackets: '[' and ']'. It normally matches the target string with any single character from the list.
If the character list begins with '^', it matches any single character not from the rest of the list.

If two characters in the list are separated by '–', this is shorthand for the (inclusive) range of characters between those two. It is illegal for two ranges to share an endpoint, e.g. a-c-e. Ranges are collating-sequence dependent and should be avoided for portability.
Most special characters lose their special status and become literals within brackets. Additionally,
– is literal at the end or beginning of a bracket expression
^ is literal if not at the beginning of a bracket expression
The backslash character, \, retains its meaning in bracket expressions, permitting the usage of the special escape sequences: such as \n, \t, \w, \d, etc.
Control characters. A backslash, \, followed by one of the characters a, b, f, n, r, t, v represents the ANSI-C interpretation of the control character
Escape character sets. These are special sequences representing commonly used character sets:
\w is word (program identifier) character: [A-Za-z0-9_]
\W is non-word character: [^A-Za-z0-9_]
\s is a whitespace character: [ \f\n\r\t]
\S is a non-whitespace character: [^ \f\n\r\t]
\d is a digit character: [0-9]
\D is a non-digit character: [^0-9]


## Anchors

Anchors. These are special sequences which match an empty substring:
^ matches at the beginning of the target string
$ matches at the end of the target string
\b matches on a word boundary, i.e., the previous or subsequent character is not a word character
Recursive expansion. Any regular expression surrounded by parentheses is an atom:
( regular_expression )


### Quantifiers

Regular expressions use quantifiers to generate unbounded matching possibilities and other matching amount specifications. An atom can optionally be followed by one of these quantifiers:
 *   representing 0 or more occurrences of the atom,
 +   representing 1 or more occurrence of the atom,
 ?   representing 0 or 1 occurrences of the atom,
the bound {n}   representing exactly n occurrences of the atom,
the bound {m,n}   representing between m and n occurrences of the atom.
The quantifier can optionally be followed by "?" indicating that the match be minimal (non-greedy, reluctant) as opposed to the default maximal (greedy) match.


### Grouping Constructs

Grouping constructs delineate the subexpressions of a regular expression and capture the substrings of an input string. You can use grouping constructs to do the following:

Match a subexpression that is repeated in the input string.

Apply a quantifier to a subexpression that has multiple regular expression language elements. For more information about quantifiers, see Quantifiers.

Include a subexpression in the string that is returned by the Regex.Replace and Match.Result methods.

Retrieve individual subexpressions from the Match.Groups property and process them separately from the matched text as a whole.

### Bracket Expressions

A bracket expression (an expression enclosed in square brackets, "[]" ) is an RE that shall match a specific set of single characters, and may match a specific set of multi-character collating elements, based on the non-empty set of list expressions contained in the bracket expression.


### Character Classes

a character class is a set of characters enclosed within square brackets. It specifies the characters that will successfully match a single character from a given input string.


### The OR Operator

Regex recognizes range expressions inside a list. They represent those characters that fall between two elements in the current collating sequence. You form a range expression by putting a range operator between two characters.


### Flags

A flag is an optional parameter to a regex that modifies its behavior of searching.
i	Ignore Casing	Makes the expression search case-insensitively.
g	Global	Makes the expression search for all occurrences.
s	Dot All	Makes the wild character . match newlines as well.
m	Multiline	Makes the boundary characters ^ and $ match the beginning and ending of every single line instead of the beginning and ending of the whole string.
y	Sticky	Makes the expression start its searching from the index indicated in its lastIndex property.
u	Unicode	Makes the expression assume individual characters as code points, not code units, and thus match 32-bit characters as well.


### Character Escapes

The \ is known as the escape code, which restore the original literal meaning of the following character. Similarly, * , + , ? (occurrence indicators), ^ , $ (position anchors) have special meaning in regex. You need to use an escape code to match with these characters.

## Author

Giulia Shelton 

Github- https://github.com/giulia037
