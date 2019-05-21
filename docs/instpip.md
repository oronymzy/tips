# installing [pip]
## installing [pip] in [Linux]
Use `curl -L https://bootstrap.pypa.io/get-pip.py -o /tmp/get-pip.py && sudo -H python /tmp/get-pip.py`.

??? info "Personal experience"
    
    Works on Slim running CentOS 7, Slim running Kubuntu 18.04, Slinky running Kubuntu 18.04, Snarky running Kubuntu 17.10, and Tabby running Kubuntu 18.04.

To update an existing Ubuntu installation of pip to use Python3 instead of Python2, use `sudo apt install python3-pip -y && sudo -H pip3 install --ignore-installed pip && sudo apt autoremove python3-pip -y`.

[Linux]: https://en.wikipedia.org/wiki/Linux

## installing [pip] in [Termux]
Use `cd ~ && curl -L https://bootstrap.pypa.io/get-pip.py -o ./get-pip.py && python get-pip.py`.

[Termux]: https://termux.com/

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The `-H` option for sudo was introduced to me by [a comment on MkDocs by k4kfh](https://github.com/mkdocs/mkdocs/issues/195#issuecomment-158222944).
- The idea of using an installer from the pip website was introduced to me by [a comment on MkDocs by abethman](https://github.com/mkdocs/mkdocs/issues/195#issuecomment-102446415).

[pip]: https://pip.pypa.io/en/stable/
