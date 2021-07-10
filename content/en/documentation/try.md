### try
```red
USAGE:
     TRY block

DESCRIPTION: 
     Tries to DO a block and returns its value or an error. 
     TRY is a native! value.

ARGUMENTS:
     block        [block!] 

REFINEMENTS:
     /all         => Catch also BREAK, CONTINUE, RETURN, EXIT and THROW exceptions.
     /keep        => Capture and save the call stack in the error object.

```