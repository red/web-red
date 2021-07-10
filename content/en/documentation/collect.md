### collect
```red
USAGE:
     COLLECT body

DESCRIPTION: 
     Collect in a new block all the values passed to KEEP function from the body block. 
     COLLECT is a function! value.

ARGUMENTS:
     body         [block!] "Block to evaluate."

REFINEMENTS:
     /into        => Insert into a buffer instead (returns position after insert).
        collected    [series!] "The buffer series (modified)."

```