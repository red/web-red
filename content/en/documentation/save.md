### save
```red
USAGE:
     SAVE where value

DESCRIPTION: 
     Saves a value, block, or other data to a file, URL, binary, or string. 
     SAVE is a function! value.

ARGUMENTS:
     where        [file! url! string! binary! none!] "Where to save."
     value        [any-type!] "Value(s) to save."

REFINEMENTS:
     /header      => Provide a Red header block (or output non-code datatypes).
        header-data  [block! object!] 
     /all         => TBD: Save in serialized format.
     /length      => Save the length of the script content in the header.
     /as          => Specify the format of data; use NONE to save as plain text.
        format       [word! none!] "E.g. bmp, gif, jpeg, png, redbin, json, csv."

```