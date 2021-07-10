### open
```red
USAGE:
     OPEN port

DESCRIPTION: 
     Opens a port; makes a new port from a specification if necessary. 
     OPEN is an action! value.

ARGUMENTS:
     port         [port! file! url! block!] 

REFINEMENTS:
     /new         => Create new file - if it exists, deletes it.
     /read        => Open for read access.
     /write       => Open for write access.
     /seek        => Optimize for random access.
     /allow       => Specificies right access attributes.
        access       [block!] 

```