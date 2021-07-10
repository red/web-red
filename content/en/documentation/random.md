### random
```red
USAGE:
     RANDOM value

DESCRIPTION: 
     Returns a random value of the same datatype; or shuffles series. 
     RANDOM is an action! value.

ARGUMENTS:
     value         "Maximum value of result (modified when series)."

REFINEMENTS:
     /seed        => Restart or randomize.
     /secure      => Returns a cryptographically secure random number.
     /only        => Pick a random value from a series.

RETURNS:
     [any-type!]

```