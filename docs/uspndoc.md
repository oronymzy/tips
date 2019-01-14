# using [pandoc]

!!! note
    
    - {==foo.md==} represents an input text file formatted with [Pandoc Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown).
    - {==bar.html==} represents an output HTML file.

Use `pandoc -f markdown -t html "foo.md" -o "bar.html"` to convert a [Pandoc Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown)-formatted text file to an HTML file.

!!! note
    
    - {==foo.html==} represents an input HTML file.
    - {==bar.md==} represents an output text file formatted with [Pandoc Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown).

Use `pandoc -f html -t markdown-escaped_line_breaks --wrap=none "foo.html" -o "bar.md"` to convert an HTML file to a [Pandoc Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown)-formatted text file.

## explanation

!!! note
    
    This is an incomplete explanation.

- The `--wrap=none` [option](https://pandoc.org/MANUAL.html#option--wrap) disables text wrapping.
- `-escaped_line_breaks` [disables](https://pandoc.org/MANUAL.html#extensions) [the Pandoc Markdown extension for backslash-escaped line breaks](https://pandoc.org/MANUAL.html#paragraphs).

!!! note
    
    - {==foo.md==} represents an input text file formatted with [Pandoc Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown).
    - {==bar.docx==} represents an output Word DOCX file.
        - {==baz.docx==} represents a [style reference](https://pandoc.org/MANUAL.html#option--reference-doc) for the output Word DOCX file.

Use `pandoc -f markdown -t docx "foo.md" --reference-doc="baz.docx" --lua-filter=~/lua/pagebreak.lua -o "bar.docx"` to convert a [Pandoc Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown)-formatted text file to a Word DOCX file, using *baz.docx* as a [style reference](https://pandoc.org/MANUAL.html#option--reference-doc) and `pagebreak.lua` to [produce page breaks](ipbkMkd.md#pandoc-filters-and-latex).

## tables
Converting HTML tables to pipe Markdown tables is tricky, and seems to involve manually removing any column width information and then re-converting to non-grid, non-simple, non-multiline [tables](https://pandoc.org/MANUAL.html#tables) using non-pandoc syntax extensions[^uspndoc1]. Some HTML may still be left over and require manual editing. An example would be `pandoc -f html -t markdown-grid_tables-multiline_tables-simple_tables --wrap=none -o output.md foo.html`, where *foo.html* is the HTML input file and *bar.md* is the Markdown-formatted output file.

!!! attention
    
    In order for Markdown-style tables to be rendered properly in HTML, a pipe must be included at the beginning of each line.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[pandoc]: http://pandoc.org/
[^uspndoc1]: https://pandoc.org/MANUAL.html#non-pandoc-extensions
