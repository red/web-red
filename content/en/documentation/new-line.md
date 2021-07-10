### new-line
```red
USAGE:
     NEW-LINE position value

DESCRIPTION: 
     Sets or clears the new-line marker within a list series. 
     NEW-LINE is a native! value.

ARGUMENTS:
     position     [any-list!] "Position to change marker (modified)."
     value        [logic!] "Set TRUE for newline."

REFINEMENTS:
     /all         => Set/clear marker to end of series.
     /skip        => Set/clear marker periodically to the end of the series.
        size         [integer!] 

RETURNS:
     [any-list!]

```