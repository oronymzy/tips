# installing [Beaker Browser]
## [Ubuntu-based] systems
Download the latest [AppImage file](https://en.wikipedia.org/wiki/AppImage) [from GitHub](https://github.com/beakerbrowser/beaker/releases/latest). Make the file executable with `chmod +x foo.bar`, where *foo.bar* is the downloaded AppImage file or, alternatively, make the file executable in Kubuntu with ++"Context Menu > Properties > Permissions > Is executable"++. To run the program, use `./foo.bar`, where *foo.bar* is the downloaded AppImage file.

??? info "Personal experience"
    
    [Beaker 0.8.0](https://github.com/beakerbrowser/beaker/releases/tag/0.8.0) does not work on Kubuntu 17.10, but the following releases do work:
    
    - [Beaker 0.8.0-prerelease.9](https://github.com/beakerbrowser/beaker/releases/tag/0.8.0-prerelease.9)
    - [Beaker 0.8.0-prerelease.8](https://github.com/beakerbrowser/beaker/releases/tag/0.8.0-prerelease.8)
    - [Beaker 0.8.0-prerelease.7](https://github.com/beakerbrowser/beaker/releases/tag/0.8.0-prerelease.7)
    - [Beaker 0.8.0-prerelease.6](https://github.com/beakerbrowser/beaker/releases/tag/0.8.0-prerelease.6)

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
The method of making a file executable using `chmod` was introduced to me by [an answer on Stack Overflow by fge](https://stackoverflow.com/questions/8779951/how-do-i-run-a-shell-script-without-using-sh-or-bash-commands/8779980#8779980).

[Beaker Browser]: https://beakerbrowser.com/
[Ubuntu-based]: https://en.wikipedia.org/wiki/List_of_Linux_distributions#Ubuntu-based
