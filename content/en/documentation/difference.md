### difference
```red
USAGE:
     DIFFERENCE set1 set2

DESCRIPTION: 
     Returns the special difference of two data sets. 
     DIFFERENCE is a native! value.

ARGUMENTS:
     set1         [block! hash! string! bitset! typeset! date!] 
     set2         [block! hash! string! bitset! typeset! date!] 

REFINEMENTS:
     /case        => Use case-sensitive comparison.
     /skip        => Treat the series as fixed size records.
        size         [integer!] 

RETURNS:
     [block! hash! string! bitset! typeset! time!]

```