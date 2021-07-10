### do
```red
USAGE:
     DO value

DESCRIPTION: 
     Evaluates a value, returning the last evaluation result. 
     DO is a native! value.

ARGUMENTS:
     value        [any-type!] 

REFINEMENTS:
     /expand      => Expand directives before evaluation.
     /args        => If value is a script, this will set its system/script/args.
        arg           "Args passed to a script (normally a string)."
     /next        => Do next expression only, return it, update block word.
        position     [word!] "Word updated with new block position."

```