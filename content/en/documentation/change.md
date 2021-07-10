### change
```red
USAGE:
     CHANGE series value

DESCRIPTION: 
     Changes a value in a series and returns the series after the change. 
     CHANGE is an action! value.

ARGUMENTS:
     series       [series! port!] "Series at point to change."
     value        [any-type!] "The new value."

REFINEMENTS:
     /part        => Limits the amount to change to a given length or position.
        range        [number! series!] 
     /only        => Changes a series as a series.
     /dup         => Duplicates the change a specified number of times.
        count        [number!] 

```