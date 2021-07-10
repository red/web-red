### copy
```red
USAGE:
     COPY value

DESCRIPTION: 
     Returns a copy of a non-scalar value. 
     COPY is an action! value.

ARGUMENTS:
     value        [series! any-object! bitset! map!] 

REFINEMENTS:
     /part        => Limit the length of the result.
        length       [number! series! pair!] 
     /deep        => Copy nested values.
     /types       => Copy only specific types of non-scalar values.
        kind         [datatype!] 

RETURNS:
     [series! any-object! bitset! map!]

```