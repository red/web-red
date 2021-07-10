### enbase
```red
USAGE:
     ENBASE value

DESCRIPTION: 
     Encodes a string into a binary-coded string (BASE-64 default). 
     ENBASE is a native! value.

ARGUMENTS:
     value        [binary! string!] "If string, will be UTF8 encoded."

REFINEMENTS:
     /base        => Binary base to use.
        base-value   [integer!] "The base to convert from: 64, 58, 16, or 2."

```