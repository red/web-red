### append
```red
USAGE:
     APPEND series value

DESCRIPTION: 
     Inserts value(s) at series tail; returns series head. 
     APPEND is an action! value.

ARGUMENTS:
     series       [series! bitset! port!] 
     value        [any-type!] 

REFINEMENTS:
     /part        => Limit the number of values inserted.
        length       [number! series!] 
     /only        => Insert block types as single values (overrides /part).
     /dup         => Duplicate the inserted values.
        count        [integer!] 

RETURNS:
     [series! port! bitset!]

```