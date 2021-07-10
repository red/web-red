### to-local-file
```red
USAGE:
     TO-LOCAL-FILE path

DESCRIPTION: 
     Converts a Red file path to the local system file path. 
     TO-LOCAL-FILE is a native! value.

ARGUMENTS:
     path         [file! string!] 

REFINEMENTS:
     /full        => Prepends current dir for full path (for relative paths only).

RETURNS:
     [string!]

```