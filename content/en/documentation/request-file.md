### request-file
```red
USAGE:
     REQUEST-FILE 

DESCRIPTION: 
     Asks user to select a file and returns full file path (or block of paths). 
     REQUEST-FILE is a function! value.

REFINEMENTS:
     /title       => Window title.
        text         [string!] 
     /file        => Default file name or directory.
        name         [string! file!] 
     /filter      => Block of filters (filter-name filter).
        list         [block!] 
     /save        => File save mode.
     /multi       => Allows multiple file selection, returned as a block.

```