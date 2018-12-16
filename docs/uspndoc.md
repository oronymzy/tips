# using [pandoc]
Converting HTML tables to pipe Markdown tables is tricky, and seems to involve manually removing any column width information and then re-converting to non-grid, non-simple, non-multiline [tables](https://pandoc.org/MANUAL.html#tables) using non-pandoc syntax extensions[^uspndoc1]. Some HTML may still be left over and require manual editing. An example would be `pandoc -f html -t markdown-grid_tables-multiline_tables-simple_tables --wrap=none -o output.md foo.html`, where *foo.html* is the HTML input file and *bar.md* is the Markdown output file.

!!! attention
    
    In order for Markdown-style tables to be rendered properly in HTML, a pipe must be included at the beginning of each line.

[pandoc]: http://pandoc.org/
[^uspndoc1]: https://pandoc.org/MANUAL.html#non-pandoc-extensions
