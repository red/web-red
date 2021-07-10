### write
```red
USAGE:
     WRITE destination data

DESCRIPTION: 
     Writes to a file, URL, or other port. 
     WRITE is an action! value.

ARGUMENTS:
     destination  [file! url! port!] 
     data         [any-type!] 

REFINEMENTS:
     /binary      => Preserves contents exactly.
     /lines       => Write each value in a block as a separate line.
     /info        => 
     /append      => Write data at end of file.
     /part        => Partial write a given number of units.
        length       [number!] 
     /seek        => Write at a specific position.
        index        [number!] 
     /allow       => Specifies protection attributes.
        access       [block!] 
     /as          => Write with the specified encoding, default is 'UTF-8.
        encoding     [word!] 

```