# converting file formats

## converting HTML to Markdown {: #HTMLtoMarkdown}

!!! note
    
    - {==foo.html==} represents an input HTML file.
    - {==bar.md==} represents an output text file formatted with [Pandoc Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown).

Use `pandoc -f html-native_divs-native_spans -t markdown-escaped_line_breaks-fenced_divs-header_attributes-fenced_code_attributes-inline_code_attributes-bracketed_spans-smart --atx-headers --wrap=none "foo.html" -o "bar.md"` to convert an HTML file to a [Pandoc Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown)-formatted text file.

### explanation

!!! note
    
    This is an incomplete explanation.

- The `--atx-headers` [option](https://pandoc.org/MANUAL.html#option--atx-headers) produces [ATX-style headings](https://pandoc.org/MANUAL.html#atx-style-headers) for all heading levels, overriding the default behavior of producing [Setext-style Markdown headings](https://pandoc.org/MANUAL.html#setext-style-headers) for levels 1 and 2.
- The `--wrap=none` [option](https://pandoc.org/MANUAL.html#option--wrap) disables text wrapping.
- Pandoc Markdown output
    - `-bracketed_spans` [disables](https://pandoc.org/MANUAL.html#extensions) [the Pandoc Markdown extension for bracketed spans](https://pandoc.org/MANUAL.html#extension-bracketed_spans).
    - `-escaped_line_breaks` [disables](https://pandoc.org/MANUAL.html#extensions) [the Pandoc Markdown extension for backslash-escaped line breaks](https://pandoc.org/MANUAL.html#paragraphs).
    - `-fenced_code_attributes` [disables](https://pandoc.org/MANUAL.html#extensions) [the Pandoc Markdown extension for assigning attribute lists to fenced code blocks](https://pandoc.org/MANUAL.html#extension-fenced_code_attributes).
    - `-header_attributes` [disables](https://pandoc.org/MANUAL.html#extensions) [the Pandoc Markdown extension for assigning attribute lists to headings](https://pandoc.org/MANUAL.html#extension-header_attributes).
    - `-inline_code_attributes` [disables](https://pandoc.org/MANUAL.html#extensions) [the Pandoc Markdown extension for assigning attribute lists to inline code](https://pandoc.org/MANUAL.html#extension-inline_code_attributes).
    - `-smart` [disables](https://pandoc.org/MANUAL.html#extensions) [the extension for interpreting ASCII characters as curly quotes, em-dashes, en-dashes, and ellipses, and for inserting nonbreaking spaces](https://pandoc.org/MANUAL.html#extension-smart). Backslash-escaped double-quotes `\"` are also no longer produced.
- HTML input
    - `-native_divs` [disables](https://pandoc.org/MANUAL.html#extensions) [the raw HTML extension for preserving native `<div>` HTML elements](https://pandoc.org/MANUAL.html#native_divs).
    - `-native_spans` [disables](https://pandoc.org/MANUAL.html#extensions) [the raw HTML extension for preserving some native `<span>` HTML elements](https://pandoc.org/MANUAL.html#native_spans). Some `<span>` HTML elements are still preserved as [bracketed spans](https://pandoc.org/MANUAL.html#extension-bracketed_spans) (see the admonition below).

!!! attention
    
    Even when `-native_spans` is used for HTML input, some `<span>` HTML elements are preserved as [bracketed spans](https://pandoc.org/MANUAL.html#extension-bracketed_spans), unless `-bracketed_spans` is used for Markdown output, in which case the `<span>` HTML elements are preserved without being converted to Markdown format.

!!! attention
    
    Using `-link_attributes` to [disable](https://pandoc.org/MANUAL.html#extensions) [the Pandoc Markdown extension for assigning attribute lists to hyperlinks](https://pandoc.org/MANUAL.html#extension-link_attributes) prevents hyperlinks with attributes from being converted to Markdown-style links.

!!! attention
    
    Even when `+fenced_code_blocks` is used for Pandoc Markdown output, [indented code blocks](https://pandoc.org/MANUAL.html#indented-code-blocks) are still produced instead of [fenced code blocks](https://pandoc.org/MANUAL.html#fenced-code-blocks).

### prior work
The method of producing ATX-style headings for all heading levels was introduced to me by [an answer on Stack Overflow by shawnhcorey](https://stackoverflow.com/questions/51015110/pandoc-force-converting-into-markdown-to-use-and-for-h1-and-h2-respective/51023582#51023582).

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

## converting Markdown to plain text {: #Markdowntoplaintext }

!!! note
    
    - {==foo.md==} represents an input text file formatted with [Pandoc Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown).
    - {==bar.txt==} represents an output plain text file.

Use `pandoc -f markdown -t plain --wrap=none "foo.md" | sed -e 's/—/-/g' -e "s/’/'/g" -e 's/\xC2\xA0/ /g' - | cat -s - | sponge "bar.txt"` to convert a [Pandoc Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown)-formatted text file to a [plain text](https://en.wikipedia.org/wiki/Plain_text) file.

### explanation

!!! note
    
    This is an incomplete explanation.

- The `cat -s` [command](https://en.wikipedia.org/wiki/Cat_(Unix)) produces a single blank line in place of multiple adjacent blank lines.[^cnvffmt1]
- The `sed -e 's/—/-/g' -e "s/’/'/g" -e 's/\xC2\xA0/ /g'` [command](https://en.wikipedia.org/wiki/Sed) does the following:
    - `'s/—/-/g'` replaces any [em dashes](https://en.wiktionary.org/wiki/%E2%80%94) (`—`) with [hyphen-minuses](https://en.wiktionary.org/wiki/-) (`-`).
    - `"s/’/'/g"` replaces any [right single quotation marks](https://en.wiktionary.org/wiki/%E2%80%99) (`’`) with [apostrophes](https://en.wiktionary.org/wiki/%27) (`'`).
    - `'s/\xC2\xA0/ /g'` replaces any [non-breaking spaces](https://en.wikipedia.org/wiki/Non-breaking_space) with ordinary spaces, using the `U+C2A0` [UTF-8](https://en.wikipedia.org/wiki/UTF-8) code point.
- The `--wrap=none` [option](https://pandoc.org/MANUAL.html#option--wrap) disables text wrapping.

[^cnvffmt1]: <https://www.gnu.org/software/coreutils/manual/html_node/cat-invocation.html>

## converting PDF to text {: #PDFtotext }

!!! note
    
    - {==foo.pdf==} represents an input PDF file.
    - {==bar.txt==} represents an output text file.

Use `pdftotext -layout -nopgbrk foo.pdf bar.txt` to convert a PDF file to a text file. 

### explanation

- The `-layout` [option](https://www.mankier.com/1/pdftotext) attempts to preserve the layout of the PDF when converting.
- The `-nopgbrk` [option](https://www.mankier.com/1/pdftotext) disables the insertion of [form feed](https://en.wikipedia.org/wiki/Page_break#Form_feed) characters to indicate page breaks.

## converting plain text to [synthesized-speech]-FLAC {: #plaintexttossFLAC }

!!! note
    
    - {==foo.txt==} represents an input plain text file.
    - {==bar.flac==} represents an output FLAC file.

Use `text2wave -otype aiff foo.txt | sox --no-clobber - bar.flac` to convert a plain text file to a [synthesized-speech]-FLAC file.

!!! attention
    
    `text2wave` does not seem to handle [contractions](https://en.wikipedia.org/wiki/Contraction_(grammar)) correctly, reading out each individual character if an apostrophe is encountered in the middle of a word.

### explanation

!!! note
    
    This is an incomplete explanation.

- The `-otype aiff` option produces synthesized speech in [AIFF](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format) format.
- The `--no-clobber` [option](http://sox.sourceforge.net/sox.html) prevents SoX from producing a FLAC output file if a file with the same name already exists.

[synthesized-speech]: https://en.wikipedia.org/wiki/Speech_synthesis

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**
