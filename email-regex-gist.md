# Regex Tutorial: Email Validation

## Introduction

In this tutorial, we will break down the components of a regular expression designed to validate email addresses. Regular expressions are powerful tools for pattern matching, and understanding how to build them can greatly enhance your coding projects.

## Summary

This tutorial explains the regex used for email validation: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. We will explore how each part of this expression works to ensure that a string matches a valid email format.

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

**`^` and `$`**
The caret `^` matches the start of a string, while the dollar sign `$` matches the end. This ensures that the regex does not allow characters outside the specific pattern of an email address.

### Quantifiers

**`+` and `{2,6}`**
The `+` quantifier matches one or more of the preceding element, making sure that each part of the email has at least one character. The `{2,6}` quantifier specifies that the top-level domain must be between 2 to 6 letters long.

### Grouping Constructs

**Parentheses `()`**
Grouping constructs break the regex into three main parts: the local-part, the domain, and the top-level domain, allowing us to apply different rules to different parts of the email address.

### Bracket Expressions

**`[a-z0-9_\.-]`**
This bracket expression allows any lowercase letter, number, underscore, period, or hyphen in the local-part of the email.

### Character Classes

**`\d`**
Represents any digit, equivalent to `[0-9]`. Used in the domain part of the regex to match numbers.

### The OR Operator

Not applicable in the basic email regex but can be discussed as an optional operator to match multiple patterns within a regex.

### Flags

Explain any flags used with the regex (e.g., `i` for case insensitivity, `g` for global search). Our basic email regex does not use flags, but they can be critical in other contexts.

### Character Escapes

**`\.`**
Escapes the dot character to treat it as a literal dot in the email addresses rather than a wildcard character.

## Author

This tutorial was written by [Fred Motta](https://github.com/fredm23579). Feel free to visit my GitHub profile for more tutorials and code snippets.
