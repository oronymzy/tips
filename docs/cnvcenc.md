# [converting character encodings]

!!! note
    
    - {==foo==} and {==bar==} represent the character encodings of the input and output files, respectively.
    - {==foo.bar==} and {==bar.baz==} represent the filenames of the input and output files, respectively.

In Linux, use `iconv -f foo -t bar foo.bar > bar.baz`.

### prior work
The method of converting character encodings with [iconv](https://en.wikipedia.org/wiki/Iconv) was introduced to me by [an answer on Stack Overflow by Troels Arvin](https://stackoverflow.com/questions/64860/best-way-to-convert-text-files-between-character-sets/64889#64889).

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[converting character encodings]: https://en.wikipedia.org/wiki/Character_encoding#Character_encoding_translation
