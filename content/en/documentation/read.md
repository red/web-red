### read
```red
USAGE:
     READ source

DESCRIPTION: 
     Reads from a file, URL, or other port. 
     READ is an action! value.

ARGUMENTS:
     source       [file! url! port!] 

REFINEMENTS:
     /part        => Partial read a given number of units (source relative).
        length       [number!] 
     /seek        => Read from a specific position (source relative).
        index        [number!] 
     /binary      => Preserves contents exactly.
     /lines       => Convert to block of strings.
     /info        => 
     /as          => Read with the specified encoding, default is 'UTF-8.
        encoding     [word!] 

```