### request-dir
```red
USAGE:
     REQUEST-DIR 

DESCRIPTION: 
     Asks user to select a directory and returns full directory path (or block of paths). 
     REQUEST-DIR is a function! value.

REFINEMENTS:
     /title       => Window title.
        text         [string!] 
     /dir         => Set starting directory.
        name         [string! file!] 
     /filter      => TBD: Block of filters (filter-name filter).
        list         [block!] 
     /keep        => Keep previous directory path.
     /multi       => TBD: Allows multiple file selection, returned as a block.

```