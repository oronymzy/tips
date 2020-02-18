# managing tabular data

## selecting the first column of a [DSV] table

!!! note
    
    - {==foo.bar==} represents an input file containing a [delimiter-separated value](https://en.wikipedia.org/wiki/Delimiter-separated_values)-formatted table.
    - {==baz==} represents the delimiter character used by the input file, for example `,` (comma) for a [CSV] file, or `\t` (tab) for a [TSV] file.

Use `cut -d$'baz' -f1 foo.bar`.

### prior work

- The method of selecting a specific column was introduced to me by [an answer on Stack Overflow by Tom Ron](https://stackoverflow.com/questions/19490411/sed-awk-removing-text-between-delimiters/19490638#19490638).
- The method of specifying a tab-character delimiter was introduced to me by [an answer on Stack Exchange](https://unix.stackexchange.com/questions/35369/how-to-define-tab-delimiter-with-cut-in-bash/35370#35370).

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[CSV]: https://en.wikipedia.org/wiki/Comma-separated_values
[DSV]: https://en.wikipedia.org/wiki/Delimiter-separated_values
[TSV]: https://en.wikipedia.org/wiki/Tab-separated_values
