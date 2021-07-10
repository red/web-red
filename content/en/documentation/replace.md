### replace
```red
USAGE:
     REPLACE series pattern value

DESCRIPTION: 
     Replaces values in a series, in place. 
     REPLACE is a function! value.

ARGUMENTS:
     series       [any-block! any-string! binary! vector!] "The series to be modified."
     pattern       "Specific value or parse rule pattern to match."
     value         "New value, replaces pattern in the series."

REFINEMENTS:
     /all         => Replace all occurrences, not just the first.
     /deep        => Replace pattern in all sub-lists as well.
     /case        => Case-sensitive replacement.

```