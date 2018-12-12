# installing [jq]
## [Ubuntu-based] systems
jq can be installed from the official repositories using `sudo apt install jq`[^instljq1], but it may not be the latest version. For jq 1.6, download [the 64-bit Linux executable file from GitHub](https://github.com/stedolan/jq/releases/download/jq-1.6/jq-linux64) and [make it executable](mkfexec.md).

!!! attention
    
    On Kubuntu 18.04, [building from source](http://stedolan.github.io/jq/download/#from_source_on_linux_os_x_cygwin_and_other_posixlike_operating_systems) did not work jq 1.6 or the latest development version as of 2018-12-11. If it had worked, the following dependencies would have been required: `sudo apt install autoconf libtool make`. I got similar errors to those reported on [an apparently resolved bug](https://github.com/stedolan/jq/issues/1659).

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The method of resolving an error by installing `libtool` was introduced to me by [an answer on Stack Overflow by Eli](https://stackoverflow.com/questions/18978252/error-libtool-library-used-but-libtool-is-undefined/36401675#36401675).

[jq]: https://stedolan.github.io/jq/
[jq 1.6]: https://github.com/stedolan/jq/releases/tag/jq-1.6
[Ubuntu-based]: https://en.wikipedia.org/wiki/List_of_Linux_distributions#Ubuntu-based
[^instljq1]: http://stedolan.github.io/jq/download/#linux
