### decompress
```red
USAGE:
     DECOMPRESS data

DESCRIPTION: 
     Decompresses data. Data in GZIP format (RFC 1952) by default. 
     DECOMPRESS is a native! value.

ARGUMENTS:
     data         [binary!] 

REFINEMENTS:
     /zlib        => Data in ZLIB format (RFC 1950).
        size         [integer!] "Uncompressed data size. Use 0 if don't know."
     /deflate     => Data in DEFLATE format (RFC 1951).
        size         [integer!] "Uncompressed data size. Use 0 if don't know."

```