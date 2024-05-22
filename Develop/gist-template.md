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

- '[a-zA-Z0-9._%+-]+' : Matches the criteria for username

- '@' : Indicates @ symbol

- '[a-zA-Z0-9.-]+' : Matches criteria for domain

- '\.' : Matching the dot before the TLD

- '[a-zA-Z]{2,}' : Matches criteria for TLD

- '$' : Indicates end of string  

This regular expression would match standard email addresses such as "erika@email.com"


# Table of Contents
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)


# Anchors

Anchors are special characters that define a position of a patten within a string. Anchors do not match any characters, but they do indicate where a match should begin and end. Anchors ensure that the string matches the pattern for an email address and that there are no extra characters before or after the email address. 

There are two types of anchors:

The first is he Beginning of Line Anchor (^) and it indicates that the pattern should occur at the beginning of a line. This anchor assures that the pattern must occur at the start of a string or immediately after a line break. 

The second is the End of Line Anchor ($) and it indicates that the said anchor should occur at the end of a line. This anchor assures that the pattern must occur at the end of a string or immediately after a line break.  



# Quantifiers

Quantifiers specify how many times characters or groups of characters appear in various parts of the email address. 

- '+' Quantifier ensures that at least one occurence of elements (lowercase letters, digits, underscores, dots or hyphens) has occured.

- '+' Quantifier after the sequence, '[a-zA-Z0-9._%+-]' signifies that at least one character has been used in the username.

- '+' Quantifier after the sequence, '+ after [a-zA-Z0-9.-]' signifies that at least one character has been in the domain. 

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

- '([A-Za-z0-9._%+-]+)' : Captures the first group known as the username part of the email address.

- '@' matches the '@' : symbol.

- '([A-Za-z0-9.-]+)' : Captures the second group known as the domain part of the email address.

- '\.' matches the dot '.' : Separating the domain and the top-level domain.

- '([A-Za-z]{2,})' : Captures the third group known as the top-level domain.


# Bracket Expressions

Bracket expressions are also known as character classes that are often used to match specific sets of characters in regular expressions. Bracket expressions are used to define characters in various parts of the email address, such as the username, domain, and top-level domain.

- Username: '[A-Za-z0-9._%+-]+'

One or more characters are matched from the set defined within the square brackets [...].
Bracket expressions allows alphanumeric characters (uppercase and lowercase), dots, and hyphens in the username.

- '@' Symbol: @

This matches the '@' symbol in the email address.

- Domain: '[A-Za-z0-9.-]+'

One or more characters are matched for the domain.
It allows alphanumeric characters (uppercase and lowercase), dots, and hyphens in the domain.

- Dot '.' :

The bracket expression matches the dot '.' that separates the domain and the top-level domain.

- Top-Level Domain (TLD): '[A-Za-z]{2,}'

Two or more alphabetic characters are matched for the top-level domain.
It allows alphabetic characters (uppercase and lowercase) like 'com', 'org', 'net', etc.


# Greedy and Lazy Match

Greedy and lazy match affect how the pattern behaves when there are multiple occurences of characters in the email address. Greedy quatifiers consume as much text as possible while lazy quantifiers consume as little as possible while still allowing matching to occur.

^ and $ represent the start and end of the string, respectively, ensuring that the entire string matches the pattern.

'([A-Za-z0-9._%+-]+)' Username
- Greedy matching quantifiers such as '+' will match one or more characters in the username and domain while still allowing the pattern to match.
Example: if the email address is: "example.erika+test" the greedy quantifier will match that as the username. 

'@' Matches the '@' symbol.

'([A-Za-z0-9.-]+)' domain 
- To make a lazy quantifier you will add '?' to the end of the sequence ([A-Za-z0-9.-]+?) this will force the quantifier to match few characters while allowing the pattern to match. Ultimately, causing the username and domain to match separately without consuming the email address.
Example: "example.erika+test@email.com"

'\.' Matches the dot '.' that separates the domain and the top-level domain.

'([A-Za-z]{2,})' Top-level domain



# Author
Questions or concerns can be addressed to [erikaylopez Github](https://github.com/erikaylopez)


# Gist GitHub
[Gist GitHub](https://gist.github.com/erikaylopez/418e0c11c1acb63525611a6ac38f724a)