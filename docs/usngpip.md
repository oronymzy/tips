# using [pip]

Use `pip list` to list installed packages.

Use `pip list --outdated --format=freeze` to list outdated installed packages using the *freeze* list format.

## explanation

- The `--outdated` [option](https://pip.pypa.io/en/stable/reference/pip_list/#cmdoption-o) lists outdated packages.
- The `--format=freeze` [option](https://pip.pypa.io/en/stable/reference/pip_list/#cmdoption-format) produces output that can be used with a [requirements file](https://pip.pypa.io/en/stable/user_guide/#requirements-files).[^usngpip1]

Use `sudo -H pip install --upgrade pip` to upgrade pip to the newest version.

Use `sudo -H pip install --upgrade foobar` to upgrade an installed package to the newest version, where *foobar* is the name of the package to be upgraded.

## explanation
The `--upgrade` [option](https://pip.pypa.io/en/stable/reference/pip_install/#cmdoption-u) upgrades the package to the newest version.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The meaning of the word “freeze” in the contect of the `--format=freeze` option was introduced to me by [an answer on Stack Overflow by Serjik](https://stackoverflow.com/questions/18966564/pip-freeze-vs-pip-list/33207042#33207042) and [an answer on Stack Overflow by Daniel Lahyani](https://stackoverflow.com/questions/18966564/pip-freeze-vs-pip-list/49251593#49251593).
- The method of upgrading an installed package was introduced to me by [an answer on Stack Overflow by rbp](https://stackoverflow.com/questions/2720014/upgrading-all-packages-with-pip/3452888#3452888).

[pip]: https://pip.pypa.io/en/stable/
[^usngpip1]: http://staticbackup.readthedocs.com/pip/rtd-builds/latest/usage.html#id11
