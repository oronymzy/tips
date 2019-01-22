# converting tabular data

## converting a Markdown-formatted table to a [TSV] file

!!! attention
    
    The Markdown-formatted table is expected to be a [pipe table](https://pandoc.org/MANUAL.html#extension-pipe_tables) with a pipe character at the beginning of each line.

!!! note
    
    - {==foo.md==} represents an input text file containing a Markdown-formatted table.
    - {==bar.tsv==} represents an output [TSV] file.

Use `sed -e 's/ *| */|/g' -e 's/[|]/\t/g' -e 's/\t//' -e '2d' foo.md > bar.tsv`.

### explanation

- `s/ *| */|/g` removes spaces from around the pipe characters that separate table cells.
- `s/[|]/\t/g` replaces pipe characters with tab characters.
- `s/\t//` removes the first tab character on each line.
- `2d` removes the second line of the text file, the row of the table that indicates column alignment.

### prior work

- The method of putting a pipe character into a character class was introduced to me by [an answer on Stack Overflow by kriegaex](https://stackoverflow.com/questions/11987221/how-to-find-and-replace-all-percent-plus-and-pipe-signs/12234566#12234566).
- The method of removing spaces from around pipe characters was introduced to me by [an answer on Stack Overflow by Michael J. Barber](https://stackoverflow.com/questions/8005128/removing-spaces-from-the-fields-in-a-pipe-delimited-file-using-shell-script/8005385#8005385).
- The method of removing the first tab character on each line was introduced to me by [an answer on Stack Overflow by dfedde](https://stackoverflow.com/questions/20405342/replacing-first-occurence-in-every-line/20405516#20405516).
- The method of using *sed* to remove the line of a text file was introduced to me by [an answer on Stack Overflow by Brian Campbell](https://stackoverflow.com/questions/2112469/delete-specific-line-numbers-from-a-text-file-using-sed/2112496#2112496).

## converting a Markdown-formatted table to an SQLite database table

!!! warning
    
    [SQLite values](https://www.sqlite.org/rowvalue.html) will be [stored as text](https://www.sqlite.org/datatype3.html#storage_classes_and_datatypes), so any HTML formatting will omitted.

!!! note
    
    - {==foo.html==} represents an input HTML file containing an HTML table.
    - {==bar.sqlite==} represents an output SQLite database file.

[Convert the text file containing a Markdown-formatted table to an HTML file containing an HTML table](cnvffmt.md#MarkdowntoHTML), then use `sqlitebiter -o bar.sqlite file foo.html`.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[TSV]: https://en.wikipedia.org/wiki/Tab-separated_values
