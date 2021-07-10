### load
```red
USAGE:
     LOAD source

DESCRIPTION: 
     Returns a value or block of values by reading and evaluating a source. 
     LOAD is a function! value.

ARGUMENTS:
     source       [file! url! string! binary!] 

REFINEMENTS:
     /header      => TBD.
     /all         => Load all values, returns a block. TBD: Don't evaluate Red header.
     /trap        => Load all values, returns [[values] position error].
     /next        => Load the next value only, updates source series word.
        position     [word!] "Word updated with new series position."
     /part        => Limit to a length or position.
        length       [integer! string!] 
     /into        => Put results in out block, instead of creating a new block.
        out          [block!] "Target block for results."
     /as          => Specify the type of data; use NONE to load as code.
        type         [word! none!] "E.g. bmp, gif, jpeg, png, redbin, json, csv."

```