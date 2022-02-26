# Intro to Regex

## Summary

Regular expressions are a search pattern used to identify characters from a group of characters, also referred to as regex. Originated in the 1950s by mathematician Stephen Cole Kleene, token it as a regular language using his notion of regular events. It incorporates literal and metacharacters to identify a specific string or number in documents or databases. In this tutorial I will be breaking down the different components of matching an email regex, for reference here is an example `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/\g`.

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

The components of regex are called atoms which include: characters, bracket expressions, escape character sets, anchors, special characters. With any combination of these atoms you can search for a specific word, number, or phrase.

### Anchors

Anchors can be placed at the beginning or end of a string, or in between. In the example from our summary we have `^` at the beginning notioning to look at the beginning of a string that starts with these specifications. We also have a `$` at the end stating this expression is finished once the matched item is found.

### Quantifiers

Quantifiers are used to create limitless matching options and stipulations for characters. It lets you specify how many of a specific character type or a range of characters. They are identified using curly braces and follow a character class or expression. In the example I gave in the summary the quantifier would be `{2,6}` stating that the minimum is 2 and the maximum is 6.

The most common options for quantifiers are greedy or lazy. A greedy quantifier finds matches for each position in a string, if there is no match it will go to the next position. An example of a greedy quantifier would be `/.+/`, this will continue to look for potential matches until the number of possible matches have been exhausted. On the other hand lazy quantifiers repeat as little as possible. For example `?` locates zero or one occurrence at a given position.

### Character Classes

Character classes are used to distinguish groups of character. For example `/d` class would be able to locate any digit number, while `/w` is used to identify any alphanumeric character. On the other hand if you use capital letters it turns it negative, meaning `/D` locates anything not a digit and `/W` locates anything not an alphanumeric character.

### Flags

Flags are an advanced searching option that allows for global searching without case sensitivity, they can be used separately or together as part of a regular expression. The different types of flags are `d,g,i,m,s,u,y`, each serving a separate purpose.
i allows you to make your search case sensitive, g makes it a global search, and m is a multiple line search.

Example:

From the example in the summary the flag would be `\g` for a global search.

### Grouping and Capturing

Grouping is the principle of categorizing the returned search patterns and giving it a position to identify in a later reference. You're able to capture subgroups of a returned group using parenthesis, the first subgroup would be referred to as group[1], while the original group would be group[0].

Example:

Group[0]:`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` -This group will look for any email.
Group[1]: `([a-z0-9_\.-]+)` - This subgroup will look for any character with lower case letters and number with hyphens and periods
Gorup[2]: `([\da-z\.-]+)` - This subgroup matches any numeric value and lower case character, and any hyphens or periods.
Group[3]: `([a-z\.]{2,6})` - This subgroup will match any 2 to 6 value character with any lower case letters and a period.

### Bracket Expressions

Brackets are used to indicate specific character matches, you can use any character or range of characters by using hyphens. They are used for grouping together multiple single expressions to help locate larger phrases or complex sequences of data.

Example:

`[a-z0-9_\.-]` this bracket expression is looking for a match with any combination of lower case letters and numbers that may have a hyphen or period.

### Look-ahead and Look-behind

In conclusion all the components of the regex are crucial to its functionality. It plays an important role in completing successful matches. Without the individual parts you wouldn't be able to make exact search criterias.

## Author

Thank you for reading my tutorial, I hope you gained as much knowledge as I did creating it for you. I am currently enrolled in a full stack web development bootcamp at OSU. I am 2/3 of the way through and have gained a tremendous amount of knowledge from it.

Github Profile: https://github.com/HGuleed
