### now
```red
USAGE:
     NOW 

DESCRIPTION: 
     Returns date and time. 
     NOW is a native! value.

REFINEMENTS:
     /year        => Returns year only.
     /month       => Returns month only.
     /day         => Returns day of the month only.
     /time        => Returns time only.
     /zone        => Returns time zone offset from UTC (GMT) only.
     /date        => Returns date only.
     /weekday     => Returns day of the week as integer (Monday is day 1).
     /yearday     => Returns day of the year (Julian).
     /precise     => High precision time.
     /utc         => Universal time (no zone).

RETURNS:
     [date! time! integer!]

```