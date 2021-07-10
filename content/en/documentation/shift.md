### shift
```red
USAGE:
     SHIFT data bits

DESCRIPTION: 
     Perform a bit shift operation. Right shift (decreasing) by default. 
     SHIFT is a native! value.

ARGUMENTS:
     data         [integer!] 
     bits         [integer!] 

REFINEMENTS:
     /left        => Shift bits to the left (increasing).
     /logical     => Use logical shift (unsigned, fill with zero).

RETURNS:
     [integer!]

```