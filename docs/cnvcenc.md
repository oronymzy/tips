# [converting character encodings]

!!! note
    
    - {==foo==} and {==bar==} represent the character encodings of the input and output files, respectively.
    - {==foo.bar==} and {==bar.baz==} represent the filenames of the input and output files, respectively.

In Linux, use `iconv -f foo -t bar foo.bar > bar.baz`.

## converting an [HTML character entity reference] to a [UTF-8] character {: #HTMLcertoUTF8 }

!!! note
    
    - {==foo.bar==} represents the filename of an input file containing an [HTML character entity reference].
    - {==bar.baz==} represents the filename of an output file containing an [HTML character entity reference] converted to a [UTF-8] character.

Use `<foo.bar recode html..utf8 > bar.baz`

## prior work
- The method of converting an [HTML character entity reference] to a [UTF-8] character was introduced to me by [an answer on Stack Overflow by ceving](https://stackoverflow.com/questions/5929492/bash-script-to-convert-from-html-entities-to-characters/5929519#5929519).
- The method of converting character encodings with [iconv](https://en.wikipedia.org/wiki/Iconv) was introduced to me by [an answer on Stack Overflow by Troels Arvin](https://stackoverflow.com/questions/64860/best-way-to-convert-text-files-between-character-sets/64889#64889).

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[converting character encodings]: https://en.wikipedia.org/wiki/Character_encoding#Character_encoding_translation
[HTML character entity reference]: https://en.wikipedia.org/wiki/List_of_XML_and_HTML_character_entity_references#Character_entity_references_in_HTML
[UTF-8]: https://en.wikipedia.org/wiki/UTF-8
