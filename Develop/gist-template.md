# Regex for matching a URL

This is a tutorial to explain how a specific regular expression works and matches what it is searching for. A regex is a series of characters that defines a search pattern. By using regular expressions, we can validate user input much more dynamically and account for multiple possible outcomes without having to account for a ton of edge cases.

## Summary

The regex that I will be discussing in this tutorial is one that will help you match a URL.

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

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

Since all regex are considered literals, they need to be wrapped in slash characters (`/`).

### Anchors

This regex has anchors at the beginning and at the end. The purpose of anchors in a regex isn't to match any character, but to designate the position before or after a set of characters. The caret (`^`) anchor sets the beginning of the text that is being matched, and the dollar (`$`) anchor sets the end.

### Quantifiers

There are a few different quantifiers in this regex. One of those is the question mark (`?`) quantifier. This quantifier will match the character that precedes it 0 or 1 time. That means that what ever comes before the `?` is optional.

So if we look at the part of the regex that reads `(https?:\/\/)?`, this means that when searching for a url, everything that is in the parenthesis is optional. It also means that the `https` is optional. The parentheses here acts as a grouping construct, which will be discussed further in the tutorial.

The star (`*`) quantifier is similar to the `?` quantifier in that anything that precedes it is optional. However, unlike the `?` quantifier, it does not only match it up to 1 time. The `*` quantifier will match whatever precedes it as many times as it appears in the string.

If we look at the part of the regex that reads `([\/\w \.-]*)*`, we can see that this searches for any amount of forward slashes, letters either upper or lower case, periods, or hyphen. These are optional however. They do not have to be included in the search.

The plus (`+`) quantifier will match anything that precedes it at least 1 time. This means that whatever precedes it is mandatory in the search. It also does not only match it up to 1 time. It will match whatever precedes it as many times as it appears in the string.

If we look at the part of the regex that reads `([\da-z\.-]+)`, this means that it will look for any amount of digits, lowercase letters from a-z, and periods.

Another type of quantifier that is present in this regex are the curly brackets (`{}`). The numbers inside these curly brackets set the minimum and maximum amount of characters that will be searched for.

If we look at the part of the regex that reads `([a-z\.]{2,6})`, this means that it will match anything with this search pattern at least 2 times and at most 6 times.

### Character Classes

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

```

```
