# converting file formats

## converting HTML to Markdown {: #HTMLtoMarkdown}

!!! note
    
    - {==foo.html==} represents an input HTML file.
    - {==bar.md==} represents an output text file formatted with [Pandoc Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown).

Use `pandoc -f html -t markdown-escaped_line_breaks --wrap=none "foo.html" -o "bar.md"` to convert an HTML file to a [Pandoc Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown)-formatted text file.

### explanation

!!! note
    
    This is an incomplete explanation.

- The `--wrap=none` [option](https://pandoc.org/MANUAL.html#option--wrap) disables text wrapping.
- `-escaped_line_breaks` [disables](https://pandoc.org/MANUAL.html#extensions) [the Pandoc Markdown extension for backslash-escaped line breaks](https://pandoc.org/MANUAL.html#paragraphs).

## converting Markdown to DOCX {: #MarkdowntoDOCX }

!!! note
    
    - {==foo.md==} represents an input text file formatted with [Pandoc Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown).
    - {==bar.docx==} represents an output Word DOCX file.
        - {==baz.docx==} represents a [style reference](https://pandoc.org/MANUAL.html#option--reference-doc) for the output Word DOCX file.

Use `pandoc -f markdown -t docx "foo.md" --reference-doc="baz.docx" --lua-filter=~/lua/pagebreak.lua -o "bar.docx"` to convert a [Pandoc Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown)-formatted text file to a Word DOCX file, using *baz.docx* as a [style reference](https://pandoc.org/MANUAL.html#option--reference-doc) and `pagebreak.lua` to [produce page breaks](ipbkMkd.md#pandoc-filters-and-latex).

## converting Markdown to HTML {: #MarkdowntoHTML }

!!! note
    
    - {==foo.md==} represents an input text file formatted with [Pandoc Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown).
    - {==bar.html==} represents an output HTML file.

Use `pandoc -f markdown -t html "foo.md" -o "bar.html"` to convert a [Pandoc Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown)-formatted text file to an HTML file.

## converting PDF to text {: #PDFtotext }

!!! note
    
    - {==foo.pdf==} represents an input PDF file.
    - {==bar.txt==} represents an output text file.

Use `pdftotext -layout foo.pdf bar.txt` to convert a PDF file to a text file. The `-layout` [option](https://www.mankier.com/1/pdftotext) attempts to preserve the layout of the PDF when converting.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**
