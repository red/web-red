# Typesets

## Abstract

Typesets represents sets of datatype values stored in a compact array of bits (up to 96 bits), allowing for high performance runtime type-checking support.

Datatypes in a typeset may share common traits or behaviors, but that is not a requirement. A typeset can be created based on any criteria that suits the users needs.

See: [typeset\!](datatypes/typeset.adoc)

## Available typesets in Red

### all-word\!

  - make typeset\! \[[word\!](datatypes/word.adoc) [set-word\!](datatypes/set-word.adoc) [lit-word\!](datatypes/lit-word.adoc) [get-word\!](datatypes/get-word.adoc) [refinement\!](datatypes/refinement.adoc) [issue\!](datatypes/issue.adoc)\]

### any-block\!

  - make typeset\! \[[block\!](datatypes/block.adoc) [paren\!](datatypes/paren.adoc) [path\!](datatypes/path.adoc) [lit-path\!](datatypes/lit-path.adoc) [set-path\!](datatypes/set-path.adoc) [get-path\!](datatypes/get-path.adoc) [hash\!](datatypes/hash.adoc)\]

### any-function\!

  - make typeset\! \[[native\!](datatypes/native.adoc) [action\!](datatypes/action.adoc) [op\!](datatypes/op.adoc) [function\!](datatypes/function.adoc) [routine\!](datatypes/routine.adoc)\]

### any-list\!

  - make typeset\! \[[block\!](datatypes/block.adoc) [paren\!](datatypes/paren.adoc) [hash\!](datatypes/hash.adoc)\]

### any-object\!

  - make typeset\! \[[object\!](datatypes/object.adoc) [error\!](datatypes/error.adoc)\]

### any-path\!

  - make typeset\! \[[path\!](datatypes/path.adoc) [lit-path\!](datatypes/lit-path.adoc) [set-path\!](datatypes/set-path.adoc) [get-path\!](datatypes/get-path.adoc)\]

### any-string\!

  - make typeset\! \[[string\!](datatypes/string.adoc) [file\!](datatypes/file.adoc) [url\!](datatypes/url.adoc) [tag\!](datatypes/tag.adoc) [email\!](datatypes/email.adoc) [ref\!](datatypes/ref.adoc)\]

### any-type\!

  - make typeset\! \[[datatype\!](datatypes/datatype.adoc) [unset\!](datatypes/unset.adoc) [none\!](datatypes/none.adoc) [logic\!](datatypes/logic.adoc) [block\!](datatypes/block.adoc) [paren\!](datatypes/paren.adoc) [string\!](datatypes/string.adoc) [file\!](datatypes/file.adoc) [url\!](datatypes/url.adoc) [char\!](datatypes/none.char) [integer\!](datatypes/integer.adoc) [float\!](datatypes/float.adoc) [word\!](datatypes/word.adoc) [set-word\!](datatypes/set-word.adoc) [lit-word\!](datatypes/lit-word.adoc) [get-word\!](datatypes/get-word.adoc) [refinement\!](datatypes/refinement.adoc) [issue\!](datatypes/issue.adoc) [native\!](datatypes/native.adoc) [action\!](datatypes/action.adoc) [op\!](datatypes/op.adoc) [function\!](datatypes/function.adoc) [path\!](datatypes/path.adoc) [lit-path\!](datatypes/lit-path.adoc) [set-path\!](datatypes/set-path.adoc) [get-path\!](datatypes/get-path.adoc) [routine\!](datatypes/routine.adoc) [bitset\!](datatypes/bitset.adoc) [object\!](datatypes/object.adoc) [typeset\!](datatypes/typeset.adoc) [error\!](datatypes/error.adoc) [vector\!](datatypes/vector.adoc) [hash\!](datatypes/hash.adoc) [pair\!](datatypes/pair.adoc) [percent\!](datatypes/percent.adoc) [tuple\!](datatypes/tuple.adoc) [map\!](datatypes/map.adoc) [binary\!](datatypes/binary.adoc) [time\!](datatypes/time.adoc) [tag\!](datatypes/tag.adoc) [email\!](datatypes/email.adoc) [handle\!](datatypes/handle.adoc) [date\!](datatypes/date.adoc) [image\!](datatypes/image.adoc) [event\!](datatypes/event.adoc)\]

### any-word\!

  - make typeset\! \[[word\!](datatypes/word.adoc) [set-word\!](datatypes/set-word.adoc) [lit-word\!](datatypes/lit-word.adoc) [get-word\!](datatypes/get-word.adoc)\]

### default\!

  - make typeset\! \[[datatype\!](datatypes/datatype.adoc) [none\!](datatypes/none.adoc) [logic\!](datatypes/logic.adoc) [block\!](datatypes/block.adoc) [paren\!](datatypes/paren.adoc) [string\!](datatypes/string.adoc) [file\!](datatypes/file.adoc) [url\!](datatypes/url.adoc) [char\!](datatypes/none.char) [integer\!](datatypes/integer.adoc) [float\!](datatypes/float.adoc) [word\!](datatypes/word.adoc) [set-word\!](datatypes/set-word.adoc) [lit-word\!](datatypes/lit-word.adoc) [get-word\!](datatypes/get-word.adoc) [refinement\!](datatypes/refinement.adoc) [issue\!](datatypes/issue.adoc) [native\!](datatypes/native.adoc) [action\!](datatypes/action.adoc) [op\!](datatypes/op.adoc) [function\!](datatypes/function.adoc) [path\!](datatypes/path.adoc) [lit-path\!](datatypes/lit-path.adoc) [set-path\!](datatypes/set-path.adoc) [get-path\!](datatypes/get-path.adoc) [routine\!](datatypes/routine.adoc) [bitset\!](datatypes/bitset.adoc) [object\!](datatypes/object.adoc) [typeset\!](datatypes/typeset.adoc) [error\!](datatypes/error.adoc) [vector\!](datatypes/vector.adoc) [hash\!](datatypes/hash.adoc) [pair\!](datatypes/pair.adoc) [percent\!](datatypes/percent.adoc) [tuple\!](datatypes/tuple.adoc) [map\!](datatypes/map.adoc) [binary\!](datatypes/binary.adoc) [time\!](datatypes/time.adoc) [tag\!](datatypes/tag.adoc) [email\!](datatypes/email.adoc) [handle\!](datatypes/handle.adoc) [date\!](datatypes/date.adoc) [image\!](datatypes/image.adoc) [event\!](datatypes/event.adoc)\]

### external\!

  - make typeset\! \[[event\!](datatypes/event.adoc)\]

### immediate\!

  - make typeset\! \[[datatype\!](datatypes/datatype.adoc) [none\!](datatypes/none.adoc) [logic\!](datatypes/logic.adoc) [char\!](datatypes/char.adoc) [integer\!](datatypes/integer.adoc) [float\!](datatypes/float.adoc) [word\!](datatypes/word.adoc) [set-word\!](datatypes/set-word.adoc) [lit-word\!](datatypes/lit-word.adoc) [get-word\!](datatypes/get-word.adoc) [refinement\!](datatypes/refinement.adoc) [issue\!](datatypes/issue.adoc) [typeset\!](datatypes/typeset.adoc) [pair\!](datatypes/pair.adoc) [percent\!](datatypes/percent.adoc) [tuple\!](datatypes/tuple.adoc) [time\!](datatypes/time.adoc) [handle\!](datatypes/handle.adoc) [date\!](datatypes/date.adoc)\]

### internal\!

  - make typeset\! \[[unset\!](datatypes/unset.adoc) [float\!](datatypes/float.adoc) [percent\!](datatypes/percent.adoc)\]

### number\!

  - make typeset\! \[[integer\!](datatypes/integer.adoc) [float\!](datatypes/float.adoc) [percent\!](datatypes/percent.adoc)\]

### scalar\!

  - make typeset\! \[[char\!](datatypes/char.adoc) [integer\!](datatypes/integer.adoc) [float\!](datatypes/float.adoc) [pair\!](datatypes/pair.adoc) [percent\!](datatypes/percent.adoc) [tuple\!](datatypes/tuple.adoc) [time\!](datatypes/time.adoc) [date\!](datatypes/date.adoc) [money\!](datatypes/money.doc)\]

### series\!

  - make typeset\! \[[block\!](datatypes/block.adoc) [paren\!](datatypes/paren.adoc) [string\!](datatypes/string.adoc) [file\!](datatypes/file.adoc) [url\!](datatypes/url.adoc) [path\!](datatypes/path.adoc) [lit-path\!](datatypes/lit-path.adoc) [set-path\!](datatypes/set-path.adoc) [get-path\!](datatypes/get-path.adoc) [vector\!](datatypes/vector.adoc) [hash\!](datatypes/hash.adoc) [binary\!](datatypes/binary.adoc) [tag\!](datatypes/tag.adoc) [email\!](datatypes/email.adoc) [image\!](datatypes/image.adoc)\]
    
    A series in Red is defined as a sequence of elements, and a starting position which can be moved along the sequence of elements from the first position (`head`), to the last position (`tail`). The starting position of an empty series is at the last position (`tail`).
    
    Several references can be set to the same series with different starting positions:
    
    ``` red
    >> a: "hello"
    == "hello"
    
    >> b: next a
    == "ello"
    
    >> index? a
    == 1
    
    >> index? b
    == 2
    
    >> same? a b
    == false
    
    >> same? a head b
    == true
    
    >> append a " world"
    == "hello world"
    
    >> b
    == "ello world"
    ```
    
    The type of the elements in a series is dependant on the [datatype\!](datatypes/datatype.adoc) of the series. For example, a [block\!](datatypes/block.adoc) series can contain values of any type. A [string\!](datatypes/string.adoc) series can only contain [char\!](datatypes/char.adoc) values, etc.
    
    `Series!` provides an index variable that can be leveraged by all series [action\!](datatypes/action.adoc) values.
