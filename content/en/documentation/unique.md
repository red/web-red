### unique
```red
USAGE:
     UNIQUE set

DESCRIPTION: 
     Returns the data set with duplicates removed. 
     UNIQUE is a native! value.

ARGUMENTS:
     set          [block! hash! string!] 

REFINEMENTS:
     /case        => Use case-sensitive comparison.
     /skip        => Treat the series as fixed size records.
        size         [integer!] 

RETURNS:
     [block! hash! string!]

```