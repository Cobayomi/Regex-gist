# Regex Tutorial

This Regex tutorial will illustrate and explain how regular expressions or reguex can be used to verify if a string contains a zipcode (postal code) or extract zip code from a string. 

## Summary

 I will describe the regular expression regex tag that would be used for a zipcode regex. My provided zipcode regex code snippet: ^[0-9]{5}(?:-[0-9]{4})?$ . Zipcode regex will read through strings of code to validate if there is zipcode within the string. These strings are also called patterns. A vaild US zipcode pattern allows both the five-digit and nine-digit (called ZIP + 4) formats.


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

## Regex Components
The valid Zipcode pattern should contain: You need to validate the ZIP codes (U.S. postal code) 
five-digit and nine-digit zipcodes (called ZIP+4) formats. The regex should match 12345 and 12345-6789, but not 1234, 123456, 123456789, or 1234-56789.


### Anchors
The valid zipcode will contain anchors starting off the pattern and ending it. The regex will match the start of this pattern and the end. If the anchor appears at the beginning of the string, with no characters before it and no characters after it.
Example from my snippet: ^ = Start of the string and the end $           # Assert position at the end of the string.
^[0-9]{5}(?:-[0-9]{4})?$

### Quantifiers
Quantifiers are the specific number of occurrence of a character to match against. This code matches the condition 1,2,3. This code shows [0-9]{5} and [0-9]{4} are matching and will capture. 

### Grouping and Capturing
Grouping in a regex defines groups of characters and captures them using the special parentheses ( and ) metacharacters. Any pattern using paratheses will be captured and matched. You may create a group by placing the regex pattern inside the set of parentheses. This code grouping shows (?:  and ) which will not capture.

### Bracket Expressions
Bracket expressions are a list of characters and/or character classes enclosed in brackets to match single characters or a range of characters in a list. This code brackets: [0-9]{5} and [0-9]{4}

### Boundaries
A zipcode Regex have several limitations.
It only works for US ZIP codes. If you need to support other countries, you might need to have a separate regular expression for each one of them and execute it based on the country provided.
It can not guarantee that ZIP code actually exists. For instance, 99999 is a correct format, but this ZIP code does not exist.
The extraction method can generate false-positive extraction if a string contains multiple numbers.

## Literal
This string has a literal matching. Any "string literal" is a sequence of characters from the source character set. The string can show for literal matching if it contain variables, literal values (text or numbers), and operators, which indicate how the other components in the expression are to be evaluated. This code shows:  -         #   Match a literal "-".

## Author
This gist was written by Capricia Obayomi, a full-stack bootcamp student.
Github: https://github.com/Cobayomi