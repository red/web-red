### function
```red
USAGE:
     FUNCTION spec body

DESCRIPTION: 
     Defines a function, making all set-words found in body, local. 
     FUNCTION is a native! value.

ARGUMENTS:
     spec         [block!] 
     body         [block!] 

REFINEMENTS:
     /extern      => Exclude words that follow this refinement.

```