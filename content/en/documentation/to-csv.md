### to-csv
```red
USAGE:
     TO-CSV data

DESCRIPTION: 
     Make CSV data from input value. 
     TO-CSV is a function! value.

ARGUMENTS:
     data         [block! map! object!] {May be block of fixed size records, block of block records, or map columns.}

REFINEMENTS:
     /with        => Delimiter to use (default is comma).
        delimiter    [char! string!] 
     /skip        => Treat block as table of records with fixed length.
        size         [integer!] 
     /quote       => 
        qt-char      [char!] {Use different character for quotes than double quote (").}

```