# Regex Tutorial: Email Validation

## Your Task

As web development students, you will often find yourself both writing code and writing about code. Understanding regular expressions (regex) is crucial for efficient pattern matching and string manipulation in any development task. This tutorial aims to demystify how a specific regex works, focusing on one commonly used for validating email addresses.

## User Story

**AS A** web development student  
**I WANT** a tutorial explaining a specific regex  
**SO THAT** I can understand the search pattern the regex defines

## Acceptance Criteria

**GIVEN** a regex tutorial  
**WHEN** I open the tutorial  
**THEN** I see a descriptive title and introductory paragraph explaining the purpose of the tutorial, a summary describing the regex featured in the tutorial, a table of contents linking to different sections that break down each component of the regex and explain what it does, and a section about the author with a link to the author’s GitHub profile.

## What Is a Regex?

A **regex**, short for **regular expression**, is a sequence of characters that forms a search pattern. When used in code or search algorithms, regex can be applied to find or replace patterns of characters within strings. They are frequently utilized to validate inputs like email addresses, URLs, and phone numbers.

## Summary

This tutorial will break down the regular expression used for email validation: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. This regex ensures a user enters a valid email format by checking for a sequence of characters followed by an "@" symbol, a domain name, and a domain suffix.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors (`^` and `$`)

`^` asserts the start of a line, and `$` asserts the end, ensuring the string conforms entirely to the regex pattern, preventing matches within longer strings.

### Quantifiers (`+`, `{2,6}`)

`+` allows one or more of the preceding element, crucial for validating parts like the username in an email. `{2,6}` specifically restricts the length of the top-level domain, applying only to the `[a-z.]` character class, which ensures the domain suffix is between 2 and 6 characters long.

### Grouping Constructs (`()`)

Grouping constructs are used to apply different rules to different parts of the regex. In this email regex, the parentheses create three groups: the local part before the `@`, the domain, and the top-level domain.

### Bracket Expressions (`[ ]`)

Bracket expressions specify a set of characters that are allowed in a segment of the email. For example, `[a-z0-9_\.-]` matches lowercase letters, digits, underscores, periods, and hyphens in the local part of the email.

### Character Classes (`\d`)

`\d` is a shorthand character class that matches any digit, equivalent to `[0-9]`. This is used in our regex to allow digits in the domain part of the email.

### Flags

This particular regex does not use flags, but common flags include `i` for case-insensitivity, allowing the regex to match letters regardless of their case, and `g` for global matching, which finds all matches within the given string.

### Character Escapes (`\`)

The backslash `\` is used to escape special characters within the regex, ensuring they are treated as literal characters. For example, `\.` is used to escape the dot in the domain, ensuring it matches a literal period rather than any character.

## Author

This tutorial was crafted by [Fred Motta](https://github.com/fredm2357). Visit my GitHub profile for more tutorials and insights into coding and software development.