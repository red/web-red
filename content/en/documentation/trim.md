### trim
```red
USAGE:
     TRIM series

DESCRIPTION: 
     Removes space from a string or NONE from a block. 
     TRIM is an action! value.

ARGUMENTS:
     series       [series! port!] 

REFINEMENTS:
     /head        => Removes only from the head.
     /tail        => Removes only from the tail.
     /auto        => Auto indents lines relative to first line.
     /lines       => Removes all line breaks and extra spaces.
     /all         => Removes all whitespace.
     /with        => Same as /all, but removes characters in 'str'.
        str          [char! string! binary! integer!] 

```