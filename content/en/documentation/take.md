### take
```red
USAGE:
     TAKE series

DESCRIPTION: 
     Removes and returns one or more elements. 
     TAKE is an action! value.

ARGUMENTS:
     series       [series! port! none!] 

REFINEMENTS:
     /part        => Specifies a length or end position.
        length       [number! series!] 
     /deep        => Copy nested values.
     /last        => Take it from the tail end.

```