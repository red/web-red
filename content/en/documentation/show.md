### show
```red
USAGE:
     SHOW face

DESCRIPTION: 
     Display a new face or update it. 
     SHOW is a function! value.

ARGUMENTS:
     face         [object! block!] "Face object to display."

REFINEMENTS:
     /with        => Link the face to a parent face.
        parent       [object!] "Parent face to link to."
     /force       => For internal use only!.

RETURNS:
     true if success.
     [logic!]

```