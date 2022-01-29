# URL Regex X

Regular expressions or regex are used in every day tasks such as find and replace tools in text editors. They can be as simple as find plain text using literal characters or can be more complex and search for patterns in plain text using a combination of literal and meta charcters.

## Summary

/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

I will be reviewing a regular expression used to find URLs. This regex uses literal and meta characters to create a meaningful search tool. Search through many lines of data to find all URLs in many different formats all at once with one regular expression. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Bracket Expressions](#bracket-expressions)
- [Escape Sequence](#escape-sequence)
- [Grouping and Capturing](#grouping-and-capturing)
- [Back References](#back-references)

## Regex Components

### Anchors
^ anchor used to mark the beginning of the search pattern  
$ anchor used to mark the end of the search pattern

### Quantifiers
? - quantifier used to note the preceding character or group of characters will match zero or one time  
Example: (https?:\/\/)?  
This is looking for character set matching http:// this can occur once or not at all in a matching URL.  

$+$ - quantifier used to note the preceding character or group of characters will match one or more times  
Example: [\da-z\.-]+  
This is looking for any digit and/or letter a thru z in any combination followed by a period and a dash. This group can repeated one or more times.  

{2,6} - quantifier used to note the preceding character or group of characters will match 2 to 6 times  
Example: [a-z\.]{2,6}  
This is looking for any letter a thru z in any combination followed by a period. This group can be repeated 2 to 6 times.  

$*$ - quantifier used to note the preceding character or group of characters will match zero or more times  
Example: [\/\w \.-]*  
This is looking for a forward slash followed by any word character alphanumeric including underscores, followed by a space followed by a period followed by a slash. This group can not exist or be repeated multiple times.  

### Character Classes
\d - used to match a digit character 0-9  
\w - used to match a word character, any word alphanumeric including underscores  

### Bracket Expressions
[a-z] - used to match any character in the set - a to z - case sensitive  

### Escape Sequence
\ - to match a character having special meaning in regex use an escape sequence prefix with a backslash  
Example: \\/
This is looking for a forward slash.  

### Grouping and Capturing
() - captured groups of characters

### Back References
() - captured groups of characters can be used as a back-reference

## Author
Kimberly Amaya

I am a student at UC Davis Coding boot camp for web development. I am super motivated to do great things. I've seriously never used a regex to search through text but I will now. Hope you find this useful as well. [Link to my github](https://github.com/kimberlyamaya)