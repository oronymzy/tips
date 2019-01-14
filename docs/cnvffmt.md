# converting file formats

## converting PDF to HTML {: #PDFtoHTML }

!!! warning
    
    pdftohtml can produce PDF conversions with some of the content from the original PDF missing. **It is not certain to work.**

!!! note
    
    - {==foo.pdf==} represents an input PDF file.
    - {==bar.html==} represents an output HTML file.

Use `pdftohtml -s foo.pdf bar.html` to convert a PDF file to an HTML file, including images. The `-s` [option](https://www.mankier.com/1/pdftohtml) combines all PDF pages into a single HTML page.

### converting PDF to HTML to Markdown {: #PDFtoHTMLtoMarkdown }

!!! note
    
    - {==foo.pdf==} represents an input PDF file.
    - {==bar.md==} represents an output text file formatted with [Pandoc Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown).

Use `pdftohtml -stdout foo.pdf | pandoc -f html -t markdown-escaped_line_breaks --wrap=none -o bar.md` to convert a PDF file to an HTML file to a [Pandoc Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown)-formatted text file, including images.

#### explanation

!!! note
    
    This is an incomplete explanation.

- The `-stdout` [option](https://www.mankier.com/1/pdftohtml) writes the results of *pdftohtml* to [standard output](https://en.wikipedia.org/wiki/Standard_streams#Standard_output_(stdout)).
- The `--wrap=none` [option](https://pandoc.org/MANUAL.html#option--wrap) disables text wrapping.
- `-escaped_line_breaks` [disables](https://pandoc.org/MANUAL.html#extensions) [the Pandoc Markdown extension for backslash-escaped line breaks](https://pandoc.org/MANUAL.html#paragraphs).

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**
