### extract
```red
USAGE:
     EXTRACT series width

DESCRIPTION: 
     Extracts a value from a series at regular intervals. 
     EXTRACT is a function! value.

ARGUMENTS:
     series       [series!] 
     width        [integer!] "Size of each entry (the skip)."

REFINEMENTS:
     /index       => Extract from an offset position.
        pos          [integer!] "The position."
     /into        => Provide an output series instead of creating a new one.
        output       [series!] "Output series."

```