# installing pip
In Kubuntu, use `wget -P /tmp https://bootstrap.pypa.io/get-pip.py && sudo -H python /tmp/get-pip.py` to install [pip](https://pip.pypa.io/en/stable/).

??? info "Personal experience"
    - Works on Slinky running Kubuntu 18.04 and Snarky running Kubuntu 17.10.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The `-H` option for sudo was introduced to me by [a comment on MkDocs by k4kfh](https://github.com/mkdocs/mkdocs/issues/195#issuecomment-158222944).
- The idea of using an installer from the pip website was introduced to me by [a comment on MkDocs by abethman](https://github.com/mkdocs/mkdocs/issues/195#issuecomment-102446415).
