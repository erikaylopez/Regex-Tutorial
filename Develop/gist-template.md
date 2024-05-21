# RegEx Tutorial i Matching an Email

RegEx, short for regular expressions, are a sequence of characters defining a pattern for matching within text. Typically utilized by string-searching algorithms for "find" or "find and replace" tasks on strings, or for input validation. These techniques for regular expressions are established in theoretical computer science and formal language theory.

This tutorial will specifically cover regex matching email addresses: 
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

# Summary 
Regular expressions for matching an email address follow a pattern that encompass various components of an email address, this includes:

- Username: this consists of alphanumeric characters, dots, hyphens and underscores. Typically, it cannot startr or end with a dot or have consecutive dots.
- Domain: this is known as the end of the email address, such as "gmail", "yahoo", ".com", or ".net"
- Top-Level Domain (TLD): any combination of letters- typically 2-6 characters long

When put together, a regular expression can look similar to this example:

^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$

The regular expression breakdown is as follows:

- ^: Indicates the start of the string.
- [a-zA-Z0-9._%+-]+: matches the criteria for username
- @ : indicates @ symbol
- [a-zA-Z0-9.-]+: matches criteria for domain
- \.: matching the dot before the TLD
- [a-zA-Z]{2,}: matches criteria for TLD
- $: indicates end of string  

This regular expression would match standard email addresses such as "erika@email.com"


# Table of Contents
- Anchors
- Quantifiers
- Character Classes
- Grouping and Capturing
- Bracket Expressions
- Greedy and Lazy Match


# Anchors

Anchors are special characters that define a position of a patten within a string. 

# Quantifiers
# Character Classes
# Grouping and Capturing
# Bracket Expressions
# Greedy and Lazy Match

# Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)