### scan
```red
USAGE:
     SCAN buffer

DESCRIPTION: 
     Returns the guessed type of the first serialized value from the input. 
     SCAN is a function! value.

ARGUMENTS:
     buffer       [binary! string!] "Input UTF-8 buffer or string."

REFINEMENTS:
     /next        => Returns both the type and the input after the value.
     /fast        => Fast scanning, returns best guessed type.

RETURNS:
     Recognized or guessed type, or NONE on empty input.
     [datatype! none!]

```