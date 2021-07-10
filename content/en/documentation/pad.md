### pad
```red
USAGE:
     PAD str n

DESCRIPTION: 
     Pad a FORMed value on right side with spaces. 
     PAD is a function! value.

ARGUMENTS:
     str           "Value to pad, FORM it if not a string."
     n            [integer!] "Total size (in characters) of the new string."

REFINEMENTS:
     /left        => Pad the string on left side.
     /with        => Pad with char.
        c            [char!] 

RETURNS:
     Modified input string at head.
     [string!]

```