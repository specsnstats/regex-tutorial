# Regex Tutorial

## Summary

Here, I will be breaking down the components of the following Regex:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` which serves the purpose of matching to an Email. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)

## Regex Components

### Anchors

The anchor `^` is meant to indicate that the results of the Regex can include any results that meet the range of possible matches that come after it, indicated in the `()` grouping construct. essentially, everything contained inside the `[]` brackets will be accepted by the regex, with one additional rule, the quantifier `+`. 

### Quantifiers

The quantifier in this example `+` indicates that the email can contain the specified characters or matches given inside the `[]` one or more times. Meaning, if that portion of the email contains 0 characters, it will not be a match for the search. 

Another quantifier used in this is the `{2,6}` quantifier which in this case indicates that the number of characters allowed in this section cannot exceed 6 or be less than 2. Single letters or strings that exceed 6 characters will not return in this regex

### Grouping Constructs

The grouping construct used here `()` is simply to wrap the items that apply to the anchor, while giving them the extra quantifier. Everything outside this grouping construct (like the `@` sign and everything that comes after) will follow a different set of rules, unless of course the anchor is repeated, which in this case it is not. 

### Bracket Expressions

The bracket expression is used to indicate what specific characters (or range of characters) will pass in the search. In this example, the first set of brackets encountered are `[a-z0-9_\.-]`, indicating that the characters that will pass are letters a-z (not including capital letters), numbers 0-9, and the special characters _ / . - 

### Character Classes

Character classes are also used in this regex, as indicated by the `\d`, which means that there can be a match of any Arabic numeral digit. Simply put, it is a shorthand for `[0-9]`.

## Author

Jonathan Newman with the help of my Teacher and TA's at University of Washington
