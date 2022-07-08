# Regex Challenge -- OSU Bootcamp Challenge 17
    Developed by Megan Beekman (2022)

## Table of Contents

- [Regex Tutorial for Email Addresses](#regex-tutorial-for-email-addresses)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
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
  - [Author](#author)


# What is RegEx?:
    -- "Regular Expression" (known as RegEx) is a pattern of characters used to validate character combinations being read inside of different coding languages. This tutorial shows a breakdown of a RegEx for an email address...

## Summary
A RegEx for emails uses specific characters to encode the input address. Below is our example: <br/>
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`


### Anchors
    The begining of the string is identified by the caret ```^``` and the end of the string is identified by the dollar sign ```$```
### Quantifiers
    ```+``` is used to communicate there is another sequence to be matched as a greedy quantifier. ```{2,6}``` is another greedy quantifer used to specify the input that there should be a minimum of 2 characrtors to a maximum of 6 characters.

### OR Operator
    The begining of the string is identified by the caret ```^``` and the end of the string is identified by the dollar sign ```$```
### Character Classes
    The period symbol ```.``` will match any character except line breaks. in our example the ```.``` actually refers to the periods in the email and are not a character class.

### Flags
    Flags are optional and change the behavior of searching; flags are denoted using ONE single lowercase alphabetic character. To give multiple flags to a Regex, we write them one after another (without any spaces or other delimiters). 
    
    In Regex for JavaScript, there's a total of SIX(6) flags, each one having a different purpose.

### Grouping and Capturing
    There are three groups that are being captured in this example. The first group is the username of the e-mail account ```[a-z0-9_\.-]```. The second group captures the domain name being used ```[\da-z\.-]```. The third group captures the domain extention, ".com" ```[a-z\.]{2,6}```.

### Bracket Expressions
    >> There are 3 bracket expressions within the example listed above. The information in the bracket expressions is opened and closed between brackets ```[]```. This indentifies which information is allowed to be matched.
        - 1st Expression:* ```[a-z0-9_\.-]``` - includes case sensitive characters from a-z and also numbers from 0-9 an underscore along with periods and hyphens.
        - 2nd Expression:* ```[\da-z\.-]``` - includes all digits, case sensitive characters from a-z, periods, and hyphens
        - 3rd Expression:* ```[a-z\.]``` - includes case sensitive characters from a-z and periods.


### Greedy and Lazy Match

    Lazy quantifiers marked. So far in this example, we have only used greedy quantifiers ```+``` and ```{}```. If these quantifiers were lazy quantifiers, they would appear as ```+?``` or ```{}?``` meaning it will direct the system to make the shortest match possible.

### Boundaries
    Boundaries ```\b``` make assertions about what can be matched to the left and right of the current position. In non-Unicode mode, it matches a position where only one side is an ASCII letter, digit or underscore. In Unicode mode, it matches a position where only one side is a Unicode letter, digit or underscore. ```\B```
        - Replace both ```^``` and ```$``` with ```\b```. 

### Back-references
    Back-references are regex commands which refer to a previous part of the matched regular expression. Back-references are specified with backslash and a single digit: ```\1```. 
### Look-ahead and Look-behind
    Lookahead and lookbehind, also known as lookaround, are zero-length assertions just like the start and end of line, and start and end with word anchors explained earlier in this tutorial. These return only the result 'match' or 'no match'. That is why they are called “assertions”, don't consume characters in the string.
## Author
    Hello. My name is Megan. I am a student in OSU coding bootcamp (2022)
### [View My GitHub Profile HERE!](https://github.com/meganbeek98)
