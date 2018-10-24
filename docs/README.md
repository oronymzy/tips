# Oronymzy's tips

Hope you find them useful.

!!! note
    [MkDocs](https://www.mkdocs.org/) pages are designed to be generated from [Python-Markdown](https://python-markdown.github.io/)-formatted text files[^Orotips1], but I tend to use [Pandoc Markdown](http://pandoc.org/MANUAL.html#pandocs-markdown), and I'm also using [PyMdown Extensions](https://facelessuser.github.io/pymdown-extensions/), so it's a bit of a mess.

## prior work
The following additions to `mkdocs.yml`:

```
markdown_extensions:
  - admonition
  - footnotes
  - pymdownx.details
  - pymdownx.keys
```

were introduced to me by the [Admonition](https://squidfunk.github.io/mkdocs-material/extensions/admonition/#installation), [Footnotes](https://squidfunk.github.io/mkdocs-material/extensions/footnotes/#installation), [Keys](https://facelessuser.github.io/pymdown-extensions/extensions/keys/), and [PyMdown Extensions](https://squidfunk.github.io/mkdocs-material/extensions/pymdown/#installation).

[^Orotips1]: https://www.mkdocs.org/user-guide/writing-your-docs/#writing-with-markdown
