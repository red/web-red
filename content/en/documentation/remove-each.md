### remove-each
```red
USAGE:
     REMOVE-EACH 'word data body

DESCRIPTION: 
     Removes values for each block that returns truthy value. 
     REMOVE-EACH is a native! value.

ARGUMENTS:
     'word        [word! block!] "Word or block of words to set each time."
     data         [series!] "The series to traverse (modified)."
     body         [block!] {Block to evaluate (return truthy value to remove).}

```