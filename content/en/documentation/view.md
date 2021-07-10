### view
```red
USAGE:
     VIEW spec

DESCRIPTION: 
     Displays a window view from a layout block or from a window face. 
     VIEW is a function! value.

ARGUMENTS:
     spec         [block! object!] "Layout block or face object."

REFINEMENTS:
     /tight       => Zero offset and origin.
     /options     => 
        opts         [block!] "Optional features in [name: value] format."
     /flags       => 
        flgs         [block! word!] "One or more window flags."
     /no-wait     => Return immediately - do not wait.

```