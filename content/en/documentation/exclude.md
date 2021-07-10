### exclude
```red
USAGE:
     EXCLUDE set1 set2

DESCRIPTION: 
     Returns the first data set less the second data set. 
     EXCLUDE is a native! value.

ARGUMENTS:
     set1         [block! hash! string! bitset! typeset!] 
     set2         [block! hash! string! bitset! typeset!] 

REFINEMENTS:
     /case        => Use case-sensitive comparison.
     /skip        => Treat the series as fixed size records.
        size         [integer!] 

RETURNS:
     [block! hash! string! bitset! typeset!]

```