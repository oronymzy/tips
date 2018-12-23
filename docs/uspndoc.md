# using [pandoc]
Use `pandoc -f markdown -t html "foo.md" -o "bar.html"` to convert a [Pandoc Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown)-formatted text file named *foo.md* to an HTML file named *bar.html*.

Use `pandoc -f markdown -t docx "input.md" --reference-doc="baz.docx" --lua-filter=~/lua/pagebreak.lua -o "bar.docx"` to convert *input.md*, a Markdown-formatted text file, to *bar.docx*, using *baz.docx* as a [reference](https://pandoc.org/MANUAL.html#option--reference-doc) and `pagebreak.lua` to [produce page breaks](ipbkMkd.md#pandoc-filters-and-latex).

## tables
Converting HTML tables to pipe Markdown tables is tricky, and seems to involve manually removing any column width information and then re-converting to non-grid, non-simple, non-multiline [tables](https://pandoc.org/MANUAL.html#tables) using non-pandoc syntax extensions[^uspndoc1]. Some HTML may still be left over and require manual editing. An example would be `pandoc -f html -t markdown-grid_tables-multiline_tables-simple_tables --wrap=none -o output.md foo.html`, where *foo.html* is the HTML input file and *bar.md* is the Markdown-formatted output file.

!!! attention
    
    In order for Markdown-style tables to be rendered properly in HTML, a pipe must be included at the beginning of each line.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[pandoc]: http://pandoc.org/
[^uspndoc1]: https://pandoc.org/MANUAL.html#non-pandoc-extensions
