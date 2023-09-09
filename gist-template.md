# Validating phone number inputs with Regex Expressions in Survey123

When creating survey forms, it is often good practice to apply validation rules to ensure the input matches the format required for the final report output. By enforcing formatting rules right at the input stage, you can streamline the QAQC process and reduce user input errors that can cause headaches down the road. The following gist describes how a regex expression can be formatted and then applied to a Survey123 form in Survey123 Connect.

## Summary

Many surveys include a question asking the user to input a phone number. In this example, we are working with an inspection form that requires the user to collect phone numbers for the Facility Owner, Operator, Qualifed Person(s), and Environmental Individual(s). Given how many phone number questions there are in the survey, we want to make sure that each one is entered in the same format so that there is consistency in each facility report.

For our report, we want the phone numbers to be in a ten digit format, separated by hyphens (i.e. 555-555-5555). 

`^[2-9]\d{2}-\d{3}-\d{4}$`

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

The characters `^` and `$` serve as anchors for our regex expression, and indicate how the string should start and end. In our example, we follow the first anchor by a bracket expression. 

### Quantifiers

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
