### get
```red
USAGE:
     GET word

DESCRIPTION: 
     Returns the value a word refers to. 
     GET is a native! value.

ARGUMENTS:
     word         [any-word! any-path! object!] 

REFINEMENTS:
     /any         => If word has no value, return UNSET rather than causing an error.
     /case        => Use case-sensitive comparison (path only).

RETURNS:
     [any-type!]

```