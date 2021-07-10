### load-csv
```red
USAGE:
     LOAD-CSV data

DESCRIPTION: 
     Converts CSV text to a block of rows, where each row is a block of fields. 
     LOAD-CSV is a function! value.

ARGUMENTS:
     data         [string!] "Text CSV data to load."

REFINEMENTS:
     /with        => 
        delimiter    [char! string!] "Delimiter to use (default is comma)."
     /header      => Treat first line as header; implies /as-columns if /as-records is not used.
     /as-columns  => Returns named columns; default names if /header is not used.
     /as-records  => Returns records instead of rows; implies /header.
     /flat        => Returns a flat block; you need to know the number of fields.
     /trim        => Ignore spaces between quotes and delimiter.
     /quote       => 
        qt-char      [char!] {Use different character for quotes than double quote (").}

```