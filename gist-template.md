# Validating Phone Number Inputs with Regex Expressions in Survey123

When creating survey forms, it is often good practice to apply validation rules to ensure the input matches the format required for the final report output. By enforcing formatting rules right at the input stage, you can streamline the QAQC process and reduce user input errors that can cause headaches down the road. The following gist describes how a regex expression can be formatted and then applied to a Survey123 form in Survey123 Connect.

## Summary

Many surveys include a question asking the user to input a phone number. In this example, we are working with an inspection form that requires the user to collect phone numbers (using United States phone number conventions) for the Facility Owner, Operator, Qualifed Person(s), and Environmental Individual(s). Given how many phone number questions there are in the survey, we want to make sure that each one is entered in the same format so that there is consistency in each facility report.

For our report, we want the phone numbers to be in a ten digit format, separated by hyphens (i.e. 555-555-5555). The following regex expression will accomplish this:

`^[2-9]\d{2}-\d{3}-\d{4}$`

## Table of Contents

- [Anchors](#anchors)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Quantifiers](#quantifiers)
- [Literal Characters](#literal-characters)

## Regex Components

### Anchors

The characters `^` and `$` serve as anchors for our regex expression, and indicate how the string should start and end. In our example, we follow the first anchor `^` by a bracket expression that accepts a range of valid digits for the first character of the input string. The closing anchor `$` is preceeded with a series of "character class/quantifier" combinations that indicate the requirements for consecutive digits in the input string.

### Bracket Expressions

As mentioned above, the regex expressions starts with a **bracket expression** `[2-9]` that looks for the string to start with a numeric digit of a value of `2` through `9`. We omit `0` and `1` as a valid first character because in the United States, area codes cannot start with 0 or 1.

and cannot end with 11 (as in 911 or 411 – as these are reserved for special uses).

as is a 9 as the middle digit of an area code


### Character Classes

A **character class** defines a set of characters that can be used in an input string to fulfill a match. In our expression, we use `/d` to match any Arabic numeral digit. Note that this class is equivalent to the bracket expression `[0-9]`.


### Quantifiers

The parts of the expression that are enclosed in curly brackets `{ }` are **quantifiers**. which set the limits of the string that the regex matches. For example, in our expression we use {4} as a quantifier to specify that the preceding \d should be matched exactly four times, meaning it will match four consecutive digits.

### Literal Characters

In regular expressions, when you use a character outside of square brackets [], it is treated as a literal character and matches itself. In our expresses, we include a dash `-` to require that the 3-digit area code, 3-digit exchange code, and 4-digit subscriber number of the phone number are separated by a dash.

## Author

Katherine Clark is a GIS Analyst and aspiring Geospatial Developer with more than five years industry experience. You can read more about her on her profile[https://kclarkdev.github.io/kc-project-portfolio/].
