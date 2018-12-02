# using [rsync]
Use the `--exclude="FOOBAR/FOO.BAR"` option to exclude specific files, where *FOOBAR/FOO.BAR* is the path to the file, relative to the source directory.

Use the `--exclude="/.*"` option to exclude hidden files in the topmost directory.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The method of excluding hidden files in the topmost directory was introduced to me by
[an answer on Ask Ubuntu by Rinzwind](https://askubuntu.com/questions/482916/rsync-exclude-hidden-files-doesnt-work/482920#482920) and 
[an answer on Server Fault by Alexander Pogrebnyak](https://serverfault.com/questions/310189/rsync-how-to-exclude-dotfiles-only-in-topmost-directory/310190#310190).
- The method of excluding specific files was introduced to me by [an answer on Ask Ubuntu by Freedom_Ben](https://askubuntu.com/questions/320458/how-to-exclude-multiple-directories-with-rsync/320459#320459).

[rsync]: https://rsync.samba.org/
