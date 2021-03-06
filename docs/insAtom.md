# installing [Atom text editor]

!!! attention
    
    Atom text editor can only be installed on 64-bit Linux systems.[^insAtom1]

Use `curl -L -o /tmp/atom-amd64.deb https://atom.io/download/deb && sudo dpkg -i --force-depends /tmp/atom-amd64.deb`. If any dependencies did not install, also use `sudo apt -f install`.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The method of getting cURL to follow a redirect was introduced to me by [an answer on Stack Overflow](https://stackoverflow.com/questions/3074288/get-url-after-curl-is-redirected/3077316#3077316).
- The method of using apt to install dependencies was introduced to me by [an answer on Ask Ubuntu by Arindom](https://askubuntu.com/questions/40011/how-to-let-dpkg-i-install-dependencies-for-me/40050#40050).

[Atom text editor]: https://atom.io/
[^insAtom1]: <https://github.com/atom/atom#linux>
