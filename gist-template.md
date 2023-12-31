# Regex Tutorial-Validating Emails

Regular Expressions (regex) are a specific sequence of characters, including letters, numbers and special characters, that can be included in search algorithm code to find or find and replace characters that are in a string or to validate input from users.  

## Summary

Regex can be used to search for text that is in a string but it can also verify whether or not a user has entered information correctly in a form.  In the case of verifying an email, regex can be made to be more specific by adding rules to the string search to ensure that the the structure of an email has been entered.  This can be done with only a few lines of code.  While this can be useful, it is important to understand that regex will not verify that an email is valid, but it will confirm if a user has entered characters into an email format.  This could add to the user experience by not accepting an email that does not meet criteria of a valid email address.  However, if not coded properly, it could invalidate or not accept international emails which could detract from the user experience.

In JavaScript the code could look like this:  

function ValidateEmail(inputText)
{
    var mailformat = /^[a-zA-Z0-9.!#$%&’*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*$/
    if(inputText.value.match(mailformat))
    {
        alert("Please enter a valid email address");
        return false;
        }
}

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

### Anchors

Search parameters are anchored by ^ or $ which tells the code to look for the characters after the ^ or before the $. 

### Quantifiers

A quantifier tells the code how many characters or symbols must be present to be a successful match.  For example, (+) means that the character matches at least once while (?) is expecting the character to match exactly zero times or one time.

### OR Operator

An OR operator tells the code that it can look for more than one condition.  This could be helpful when considering international email addresses (.com in the US OR .uk in UK)

### Character Classes

Character classes simplifies code by making a smaller range of characters represent a larger range.  For example instead of typing out [ abcdefghijklmnopqrstuvwxyz ] we can simply use [ a-z ].  It can also distinguish between types of characters like numbers and symbols. 

### Flags

Flags can be used in conjuction with other flags or independently.  They allow for additional functionality like searching globaly or case sensitive searches.

### Grouping and Capturing

Grouping allows a search for multiple patterns.  Grouping will use flags to capture the matched groups and then put them together in a different matched group.

### Bracket Expressions

Bracket expressions add additional simplification by telling the regex to look for the character classes that are in the brackets.

### Greedy and Lazy Match

A greedy match happens when a quantifier looks for the longest possible match or a match with as many successful matches as possible.  A lazy match is the exact opposite, finding the smallest amount of possible matches.

### Boundaries

Boundaries are parameters that are signaled by \b, \B, ^ or $.  It tells the regex to look for matches before or after or in between a match.  This can allow for partial or exact matches depending on how the assertion is written.   

### Back-references

Back-references refer to previously search for and/or found groups so that we do not have to keep searching for results that we already have when we are searching for multiple groups.

### Look-ahead and Look-behind

Look-ahead and look-behind are typically called "look-around".  These assertions do not look for matching characters, but simply look to see if the search is possible.  It does not return a string of searched characters but returns a "yes" or "no" response.  

## Author

Stephanie Jauch is a full stack developer with a passion for problem solving and making a difference. To learn more visit [GitHub](https://github.com/SKJauch)

