### debase
```red
USAGE:
     DEBASE value

DESCRIPTION: 
     Decodes binary-coded string (BASE-64 default) to binary value. 
     DEBASE is a native! value.

ARGUMENTS:
     value        [string!] "The string to decode."

REFINEMENTS:
     /base        => Binary base to use.
        base-value   [integer!] "The base to convert from: 64, 58, 16, or 2."

```