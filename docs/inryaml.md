# installing [ruamel.yaml]
## installing [ruamel.yaml] in [Linux]
Use `sudo -H pip install -U pip setuptools wheel && sudo -H pip install ruamel.yaml ruamel.yaml.cmd`.

## installing [ruamel.yaml] in [Termux]
Use `apt install clang python-dev && pip install ruamel.yaml`.

## prior work
- The bulk of the Linux installation script was introduced to me by [the “Installing” page of the Python YAML package documentation site](https://yaml.readthedocs.io/en/latest/install.html).
- The necessity of installing `clang` and `python-dev` with the [APT package manager](https://en.wikipedia.org/wiki/APT_(Package_Manager)) was introduced to me by [a comment on GitHub by kutsan](https://github.com/neovim/pynvim/issues/267).

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[Linux]: https://en.wikipedia.org/wiki/Linux
[Termux]: https://termux.com/
[ruamel.yaml]: https://pypi.org/project/ruamel.yaml/
