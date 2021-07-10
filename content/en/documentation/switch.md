### switch
```red
USAGE:
     SWITCH value cases

DESCRIPTION: 
     Evaluates the first block following the value found in cases. 
     SWITCH is a native! value.

ARGUMENTS:
     value        [any-type!] "The value to match."
     cases        [block!] 

REFINEMENTS:
     /default     => Specify a default block, if value is not found in cases.
        case         [block!] "Default block to evaluate."

```