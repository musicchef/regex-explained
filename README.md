# Regex for Matching URLs

Introductory paragraph (replace this with your text)

## Summary

In this document, we'll explore a regular expression (regex) designed to match URLs. The regex is /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/. We'll break down this regex into its individual components, explaining their roles and how they work together to validate and extract parts of a URL.

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

### Anchors
In the regex /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/, the ^ and $ are anchors.

^ asserts the start of the string, ensuring that the match begins at the beginning of the input.
$ asserts the end of the string, ensuring that the match extends to the end of the input.
These anchors collectively define the boundaries of the URL.
### Quantifiers
The quantifiers in this regex are ?, *, and {2,6.

? makes the preceding s? (https) group optional. This allows URLs to have either http:// or https://, or none at all.
* allows the preceding ([\/\w \.-]*)* to match zero or more characters within the path part of the URL.
{2,6} specifies the allowed length for the top-level domain (TLD) part of the URL. It matches domains with 2 to 6 characters (e.g., .com, .net, .info).
### Grouping Constructs
This regex uses several grouping constructs to capture different parts of the URL:

(https?:\/\/)? captures the optional protocol part (e.g., http:// or https://).
([\da-z\.-]+) captures the domain name, including letters, digits, periods, and hyphens.
([a-z\.]{2,6}) captures the TLD (e.g., .com, .net).
([\/\w \.-]*)* captures the optional path part of the URL.
### Bracket Expressions
The regex contains square brackets [...] within character classes:

[\da-z\.-] matches digits, lowercase letters, periods, and hyphens.
### Character Classes
Character classes like \d and \w are used to match specific character types:

\d matches digits (0-9).
\w matches word characters (letters, digits, and underscores).
### The OR Operator
The | symbol is used to denote an OR operation. For example, https? matches either "http" or "https."
### Flags
The regex doesn't use any flags like /g, /i, or /m.
### Character Escapes
The regex doesn't contain any character escapes.
## Author
Hamza Lhamous
