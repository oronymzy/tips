# using MkDocs

!!! bug
    If a page begins with an admonition, there must be a newline between the first heading and the admonition, or the text between the first and second heading will not be searchable.

!!! warning
    After being [built](https://www.mkdocs.org/#building-the-site), the site assumes it will come from a server, so when it is opened locally using the [file URI scheme](https://en.wikipedia.org/wiki/File_URI_scheme) there will be problems. Pages will show an "Index of" directory page instead of the actual page, and the search bar will not work.

!!! attention
    If the `repo_url` setting is used in the YAML configuration file, automatically-generated edit buttons can be disabled with `edit_uri: ''`.

### licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

### prior work
- The explanation for MkDoc's difficulty in serving pages opened locally was introduced to me by [a comment on GitHub by waylan](https://github.com/mkdocs/mkdocs/issues/1367#issuecomment-354797280).
- The method of disabling automatically-generated edit buttons was introduced to me by [a page on the MkDocs website](https://www.mkdocs.org/user-guide/configuration/#edit_uri) and [the Getting started page on the Material for MkDocs website](https://squidfunk.github.io/mkdocs-material/getting-started/#adding-a-source-repository).
