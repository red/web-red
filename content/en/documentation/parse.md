### parse
```red
USAGE:
     PARSE input rules

DESCRIPTION: 
     Process a series using dialected grammar rules. 
     PARSE is a native! value.

ARGUMENTS:
     input        [binary! any-block! any-string!] 
     rules        [block!] 

REFINEMENTS:
     /case        => Uses case-sensitive comparison.
     /part        => Limit to a length or position.
        length       [number! series!] 
     /trace       => 
        callback     [function! [event [word!] match? [logic!] rule [block!] input [series!] stack [block!] return: [logic!]]] 

RETURNS:
     [logic! block!]

```