# installing beets
## CentOS

!!! note
    These are incomplete instructions.

[Install pip](instpip.md), then use `sudo -H pip install beets`.

## Kubuntu
[Install pip](instpip.md), use `sudo -H pip install beets`, then use `beet config -p` to find the `config.yaml` YAML-formatted text configuration file for beets (or create it if it doesn't exist) and customize it with:

```
directory: /foo/bar/baz
library: /foo/bar/baz/musiclibrary.db
import:
  move: yes
plugins: edit play
paths:
  ^filename::^$: $filename
  ^disc:00: $albumartist - $album - $disc - $track - $title
  album::^$: $artist - $title
  default: $albumartist - $album - $track - $title
```

where */foo/bar/baz* is the path to where the music is stored.

!!! bug
    The `singleton` field does not seem to function correctly when used to set the file name for imported files. A workaround is to use `album::^$: $artist - $title` instead.

Use `beet import /foo/bar` to add some music, where */foo/bar* is the path to the music to be imported, then ensure that the plugins work. The [Edit](http://beets.readthedocs.io/en/v1.4.5/plugins/edit.html) plugin requires [changing the environment variable](chgevtb.md) `$EDITOR` to gedit and not Kate with `export EDITOR="/usr/bin/gedit"`.

??? info "Personal experience"
    Tested in Kubuntu 16.10 and 17.10.

## Termux
Use `pip install beets` to install beets, then use `beet config -p` to find the `config.yaml` YAML-formatted text configuration file for beets and customize it with:

```
directory: /foo/bar/baz
library: /foo/bar/baz/musiclibrary.db
plugins: edit play
```

where */foo/bar/baz* is the path to where the music is stored.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The bulk of the installation script was introduced to me by [the Getting Started page on beets documentation](https://beets.readthedocs.io/en/v1.4.5/guides/main.html#installing).
- The method of finding the text file where beets configuration is stored was introduced to me by [the Getting Started page on beets documentation](http://beets.readthedocs.io/en/v1.4.5/guides/main.html#configuring).
- The method of importing music without autotagging it was introduced to me by [the Getting Started page on beets documentation](http://beets.readthedocs.io/en/v1.4.5/guides/main.html#importing-your-library).
- The possibility of customizing the path format configuration was introduced to me by [the Configuration page on beets documentation](http://beets.readthedocs.io/en/v1.4.5/reference/config.html#path-format-configuration).
- The workaround for a non-functioning `singleton` field was introduced to me by [the Queries page on beets documentation](http://beets.readthedocs.io/en/v1.4.5/reference/query.html#regular-expressions).
