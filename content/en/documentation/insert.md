### insert
```red
USAGE:
     INSERT series value

DESCRIPTION: 
     Inserts value(s) at series index; returns series past the insertion. 
     INSERT is an action! value.

ARGUMENTS:
     series       [series! port! bitset!] 
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