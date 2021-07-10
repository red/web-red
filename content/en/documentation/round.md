### round
```red
USAGE:
     ROUND n

DESCRIPTION: 
     Returns the nearest integer. Halves round up (away from zero) by default. 
     ROUND is an action! value.

ARGUMENTS:
     n            [number! money! time! pair!] 

REFINEMENTS:
     /to          => Return the nearest multiple of the scale parameter.
        scale        [number! money! time!] "If zero, returns N unchanged."
     /even        => Halves round toward even results.
     /down        => Round toward zero, ignoring discarded digits. (truncate).
     /half-down   => Halves round toward zero.
     /floor       => Round in negative direction.
     /ceiling     => Round in positive direction.
     /half-ceiling => Halves round in positive direction.

```