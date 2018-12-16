# indicating [page breaks] in Markdown
## HTML and CSS
Markdown does not have a page break element, but with HTML and CSS a page break can be indicated with the [`page-break-before`](https://developer.mozilla.org/en-US/docs/Web/CSS/page-break-before) or [`page-break-after`](https://developer.mozilla.org/en-US/docs/Web/CSS/page-break-after) CSS properties. These will only work if applied to block-generating block-level elements, so the following example *might* work:

`<div style="page-break-after: always;"></div>`

but a better way is to include existing HTML content within the `div` element, for example:

```
<div style="page-break-after: always;">
<p>Hello world!</p>
</div>
```

!!! note
    
    HTML does not normally display page breaks, **except when printing**.

## pandoc filters and LaTeX

!!! attention
    
    LaTeX is not natively supported by Markdown, so this method is unlikely to render properly outside pandoc.

The [LaTeX](https://www.latex-project.org/) [command](https://en.wikibooks.org/wiki/LaTeX/Command_Glossary) `\newpage` can be used to indicate a page break in combination with [pandoc](http://pandoc.org/) and a [Lua](http://pandoc.org/lua-filters.html) [filter](https://pandoc.org/filters.html). To use pandoc to convert Markdown to DOCX, save the following code to `pagebreak.lua`:

??? note "pagebreak.lua code"
    
    ```
    --[[
    pagebreak – convert raw LaTeX page breaks to other formats
    
    Copyright © 2017-2018 Benct Philip Jonsson, Albert Krewinkel
    
    Permission to use, copy, modify, and/or distribute this software for any
    purpose with or without fee is hereby granted, provided that the above
    copyright notice and this permission notice appear in all copies.
    
    THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES
    WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF
    MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR
    ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES
    WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN
    ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF
    OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.
    ]]
    local stringify_orig = (require 'pandoc.utils').stringify
    
    local function stringify(x)
      return type(x) == 'string' and x or stringify_orig(x)
    end
    
    --- configs – these are populated in the Meta filter.
    local pagebreak = {
      epub = '<p style="page-break-after: always;"> </p>',
      html = '<div style="page-break-after: always;"></div>',
      latex = '\\newpage{}',
      ooxml = '<w:p><w:r><w:br w:type="page"/></w:r></w:p>',
    }
    
    local function pagebreaks_from_config (meta)
      local html_class =
        (meta.newpage_html_class and stringify(meta.newpage_html_class))
        or os.getenv 'PANDOC_NEWPAGE_HTML_CLASS'
      if html_class and html_class ~= '' then
        pagebreak.html = string.format('<div class="%s"></div>', html_class)
      end
    
      local odt_style =
        (meta.newpage_odt_style and stringify(meta.newpage_odt_style))
        or os.getenv 'PANDOC_NEWPAGE_ODT_STYLE'
      if odt_style and odt_style ~= '' then
        pagebreak.odt = string.format('<text:p text:style-name="%s"/>', odt_style)
      end
    end
    
    --- Return a block element causing a page break in the given format.
    local function newpage(format)
      if format == 'docx' then
        return pandoc.RawBlock('openxml', pagebreak.ooxml)
      elseif format:match 'latex' then
        return pandoc.RawBlock('tex', pagebreak.latex)
      elseif format:match 'html.*' then
        return pandoc.RawBlock('html', pagebreak.html)
      elseif format:match 'epub' then
        return pandoc.RawBlock('html', pagebreak.epub)
      else
        -- fall back to insert a form feed character
        return pandoc.Para{pandoc.Str '\f'}
      end
    end
    
    local function is_newpage_command(command)
      return command:match '^\\newpage%{?%}?$'
        or command:match '^\\pagebreak%{?%}?$'
    end
    
    -- Filter function called on each RawBlock element.
    function RawBlock (el)
      -- Don't do anything if the output is TeX
      if FORMAT:match 'tex$' then
        return nil
      end
      -- check that the block is TeX or LaTeX and contains only
      -- \newpage or \pagebreak.
      if el.format:match 'tex' and is_newpage_command(el.text) then
        -- use format-specific pagebreak marker. FORMAT is set by pandoc to
        -- the targeted output format.
        return newpage(FORMAT)
      end
      -- otherwise, leave the block unchanged
      return nil
    end
    
    -- Turning paragraphs which contain nothing but a form feed
    -- characters into line breaks.
    function Para (el)
      if #el.content == 1 and el.content[1].text == '\f' then
        return newpage(FORMAT)
      end
    end
    
    return {
      {Meta = pagebreaks_from_config},
      {RawBlock = RawBlock, Para = Para}
    }
    ```

Then use `pandoc -f markdown -t docx foo.md --lua-filter=pagebreak.lua -o bar.docx`, where *foo.md* is the Markdown-formatted input file and *bar.docx* is the output file.

## licensing
**Some rights reserved: MIT License.** Includes significant content from [pagebreak.lua on GitHub](https://github.com/pandoc/lua-filters/blob/master/pagebreak/pagebreak.lua).

??? note "[MIT License](https://choosealicense.com/licenses/mit/) for pagebreak.lua[^ipbkMkd1]"
    
    MIT License
    
    Copyright (c) 2017-2018 pandoc
    
    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:
    
    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.
    
    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.

## prior work
- The method of using a pandoc filter to enable conversion of page breaks in Markdown was introduced to me by [an answer on Stack Overflow by tarleb](https://stackoverflow.com/questions/16965490/pandoc-markdown-page-break/52131435#52131435).
- The possibility of using HTML and CSS to introduce a page break was introduced to me by [an answer on Stack Overflow by tomodian](https://stackoverflow.com/questions/22601053/pagebreak-in-markdown-while-creating-pdf/29642392#29642392).
- The requirements for the `page-break-before` and `page-break-after` CSS properties to work properly were introduced to me by [the comments on an answer on Stack Overflow](https://stackoverflow.com/questions/1664049/can-i-force-a-page-break-in-html-printing/1664058#1664058).

[page breaks]: https://en.wikipedia.org/wiki/Page_break
[^ipbkMkd1]: https://github.com/pandoc/lua-filters/blob/master/LICENSE
