# using [MkDocs]
MkDocs converts Markdown to HTML using [Python-Markdown](https://python-markdown.github.io/extensions/).[^usgMkDc1]

MkDocs uses [lunr.js](https://lunrjs.com/) as its search engine[^usgMkDc2], but different themes may have different search plugins.

!!! warning
    
    After being [built](https://www.mkdocs.org/#building-the-site), the site assumes it will come from a server, so when it is opened locally using the [file URI scheme](https://en.wikipedia.org/wiki/File_URI_scheme) there will be problems. Pages will show an "Index of" directory page instead of the actual page, and the search bar will not work.

!!! note
    
    By design, MkDocs does not provide the option of excluding any of the files in `docs_dir` when building `site_dir`.[^usgMkDc3] [^usgMkDc4]

## `mkdocs.yml` configuration file
The MkDocs configuration file is formatted with [YAML](https://yaml.org/).

MkDocs supports a number of [Python-Markdown](https://python-markdown.github.io/extensions/)[^usgMkDc1] and [PyMdown](https://facelessuser.github.io/PyMdown/) extensions, with documentation available from [facelessuser](https://facelessuser.github.io/pymdown-extensions/) and [squidfunk](https://squidfunk.github.io/mkdocs-material/extensions/pymdown/). They are enabled and customized through the `mkdocs.yml` configuration file.

!!! note
    
    By design, a parent nav item in `mkdocs.yml` cannot have a page listed after it.[^usgMkDc5]

!!! note
    
    If the `repo_url` setting is used in the YAML configuration file, automatically-generated edit buttons can be disabled with `edit_uri: ''`.

Here is part of the `mkdocs.yml` configuration used for this site:

```
markdown_extensions:
  - admonition
  - attr_list
  - codehilite:
      guess_lang: false
  - def_list
  - footnotes
  - meta
  - pymdownx.caret
  - pymdownx.critic
  - pymdownx.details
  - pymdownx.extrarawhtml
  - pymdownx.keys
  - pymdownx.snippets
  - pymdownx.superfences
  - pymdownx.tasklist:
      custom_checkbox: true
  - pymdownx.tilde
theme:
  name: 'material'
extra_css:
  - 'extra.css'
extra:
  social:
    - type: 'github'
      link: 'https://github.com/oronymzy'
repo_name: 'oronymzy/tips'
repo_url: 'https://github.com/oronymzy/tips'
edit_uri: ''
```

### explanation

- The `markdown_extensions` setting [specifies](https://www.mkdocs.org/user-guide/configuration/#markdown_extensions) the [Python-Markdown extensions](https://python-markdown.github.io/extensions/) for MkDocs.
    - The `admonition` entry point enables the [Python-Markdown admonitions](https://python-markdown.github.io/extensions/admonition/) extension.  
    Additional documentation is available for [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/extensions/admonition/).
    - The `attr_list` entry point enables the [Python-Markdown attribute lists](https://python-markdown.github.io/extensions/attr_list/) extension, which adds support for [HTML-style attributes](https://en.wikipedia.org/wiki/HTML_attribute) using curly brackets (`{}`) and a [CSS-like syntax](https://en.wikipedia.org/wiki/Cascading_Style_Sheets#Syntax).
    - The `codehilite` entry point enables the [Python-Markdown](https://python-markdown.github.io/extensions/code_hilite/) [syntax highlighting](https://en.wikipedia.org/wiki/Syntax_highlighting) extension.  
    Additional documentation is available for [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/extensions/codehilite/).
        - `guess_lang: false` disables automatic language detection and ensures that blocks are highlighted only when the language is specified.
    - The `def_list` entry point enables the [Python-Markdown definition lists](https://python-markdown.github.io/extensions/definition_lists/) (or *description lists*) extension.
    - The `footnotes` entry point enables the [Python-Markdown footnotes](https://python-markdown.github.io/extensions/footnotes/) extension.  
    Additional documentation is available for [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/extensions/footnotes/).
    - The `meta` entry point enables the [Python-Markdown metadata (or meta-data)](https://python-markdown.github.io/extensions/meta_data/) extension, which enables [metadata](https://en.wikipedia.org/wiki/Metadata) blocks with [key-value pairs (or attribute-value pairs)](https://en.wikipedia.org/wiki/Attribute%E2%80%93value_pair) as the contents.  
    Additional documentation is available for [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/extensions/metadata/).
    - The `pymdownx.caret` entry point enables the [PyMdown Caret](https://facelessuser.github.io/pymdown-extensions/extensions/caret/) extension, which allows the *ins* and *sup* HTML elements to be added using a caret (`^`).
    - The `pymdownx.critic` entry point enables the [PyMdown Critic](https://facelessuser.github.io/pymdown-extensions/extensions/critic/) extension, which adds support for the [CriticMarkdown](http://criticmarkup.com/) syntax.
    - The `pymdownx.details` entry point enables the [PyMdown Details](https://facelessuser.github.io/pymdown-extensions/extensions/details/) extension, which adds support for collapsible admonition-style elements using the *details* and *summary* HTML elements.
    - The `pymdownx.extrarawhtml` entry point enables the [PyMdown ExtraRawHTML](https://facelessuser.github.io/pymdown-extensions/extensions/extrarawhtml/) extension, which allows parsing of Markdown within any HTML element as long as the `markdown="1"` attribute is added to its opening tag. It is taken from [Python-Markdown Extra](https://python-markdown.github.io/extensions/extra/#nested-markdown-inside-html-blocks), and is also available through the [PyMdown Extra](https://facelessuser.github.io/pymdown-extensions/extensions/extra/) and [Python-Markdown Extra](https://python-markdown.github.io/extensions/extra/) extension compilations.
    - The `pymdownx.keys` entry point enables the [PyMdown Keys](https://facelessuser.github.io/pymdown-extensions/extensions/keys/) extension, which allows the *kbd* HTML element using two plus signs (`++`).
    - The `pymdownx.snippets` entry point enables the [PyMdown Snippets](https://facelessuser.github.io/pymdown-extensions/extensions/snippets/) extension, which allows one Markdown or HTML file into another Markdown file using ASCII scissors (`--8<--`).
    - The `pymdownx.superfences` entry point enables the [PyMdown SuperFences](https://facelessuser.github.io/pymdown-extensions/extensions/superfences/) extension, which expands the functionality of fenced code blocks.
    - The `pymdownx.tasklist` entry point enables the [PyMdown Tasklist](https://facelessuser.github.io/pymdown-extensions/extensions/tasklist/) extension, which allows the inclusion of checkboxes to create a (usually non-interactive) task list out of an HTML unordered list.
        - `custom_checkbox: true` enables CSS styling of checkboxes.
    - The `pymdownx.tilde` entry point enables the [PyMdown Tilde](https://facelessuser.github.io/pymdown-extensions/extensions/tilde/) extension, which allows the *del* and *sub* HTML elements to be added using a tilde (`~`).
- The following:
```
theme:
  name: 'material'
```
[specifies](https://www.mkdocs.org/user-guide/configuration/#theme) [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) as the MkDocs theme.
- The following:
```
extra_css:
  - 'extra.css'
```
[sets an additional CSS file to be included with the theme](https://www.mkdocs.org/user-guide/configuration/#extra_css).  
Additional documentation is available for [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/customization/#additional-stylesheets).
- The following:
```
extra:
  social:
    - type: 'github'
      link: 'https://github.com/oronymzy'
```
is a custom [`extra` setting](https://www.mkdocs.org/user-guide/configuration/#extra) for the [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) theme that [adds a social link](https://squidfunk.github.io/mkdocs-material/getting-started/#adding-social-links) to GitHub.
- The following:
```
repo_name: 'oronymzy/tips'
repo_url: 'https://github.com/oronymzy/tips'
edit_uri: ''
```
[adds a GitHub source repository](https://www.mkdocs.org/user-guide/configuration/#repo_url) and disables automatically-generated edit buttons.  
Additional documentation is available for [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/getting-started/#adding-a-source-repository).

## [Material for MkDocs] theme

!!! attention
    
    Material for MkDocs expects only one level 1 heading per page. If more than one is included, the table of contents will not display correctly.

!!! attention
    
    By default, table headers display with a dark gray that can make it difficult to see the dark blue of visited links. A workaround is to introduce an [additional stylesheet](https://squidfunk.github.io/mkdocs-material/customization/#additional-stylesheets) and add the following to it: `.md-typeset table:not([class]) th {background-color: rgba(0, 0, 0, 0.1); color: black;}`. This will make the table headers a lighter gray and the text black.

!!! attention
    
    The [Material for MkDocs implementation of lunr.js](https://squidfunk.github.io/mkdocs-material/getting-started/#site-search) may behave differently than the default MkDocs implementation of lunr.js.[^usgMkDc6]

!!! attention
    
    Material for MkDocs [uses an older version of Font Awesome that does not include some currently-available icons](https://github.com/squidfunk/mkdocs-material/issues/756). For example, the [social link](https://squidfunk.github.io/mkdocs-material/getting-started/#adding-social-links) for Mastodon `mastodon` does not render, [even though there is a Font Awesome icon for it](https://fontawesome.com/icons/mastodon?style=brands). A workaround is to replace it with something more generic, such as the [*user* icon](https://fontawesome.com/icons/user?style=solid).

## [admonition extension]

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
[^usgMkDc1]: https://www.mkdocs.org/user-guide/configuration/#markdown_extensions
[^usgMkDc2]: https://www.mkdocs.org/user-guide/configuration/#search
[^usgMkDc3]: https://github.com/mkdocs/mkdocs/issues/1152
[^usgMkDc4]: https://github.com/mkdocs/mkdocs/issues/1500
[^usgMkDc5]: https://github.com/mkdocs/mkdocs/issues/1139#issuecomment-281483739
[^usgMkDc6]: https://github.com/mkdocs/mkdocs/issues/1704#event-2031239880
