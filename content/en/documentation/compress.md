### compress
```red
USAGE:
     COMPRESS data

DESCRIPTION: 
     compresses data. return GZIP format (RFC 1952) by default. 
     COMPRESS is a native! value.

ARGUMENTS:
     data         [any-string! binary!] 

REFINEMENTS:
     /zlib        => Return ZLIB format (RFC 1950).
     /deflate     => Return DEFLATE format (RFC 1951).

```