### transcode
```red
USAGE:
     TRANSCODE src

DESCRIPTION: 
     Translates UTF-8 binary source to values. Returns one or several values in a block. 
     TRANSCODE is a native! value.

ARGUMENTS:
     src          [binary! string!] {UTF-8 input buffer; string argument will be UTF-8 encoded.}

REFINEMENTS:
     /next        => Translate next complete value (blocks as single value).
     /one         => Translate next complete value, returns the value only.
     /prescan     => Prescans only, do not load values. Returns guessed type.
     /scan        => Scans only, do not load values. Returns recognized type.
     /part        => Translates only part of the input buffer.
        length       [integer! binary!] "Length in bytes or tail position."
     /into        => Optionally provides an output block.
        dst          [block!] 
     /trace       => 
        callback     [function! [event [word!] input [binary! string!] type [word! datatype!] line [integer!] token return: [logic!]]] 

RETURNS:
     [block!]

```