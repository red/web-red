### clean-path
```red
USAGE:
     CLEAN-PATH file

DESCRIPTION: 
     Cleans-up '.' and '..' in path; returns the cleaned path. 
     CLEAN-PATH is a function! value.

ARGUMENTS:
     file         [file! url! string!] 

REFINEMENTS:
     /only        => Do not prepend current directory.
     /dir         => Add a trailing / if missing.

```