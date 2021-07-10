### mold
```red
USAGE:
     MOLD value

DESCRIPTION: 
     Returns a source format string representation of a value. 
     MOLD is an action! value.

ARGUMENTS:
     value        [any-type!] 

REFINEMENTS:
     /only        => Exclude outer brackets if value is a block.
     /all         => TBD: Return value in loadable format.
     /flat        => Exclude all indentation.
     /part        => Limit the length of the result.
        limit        [integer!] 

RETURNS:
     [string!]

```