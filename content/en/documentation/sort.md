### sort
```red
USAGE:
     SORT series

DESCRIPTION: 
     Sorts a series (modified); default sort order is ascending. 
     SORT is an action! value.

ARGUMENTS:
     series       [series! port!] 

REFINEMENTS:
     /case        => Perform a case-sensitive sort.
     /skip        => Treat the series as fixed size records.
        size         [integer!] 
     /compare     => Comparator offset, block (TBD) or function.
        comparator   [integer! block! any-function!] 
     /part        => Sort only part of a series.
        length       [number! series!] 
     /all         => Compare all fields (used with /skip).
     /reverse     => Reverse sort order.
     /stable      => Stable sorting.

RETURNS:
     [series!]

```