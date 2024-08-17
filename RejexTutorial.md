# Rejex Tutorial 
Welcome to this tutorial focused on understanding what a Regex is and its various components.

## Summary
A regular expression, commonly referred to as regex, is a sequence of characters that establishes a search pattern. Regex is utilized to locate and match specific patterns within text strings, frequently appearing in programming and text manipulation tasks. An example of a regex code is:

Example regex: \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b

This particular regex is designed to identify email addresses within a text string. It looks for patterns that conform to the structure of an email address: beginning with one or more characters (letters, numbers, or certain symbols), followed by the @ symbol, then one or more characters (letters, numbers, or certain symbols), followed by a period, and concluding with at least two letters. The \b characters at both ends denote word boundaries, ensuring that the regex matches only complete email addresses rather than segments of larger words.

Regex can be employed across various programming languages and tools for text searching and manipulation. For instance, a developer might implement a regex to extract email addresses from a compilation of names and addresses, or to verify that a user’s input in a form field adheres to a valid email address format.

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
An anchor is a specific character that indicates the position of a pattern within a text string. In the given regex, the \b characters at the start and end function as word boundary anchors.

Word boundary anchors serve to identify the position of a word in a string. The \b anchor matches the location between a word character (like a letter or a number) and a non-word character (such as a space or punctuation), or vice versa. This ensures that the regex captures complete words rather than fragments.

In this instance, the word boundary anchors ensure that the regex matches entire email addresses exclusively. For example, it would successfully match example@gmail.com but would not match example@gm ail.com, as there is a space separating "gm" and "ail."

### Quantifiers
A quantifier specifies the number of times a pattern should appear in a text string. In this regex, the + symbol serves as a quantifier.

The + quantifier indicates that the preceding pattern must occur one or more times. Here, the pattern [A-Z0-9._%+-] defines a character class that includes uppercase letters, numbers, and certain symbols. Thus, the regex will match one or more uppercase letters, numbers, or symbols.

Additionally, the regex includes a quantifier represented by {2,}, which indicates that the preceding pattern must appear at least twice. In this case, the pattern [A-Z] defines a character class of uppercase letters. The {2,} quantifier ensures that this class appears a minimum of two times, meaning the regex will match at least two uppercase letters.

### OR Operator
The regex expression \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b does not incorporate an "or" operator.

Typically, the "or" operator in regex is denoted by the | symbol, allowing for multiple alternative patterns, with the regex matching any of the specified options. For example, the regex cat|dog will match either "cat" or "dog".

In this specific regex, no | operator is present; instead, various patterns are articulated through character classes, sets, and quantifiers.

### Character Classes
A character class is a collection of characters enclosed in square brackets, matching any single character that belongs to that class. For instance, the character class [A-Z] matches any uppercase letter.

A character set, meanwhile, is a range of characters specified within square brackets and separated by a hyphen, matching any single character within that range. For example, the character set [0-9] matches any digit.

### Flags
The regex expression \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b does not include any flags.

Flags are special characters added at the end of a regex expression that modify how the regex is interpreted. They can adjust the matching behavior, including whether the regex should be case-sensitive or capable of matching across multiple lines.

In this regex, the absence of flags means it will be interpreted according to the default behavior of the programming tool being utilized. For instance, in a language like Python, the default may be case-sensitive and not support multi-line matching.

To use flags in a regex, you can append them after the closing slash / of the expression. For example, using the i flag would make the regex case-insensitive: /\b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b/i.


### Grouping and Capturing
Grouping allows for the combination of multiple patterns, enabling the application of quantifiers or other functions to the entire group. Grouping is indicated using parentheses (( and )). For instance, the regex (cat|dog)+ will match one or more instances of either "cat" or "dog."

Capturing permits the extraction of matched text as a distinct string or variable, also using parentheses. For example, the regex (cat|dog) captures the matched text ("cat" or "dog") separately.

In the regex example \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b, the patterns [A-Z0-9._%+-]+ and [A-Z0-9.-]+ are grouped using parentheses, with the + quantifier applied to the entire group, allowing the regex to match one or more occurrences of the defined character classes (uppercase letters, numbers, and specific symbols).

This regex also incorporates capturing, as the full email address (including the local part, domain, and top-level domain) is enclosed in parentheses, enabling it to be captured as a separate string or variable.

### Bracket Expressions
Brackets in regex are utilized to denote a character class or set. A character class is a collection of characters in square brackets that matches any single character within that class. For example, the character class [A-Z] matches any uppercase letter.

A character set consists of characters enclosed in square brackets and separated by a hyphen, matching any single character in that range. For example, the character set [0-9] matches any digit.

In the regex expression \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b, two character classes are present: [A-Z0-9._%+-] and [A-Z]. The first class specifies uppercase letters, numbers, and certain symbols, while the second specifies only uppercase letters. These classes work alongside quantifiers (like + and {2,}) to define a pattern for matching email addresses in text.

### Greedy and Lazy Match
The regex expression \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b does not involve greedy or lazy matching.

Greedy matching refers to the tendency of most regex engines to match the longest possible string fitting the pattern. For instance, the regex .* applied to the string "abcdef" will match the entire string, as it is the longest match.

Conversely, lazy matching attempts to match the shortest possible string that fits the pattern. In the same example, using lazy matching with .* would match an empty string because it is the shortest match.

In the provided regex, there are no patterns utilizing the * or + quantifiers, which are typically associated with greedy and lazy matching behaviors.

### Boundaries
A boundary character indicates the position of a pattern within a text string, anchoring it to a specific location, such as the start or end of a word or line.

In the regex \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b, the \b characters at either end are word boundary indicators. These match positions between word characters (letters or numbers) and non-word characters (like spaces or punctuation).

This regex employs word boundary characters to ensure that it matches only complete email addresses rather than fragments. For example, it would match example@gmail.com but not example@gm ail.com due to the space between "gm" and "ail."

Overall, the regex \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b effectively combines character classes, sets, quantifiers, and boundaries to establish a pattern for identifying email addresses within text.

### Back-references
The regex expression \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b does not contain any back-references.

Back-references in regex allow for matching text that has previously been captured using parentheses. A back-reference is indicated by a backslash \ followed by a digit, which corresponds to a specific capturing group. For example, the regex (\w)\1 matches any character that is repeated in succession.

In the regex provided, there are no capturing groups or back-references present. Instead, it utilizes character classes, sets, and quantifiers to define a pattern for matching email addresses.

While back-references can be useful for identifying repeating patterns or confirming that a certain pattern appears multiple times, they are not necessary for matching email addresses, which typically do not exhibit repeating patterns.


### Look-ahead and Look-behind
The regex expression \b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b does not utilize look-ahead or look-behind constructs.

Look-ahead and look-behind are specialized constructs in regex that allow for matching a pattern based on the presence or absence of another pattern in the text. Look-ahead specifies a condition that must follow the current position, while look-behind specifies a condition that must precede it.

These constructs are beneficial for matching patterns that are not directly adjacent within the text. They are denoted using parentheses (( and )) along with the ?= or ?<= symbols.

For example, the regex (?<=abc)def will only match "def" if it is preceded by "abc". Conversely, (?=abc)def will match "def" only if it is followed by "abc".

In the provided regex, there are no look-ahead or look-behind constructs. It relies on character classes, sets, and quantifiers to define a structure for matching email addresses, which have a clear format that can be addressed using these elements.

While look-ahead and look-behind can be advantageous for matching more intricate patterns, they are not essential for matching email addresses due to their straightforward structure.


## Author
My name is Fabian Medina, and I am an aspiring web developer. You can find my recent projects on my GitHub: https://github.com/fabianmedina3012.

##References 
1. https://www.youtube.com/watch?v=7DG3kCDx53c
2. https://www.regular-expressions.info/possessive.html