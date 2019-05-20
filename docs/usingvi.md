# using [vi]

## entering four consecutive space characters with the tab key

Add `set tabstop=8 softtabstop=0 expandtab shiftwidth=4 smarttab` to `$HOME/.exrc`.

!!! info "Explanation (incomplete)"
    
    - `tabstop` is the width of a hard tabstop measured in "spaces". It is effectively the (maximum) width of an actual tab character.
    - `softtabstop`. Setting this to a non-zero value other than `tabstop` will make the tab key (in insert mode) insert a combination of spaces (and possibly tabs) to *simulate* tab stops at this width.
    - `expandtab`. Enabling this will make the tab key (in insert mode) insert spaces instead of tab characters. This also affects the behavior of the `retab` command.
    - `shiftwidth`. The size of an "indent". It's also measured in spaces, so if your code base indents with tab characters then you want `shiftwidth` to equal the number of tab characters times `tabstop`. This is also used by things like the `=`, `>` and `<` commands.
    - `smarttab`. Enabling this will make the tab key (in insert mode) insert spaces or tabs to go to the next indent of the next tabstop when the cursor is at the beginning of a line (i.e. the only preceding characters are whitespace).
    - `.exrc` is the startup file for vi.[^usingvi1]

## licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Includes significant content from [an answer on Stack Overflow by Laurence Gonsalves](https://stackoverflow.com/questions/1878974/redefine-tab-as-4-spaces/1878983#1878983), with changes made.

[vi]: https://en.wikipedia.org/wiki/Vi
[^usingvi1]: <http://ex-vi.sourceforge.net/vi.html#4>
