# Oronymzy's tips

Hope you find them useful.

!!! info
    This site came about from my habit of [information grazing](https://en.wikipedia.org/wiki/Information_grazing), and serves as a way of documenting information I tend to quickly forget.

## disclosure of bias
My operating system of choice is [Kubuntu](https://kubuntu.org/) for desktop and notebook computers and [Android](https://en.wikipedia.org/wiki/Android_(operating_system)) for mobile devices. These operating systems are both (arguably) [Linux distributions](https://en.wikipedia.org/wiki/Linux_distribution), and are therefore [Unix-like](https://en.wikipedia.org/wiki/Unix-like). Consequently, much material relies on the [Unix shell](https://en.wikipedia.org/wiki/Unix_shell), though some material will use a graphical user interface. Proprietary operating systems like Windows and Mac will appear only occasionally. There is also an almost exclusive use of permissively-licensed software, even to the point of sacrificing functionality. The rationale for this is sustainability, as proprietary tools often become obsolete or inaccessible with no recourse for the user.

## license
All content is licensed [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) **unless otherwise noted**, and will always be more permissive than all rights reserved. The *Licensing* heading denotes the license for each page.

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

!!! note
    [MkDocs](https://www.mkdocs.org/) pages are designed to be generated from [Python-Markdown](https://python-markdown.github.io/)-formatted text files[^Orotips1], but I tend to use [Pandoc Markdown](http://pandoc.org/MANUAL.html#pandocs-markdown), and I'm also using [PyMdown Extensions](https://facelessuser.github.io/pymdown-extensions/), so it's a bit of a mess.

[^Orotips1]: https://www.mkdocs.org/user-guide/writing-your-docs/#writing-with-markdown
