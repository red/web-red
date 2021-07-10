### size-text
```red
USAGE:
     SIZE-TEXT face

DESCRIPTION: 
     Returns the area size of the text in a face. 
     SIZE-TEXT is a function! value.

ARGUMENTS:
     face         [object!] "Face containing the text to size."

REFINEMENTS:
     /with        => Provide a text string instead of face/text.
        text         [string!] "Text to measure."

RETURNS:
     Return the text's size or NONE if failed.
     [pair! none!]

```