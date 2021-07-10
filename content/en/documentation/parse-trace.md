### parse-trace
```red
USAGE:
     PARSE-TRACE input rules

DESCRIPTION: 
     Wrapper for parse/trace using the default event processor. 
     PARSE-TRACE is a function! value.

ARGUMENTS:
     input        [series!] 
     rules        [block!] 

REFINEMENTS:
     /case        => Uses case-sensitive comparison.
     /part        => Limit to a length or position.
        limit        [integer!] 

RETURNS:
     [logic! block!]

```