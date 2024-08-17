# Rejex Tutorial 
Hello, this is a tutorial about what a Rerjex is and its different components. Thank you for reading! 

## Summary

A regular expression, or regex for short, is a sequence of characters that defines a search pattern. Regexes are used to search for and match specific patterns in strings of text, and they are often used in programming and text processing. Here is an example of a regex code:

Example regex: \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b

This regex can be used to match email addresses in a string of text. The regex looks for patterns that match the structure of an email address: it starts with one or more characters (letters, numbers, or certain symbols) followed by an @ symbol, followed by one or more characters (letters, numbers, or certain symbols) followed by a period, followed by two or more letters. The \b characters at the beginning and end of the regex indicate word boundaries, which helps to ensure that the regex only matches complete email addresses and not parts of other words.

Regexes can be used in various programming languages and tools to search for and manipulate text. For example, a programmer might use a regex to extract email addresses from a list of names and addresses, or to validate that a user's input in a form field is a properly formatted email address.

## Table of Contents 

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)
- [About the Author](#author)
- [References used](#references)

## Regex Components 

### Anchors

An anchor is a special character that specifies the position of a pattern within a string of text. In this regex, the \b characters at the beginning and end of the pattern are word boundary anchors.

Word boundary anchors are used to match the position of a word in a string of text. The \b anchor matches the position between a word character (such as a letter or number) and a non-word character (such as a space or punctuation mark), or vice versa. This helps to ensure that the regex only matches complete words and not parts of other words.

In the case of this regex, the word boundary anchors are used to ensure that the regex only matches complete email addresses and not parts of other words. For example, the regex would match example@gmail.com, but it would not match example@gm ail.com, because there is a space between gm and ail.

### Quantifiers

A quantifier is a special character that specifies how many times a pattern should be repeated in a string of text. In this regex, the + symbol is a quantifier.

The + quantifier specifies that the pattern preceding it should be repeated one or more times. In this case, the pattern [A-Z0-9._%+-] specifies a character class that includes uppercase letters, numbers, and certain symbols. The + quantifier specifies that this character class should be repeated one or more times, which means that the regex will match one or more uppercase letters, numbers, or symbols.

There is also a quantifier in the regex in the form of the {2,} symbol. This quantifier specifies that the pattern preceding it should be repeated at least two times. In this case, the pattern [A-Z] specifies a character class that includes uppercase letters. The {2,} quantifier specifies that this character class should be repeated at least two times, which means that the regex will match at least two uppercase letters.

### OR Operator

There is no "or" operator in the regex expression \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b.

The "or" operator in regex is typically represented by the | symbol. This operator allows you to specify multiple alternative patterns, and the regex will match any of the specified patterns. For example, the regex cat|dog will match either the word "cat" or the word "dog".

In this regex expression, the | operator is not used. Instead, the different patterns are specified using character classes, character sets, and quantifiers.

### Character Classes

A character class is a set of characters that are enclosed in square brackets, and it matches any single character that is a member of the class. For example, the character class [A-Z] matches any uppercase letter.

A character set is a set of characters that are enclosed in square brackets and separated by a hyphen, and it matches any single character that falls within the range specified by the set. For example, the character set [0-9] matches any digit.

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)