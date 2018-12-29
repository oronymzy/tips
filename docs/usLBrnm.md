# using [Lloyd Brookes's renamer]
Use `renamer -d -f foo.bar -r bar.foo *` to simulate the renaming of a file named *foo.bar* to a file named *bar.foo*. If the results are satisfactory, use `renamer -f foo.bar -r bar.foo *` to actually perform the renaming.

## explanation
- The `-d` option specifies that a **dry run** wiil be performed.
- The `-f` option specifies the string or regular expression literal to **find** for renaming.
- The `-r` option specifies the string that will **replace** the existing name.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The explanation of the renamer options was introduced to me by [the Renamer CLI docs page on the renamer wiki on GitHub](https://github.com/75lb/renamer/wiki/Renamer-CLI-docs).
- The importance of including the `-d` option to perform a dry run was introduced to me by [the Disclaimer section of the renamer README on GitHub](https://github.com/75lb/renamer#disclaimer).
- The method of renaming files was introduced to me by [the Synopsis section of the renamer README on GitHub](https://github.com/75lb/renamer#synopsis).

[Lloyd Brookes's renamer]: https://github.com/75lb/renamer
