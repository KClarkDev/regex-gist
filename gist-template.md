# Validating phone number inputs with Regex Expressions in Survey123

When creating survey forms, it is often good practice to apply validation rules to ensure the input matches the format required for the final report output. By enforcing formatting rules right at the input stage, you can streamline the QAQC process and reduce user input errors that can cause headaches down the road. The following gist describes how a regex expression can be formatted and then applied to a Survey123 form in Survey123 Connect.

## Summary

Many surveys include a question asking the user to input a phone number. In this example, we are working with an inspection form that requires the user to collect phone numbers for the Facility Owner, Operator, Qualifed Person(s), and Environmental Individual(s). Given how many phone number questions there are in the survey, we want to make sure that each one is entered in the same format so that there is consistency in each facility report.

For our report, we want the phone numbers to be in a ten digit format, separated by hyphens (i.e. 555-555-5555). The following regex expression will accomplish this:

`^[2-9]\d{2}-\d{3}-\d{4}$`

## Table of Contents

- [Anchors](#anchors)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Quantifiers](#quantifiers)

## Regex Components

### Anchors

The characters `^` and `$` serve as anchors for our regex expression, and indicate how the string should start and end. In our example, we follow the first anchor by a bracket expression that accepts a range of valid digits. The closing anchor is preceeded with a quantifier that indicates the requirement for four consecutive digits in the input string.

### Bracket Expressions

As mentioned above, the regex expressions starts with a **bracket expression** `[2-9]` that looks for the string to start with a numeric digit of a value of `2` through `9`. We omit `0` and `1` as a valid first character because in the United States, area codes cannot start with 0 or 1.

### Character Classes

### Quantifiers

The rest of the expression includes **quantifiers**, which set the limits of the string that the regex matches. 

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
