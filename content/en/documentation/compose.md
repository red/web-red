### compose
```red
USAGE:
     COMPOSE value

DESCRIPTION: 
     Returns a copy of a block, evaluating only parens. 
     COMPOSE is a native! value.

ARGUMENTS:
     value        [block!] 

REFINEMENTS:
     /deep        => Compose nested blocks.
     /only        => Compose nested blocks as blocks containing their values.
     /into        => Put results in out block, instead of creating a new block.
        out          [any-block!] "Target block for results, when /into is used."

```