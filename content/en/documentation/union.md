### union
```red
USAGE:
     UNION set1 set2

DESCRIPTION: 
     Returns the union of two data sets. 
     UNION is a native! value.

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