# using [pandoc]

## tables
Converting HTML tables to pipe Markdown tables is tricky, and seems to involve manually removing any column width information and then re-converting to non-grid, non-simple, non-multiline [tables](https://pandoc.org/MANUAL.html#tables) using non-pandoc syntax extensions[^uspndoc1]. Some HTML may still be left over and require manual editing. An example would be `pandoc -f html -t markdown-grid_tables-multiline_tables-simple_tables --wrap=none -o output.md foo.html`, where *foo.html* is the HTML input file and *bar.md* is the Markdown-formatted output file.

!!! attention
    
    In order for Markdown-style tables to be rendered properly in HTML, a pipe must be included at the beginning of each line.

## [pandoc Markdown] output
[Indented code blocks](https://pandoc.org/MANUAL.html#indented-code-blocks) cannot be disabled for pandoc Markdown output.[^uspndoc4]

## plain text output
The formatting of plain text output is based on the formatting of [Project Gutenberg](https://www.gutenberg.org/wiki/Main_Page).[^uspndoc2] Specifically:

- Emphasis is indicated with surrounding underscores (`_`) and strong emphasis is indicated with [all caps](https://en.wikipedia.org/wiki/All_caps).[^uspndoc3]
- Footnote references are indicated with numbers within square brackets (`[n]`).[^uspndoc3]
- Level one headings are indicated with [all caps](https://en.wikipedia.org/wiki/All_caps).[^uspndoc3]

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[pandoc]: http://pandoc.org/
[pandoc Markdown]: https://pandoc.org/MANUAL.html#pandocs-markdown
[^uspndoc1]: <https://pandoc.org/MANUAL.html#non-pandoc-extensions>
[^uspndoc2]: <https://stackoverflow.com/questions/34132549/pandoc-markdown-to-plain-text-formatting/34139581#34139581>
[^uspndoc3]: <https://github.com/jgm/pandoc/blob/6d91fb25639c6ac985d15c7112e009533d06e5f2/changelog>
[^uspndoc4]: <https://github.com/jgm/pandoc/issues/2120#issuecomment-99156655>
