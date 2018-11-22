# installing [Node.js] and [npm] with [nvm]

In Kubuntu, use `curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash` to install [the Node Version Manager](https://github.com/creationix/nvm) and avoid [the use of sudo in the installation of npm packages](https://medium.com/@ExplosionPills/dont-use-sudo-with-npm-still-66e609f5f92). Close and reopen the terminal, then use `command -v nvm` to verify the installation of nvm. Then use `nvm install node` to install the latest version of Node.js and npm.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
The bulk of the installation script was introduced to me by the [Installation](https://github.com/creationix/nvm#installation), [Verify installation](https://github.com/creationix/nvm#verify-installation), and [Usage](https://github.com/creationix/nvm#usage) sections of the [Node Version Manager README on GitHub](https://github.com/creationix/nvm).

[Node.js]: https://en.wikipedia.org/wiki/Node.js
[npm]: https://en.wikipedia.org/wiki/Npm_(software)
[nvm]: https://github.com/creationix/nvm
