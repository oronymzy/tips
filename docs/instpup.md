# installing [pup]
[Install Go](instlGo.md), use `go get -v github.com/ericchiang/pup && cd $HOME/go/src/github.com/ericchiang/pup && go build` to download and install pup, then append `PATH=$PATH:$HOME/go/src/github.com/ericchiang/pup/` to *.bashrc*.

## explanation
- `go get -v github.com/ericchiang/pup` downloads pup.
- `cd $HOME/go/src/github.com/ericchiang/pup && go build` installs pup.
- `PATH=$PATH:$HOME/go/src/github.com/ericchiang/pup/` makes it possible to start pup by typing `pup` into Bash.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The method of installing pup was introduced to me by [the Install section on the pup GitHub](https://github.com/ericchiang/pup#install).
- The method of making it possible to start pup by typing `pup` into Bash was introduced to me by my dad, and reinforced by [an answer on Unix & Linux Stack Exchange by Warren Young](https://unix.stackexchange.com/questions/129143/what-is-the-purpose-of-bashrc-and-how-does-it-work/129144#129144) and [an answer on Unix & Linux Stack Exchange by Gilles](https://unix.stackexchange.com/questions/26047/how-to-correctly-add-a-path-to-path/26059#26059).

[pup]: https://github.com/ericchiang/pup
