### select
```red
USAGE:
     SELECT series value

DESCRIPTION: 
     Find a value in a series and return the next value, or NONE. 
     SELECT is an action! value.

ARGUMENTS:
     series       [series! any-object! map! none!] 
     value        [any-type!] 

REFINEMENTS:
     /part        => Limit the length of the search.
        length       [number! series!] 
     /only        => Treat a series search value as a single value.
     /case        => Perform a case-sensitive search.
     /same        => Use "same?" as comparator.
     /any         => TBD: Use * and ? wildcards in string searches.
     /with        => TBD: Use custom wildcards in place of * and ?.
        wild         [string!] 
     /skip        => Treat the series as fixed size records.
        size         [integer!] 
     /last        => Find the last occurrence of value, from the tail.
     /reverse     => Find the last occurrence of value, from the current index.

RETURNS:
     [any-type!]

```