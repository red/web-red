### checksum
```red
USAGE:
     CHECKSUM data method

DESCRIPTION: 
     Computes a checksum, CRC, hash, or HMAC. 
     CHECKSUM is a native! value.

ARGUMENTS:
     data         [binary! string! file!] 
     method       [word!] {MD5 SHA1 SHA256 SHA384 SHA512 CRC32 TCP ADLER32 hash.}

REFINEMENTS:
     /with        => Extra value for HMAC key or hash table size; not compatible with TCP/CRC32/ADLER32 methods.
        spec         [any-string! binary! integer!] {String or binary for MD5/SHA* HMAC key, integer for hash table size.}

RETURNS:
     [integer! binary!]

```