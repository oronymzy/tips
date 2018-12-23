# using [MkDocs]

!!! warning
    
    After being [built](https://www.mkdocs.org/#building-the-site), the site assumes it will come from a server, so when it is opened locally using the [file URI scheme](https://en.wikipedia.org/wiki/File_URI_scheme) there will be problems. Pages will show an "Index of" directory page instead of the actual page, and the search bar will not work.

!!! note
    
    By design, MkDocs does not provide the option of excluding any of the files in `docs_dir` when building `site_dir`.[^usgMkDc1] [^usgMkDc2]

!!! note
    
    By design, a parent nav item in `mkdocs.yml` cannot have a page listed after it.[^usgMkDc3]

!!! note
    
    If the `repo_url` setting is used in the YAML configuration file, automatically-generated edit buttons can be disabled with `edit_uri: ''`.

## [Material for MkDocs]

!!! attention
    
    Material for MkDocs expects only one level 1 heading per page. If more than one is included, the table of contents will not display correctly.

!!! attention
    
    By default, table headers display with a dark gray that can make it difficult to see the dark blue of visited links. A workaround is to introduce an [additional stylesheet](https://squidfunk.github.io/mkdocs-material/customization/#additional-stylesheets) and add the following to it: `.md-typeset table:not([class]) th {background-color: rgba(0, 0, 0, 0.1); color: black;}`. This will make the table headers a lighter gray and the text black.

### [admonition extension]

!!! bug
    
    If a page begins with an admonition, there must be a newline between the first heading and the admonition, or the text between the first and second heading will not be searchable.

!!! bug
    
    If an admonition contains a table, the table may not render correctly.

!!! attention
    
    Reference-style links do not work within admonitions.

!!! attention
    
    Markdown is rendered within HTML when inside admonitions.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The explanation for MkDoc's difficulty in serving pages opened locally was introduced to me by [a comment on GitHub by waylan](https://github.com/mkdocs/mkdocs/issues/1367#issuecomment-354797280).
- The explanation for MkDoc's inability to render within HTML block-level elements was introduced to me by [a comment on GitHub by facelessuser](https://github.com/squidfunk/mkdocs-material/issues/757).
- The explanation for not producing a correct table of contents when a level 1 heading is used was introduced to me by [a comment on GitHub by squidfunk](https://github.com/squidfunk/mkdocs-material/issues/818#issuecomment-404156956).
- The method of disabling automatically-generated edit buttons was introduced to me by [a page on the MkDocs website](https://www.mkdocs.org/user-guide/configuration/#edit_uri) and [the Getting started page on the Material for MkDocs website](https://squidfunk.github.io/mkdocs-material/getting-started/#adding-a-source-repository).
- The possibility of using an additional stylesheet to change the appearance of MkDocs was introduced to me by [a comment on GitHub by squidfunk](https://github.com/squidfunk/mkdocs-material/issues/466#issuecomment-330044473).

[admonition extension]: https://squidfunk.github.io/mkdocs-material/extensions/admonition/
[Material for MkDocs]: https://squidfunk.github.io/mkdocs-material/
[MkDocs]: https://www.mkdocs.org/
[^usgMkDc1]: https://github.com/mkdocs/mkdocs/issues/1152
[^usgMkDc2]: https://github.com/mkdocs/mkdocs/issues/1500
[^usgMkDc3]: https://github.com/mkdocs/mkdocs/issues/1139#issuecomment-281483739
