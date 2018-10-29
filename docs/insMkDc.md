# installing MkDocs
In Kubuntu, [install pip](instpip.md), then use `sudo -H pip install mkdocs mkdocs-material` to install [MkDocs](https://www.mkdocs.org/) and [Material for MkDocs](https://github.com/squidfunk/mkdocs-material).

??? info "Personal experience"
    - Works on Snarky running Kubuntu 17.10.
    - Somewhat works on Slim running CentOS 7, with pages rendering incorrectly. Does not work with mkdocs-material.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The `-H` option for sudo was introduced to me by [a comment on MkDocs by k4kfh](https://github.com/mkdocs/mkdocs/issues/195#issuecomment-158222944).
