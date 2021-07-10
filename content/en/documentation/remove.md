### remove
```red
USAGE:
     REMOVE series

DESCRIPTION: 
     Returns the series at the same index after removing a value. 
     REMOVE is an action! value.

ARGUMENTS:
     series       [series! port! bitset! map! none!] 

REFINEMENTS:
     /part        => Removes a number of values, or values up to the given series index.
        length       [number! char! series!] 
     /key         => Removes a key in map.
        key-arg      [scalar! any-string! any-word! binary! block!] 

RETURNS:
     [series! port! bitset! map! none!]

```