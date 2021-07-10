### reverse
```red
USAGE:
     REVERSE series

DESCRIPTION: 
     Reverses the order of elements; returns at same position. 
     REVERSE is an action! value.

ARGUMENTS:
     series       [series! port! pair! tuple!] 

REFINEMENTS:
     /part        => Limits to a given length or position.
        length       [number! series!] 
     /skip        => Treat the series as fixed size records.
        size         [integer!] 

RETURNS:
     [series! port! pair! tuple!]

```