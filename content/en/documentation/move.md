### move
```red
USAGE:
     MOVE origin target

DESCRIPTION: 
     Moves one or more elements from one series to another position or series. 
     MOVE is an action! value.

ARGUMENTS:
     origin       [series! port!] 
     target       [series! port!] 

REFINEMENTS:
     /part        => Limit the number of values inserted.
        length       [integer!] 

RETURNS:
     [series! port!]

```