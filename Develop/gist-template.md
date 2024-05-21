# RegEx Tutorial in Matching an Email

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

- '^' : Indicates the start of the string.

- '[a-zA-Z0-9._%+-]+' : matches the criteria for username

- '@' : indicates @ symbol

- '[a-zA-Z0-9.-]+' : matches criteria for domain

- '\.' : matching the dot before the TLD

- '[a-zA-Z]{2,}' : matches criteria for TLD

- '$' : indicates end of string  

This regular expression would match standard email addresses such as "erika@email.com"


# Table of Contents
- Anchors
- Quantifiers
- Character Classes
- Grouping and Capturing
- Bracket Expressions
- Greedy and Lazy Match


# Anchors

Anchors are special characters that define a position of a patten within a string. Anchors do not match any characters, but they do indicate where a match should begin and end. Anchors ensure that the string matches the pattern for an email address and that there are no extra characters before or after the email address. 

There are two types of anchors:

The first is he Beginning of Line Anchor (^) and it indicates that the pattern should occur at the beginning of a line. This anchor assures that the pattern must occur at the start of a string or immediately after a line break. 

The second is the End of Line Anchor ($) and it indicates that the said anchor should occur at the end of a line. This anchor assures that the pattern must occur at the end of a string or immediately after a line break.  



# Quantifiers

Quantifiers specify how many times characters or groups of characters appear in various parts of the email address. 

- '+' quantifier ensures that at least one occurence of elements (lowercase letters, digits, underscores, dots or hyphens) has occured.

- '+' quantifier after the sequence, '[a-zA-Z0-9._%+-]' signifies that at least one character has been used in the username.

- '+' quantifier after the sequence, '+ after [a-zA-Z0-9.-]' signifies that at least one character has been in the domain. 

- {2,4} is another quantifier in matching an email address and signifies that the top-level domain (TLD) should contain between 2 to 4 alphabetical characters. This quantifier can be found after the sequence, '[a-zA-Z]'. 


# Character Classes

Character classes are used to match specific patterns found in email addresses.

- '[A-Za-z0-9._%+-]+' : This character class matches one or more alphanumeric characters, dots, underscores, percentage signs, plus signs, or hyphens in the username.

- '@' : Matches the '@' symbol.

- '[A-Za-z0-9.-]+' : Matches one or more alphanumeric characters, dots, or hyphens in the domain.

- '\.' : Matches a dot '.'

- '[A-Za-z]{2,}' : Matches two or more alphabetic characters for the top-level domain.


# Grouping and Capturing

Grouping and capturing allows the isolation and extraction of specific parts of an email address such as username, domain, and top-level domain. 
Parentheses in regular expressions allows you to create groups- where anything inside the parentheses captures a group. 

- '([A-Za-z0-9._%+-]+)' : captures the first group known as the username part of the email address.

- '@' matches the '@' : symbol.

- '([A-Za-z0-9.-]+)' : captures the second group known as the domain part of the email address.

- '\.' matches the dot '.' : separating the domain and the top-level domain.

- '([A-Za-z]{2,})' : captures the third group known as the top-level domain.


# Bracket Expressions



# Greedy and Lazy Match



# Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)