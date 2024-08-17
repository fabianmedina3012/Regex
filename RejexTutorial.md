# Rejex Tutorial 
Hello, this is a tutorial about what a Rerjex is and its different components.

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

There are no flags in the regex expression \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b.

A flag is a special character that is added to the end of a regex expression and modifies the way the regex is interpreted. Flags are typically used to change the matching behavior of the regex, such as by specifying whether the regex should be case-sensitive or whether it should match across multiple lines.

In this regex expression, no flags are used. This means that the regex will be interpreted according to the default matching behavior of the tool or programming language being used. For example, if the regex is being used in a programming language like Python, the default matching behavior may be case-sensitive and may not match across multiple lines.

If you want to use flags in a regex expression, you can add them after the closing slash (/) at the end of the expression. For example, you could use the i flag to make the regex case-insensitive, like this: /\b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b/i.

### Grouping and Capturing

Grouping allows you to group multiple patterns together and apply quantifiers or other operations to the group as a whole. Grouping is achieved using parentheses (( and )). For example, the regex (cat|dog)+ will match one or more occurrences of the words "cat" or "dog".

Capturing allows you to extract the matched text as a separate string or variable. Capturing is achieved using parentheses (( and )). For example, the regex (cat|dog) will capture the matched text (either "cat" or "dog") as a separate string or variable.

In the regex expression \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b, the [A-Z0-9._%+-]+ and [A-Z0-9.-]+ patterns are grouped using parentheses. The + quantifier is applied to the group as a whole, which means that the regex will match one or more occurrences of the character class (uppercase letters, numbers, and certain symbols).

There is also capturing in the regex expression, as the entire email address (including the local part, domain part, and top-level domain) is enclosed in parentheses. This means that the matched email address will be captured as a separate string or variable.

### Bracket Expressions

Brackets are used in regex to specify a character class or a character set. A character class is a set of characters that are enclosed in square brackets, and it matches any single character that is a member of the class. For example, the character class [A-Z] matches any uppercase letter.

A character set is a set of characters that are enclosed in square brackets and separated by a hyphen, and it matches any single character that falls within the range specified by the set. For example, the character set [0-9] matches any digit.

In the regex expression \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b, there are two character classes: [A-Z0-9._%+-] and [A-Z]. The first character class specifies a set of uppercase letters, numbers, and certain symbols, and the second character class specifies a set of uppercase letters. These character classes are used in conjunction with quantifiers (the + and {2,} symbols) to specify a pattern for matching email addresses in a string of text. 

### Greedy and Lazy Match

There is no greedy or lazy match in the regex expression \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b.

Greedy and lazy matching refer to the way that a regex engine handles repeated patterns in a string of text. By default, most regex engines use greedy matching, which means that they will try to match the longest possible string that matches the pattern.

For example, consider the regex .* and the string "abcdef". The .* regex will match the entire string "abcdef", because it matches zero or more characters and the string "abcdef" is the longest possible string that matches the pattern. This is an example of greedy matching.

On the other hand, lazy matching means that the regex engine will try to match the shortest possible string that matches the pattern. For example, consider the same regex .* and the same string "abcdef". Using lazy matching, the .* regex will match the empty string "", because it is the shortest possible string that matches the pattern.

In the regex expression \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b, there are no patterns that use the * or + quantifiers, which are the most common quantifiers used in greedy and lazy matching.

### Boundaries
A boundary is a special character that specifies the position of a pattern within a string of text. Boundaries are used to anchor the pattern to a specific position within the string, such as the beginning or end of a word or the beginning or end of a line.

In the regex expression \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b, the \b characters at the beginning and end of the pattern are word boundary characters. Word boundary characters are used to match the position of a word in a string of text. The \b character matches the position between a word character (such as a letter or number) and a non-word character (such as a space or punctuation mark), or vice versa.

In this regex expression, the word boundary characters are used to ensure that the regex only matches complete email addresses and not parts of other words. For example, the regex would match example@gmail.com, but it would not match example@gm ail.com, because there is a space between gm and ail.

Overall, the regex expression \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b uses a combination of character classes, character sets, quantifiers, and boundaries to specify a pattern for matching email addresses in a string of text.


### Back-references

there are no back-references in the regex expression \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b.

Back-references are used in regex to match text that was previously captured using capturing parentheses. A back-reference is specified using a backslash (\) followed by a digit, which refers to a specific capturing group. For example, the regex (\w)\1 will match any character that is repeated twice in a row.

In the regex expression \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b, there are no capturing groups or back-references. This regex uses character classes, character sets, and quantifiers to specify a pattern for matching email addresses in a string of text.

Back-references are useful for matching repeating patterns or verifying that a specific pattern appears more than once in a string of text. However, they are not necessary for the task of matching email addresses, as email addresses do not generally contain repeating patterns.


### Look-ahead and Look-behind

There are no look ahead or look behind in the regex expression \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b.

Look ahead and look behind are special constructs in regex that allow you to match a pattern based on the presence or absence of another pattern in the string of text. Look ahead specifies a pattern that must be present after the current position, while look behind specifies a pattern that must be present before the current position.

Look ahead and look behind are useful for matching patterns that are not directly next to each other in the string of text. They are specified using parentheses (( and )) and the ?= or ?<= symbols.

For example, the regex (?<=abc)def will match the string "def" only if it is preceded by the string "abc". The regex (?=abc)def will match the string "def" only if it is followed by the string "abc".

In the regex expression \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b, there are no look ahead or look behind constructs. This regex uses character classes, character sets, and quantifiers to specify a pattern for matching email addresses in a string of text.

Look ahead and look behind can be useful for matching more complex patterns in a string of text, but they are not necessary for the task of matching email addresses, as email addresses have a well-defined structure that can be matched using character classes and quantifiers.


## Author

My name is Fabian Medina, and I am a beginner web developer, here is my github with my recent projects https://github.com/fabianmedina3012