# installing [youtube-dl]
## Linux
Use `sudo curl -L https://yt-dl.org/downloads/latest/youtube-dl -o /usr/local/bin/youtube-dl && sudo chmod a+rx /usr/local/bin/youtube-dl`.

## Termux
Use`termux-setup-storage && pkg install curl && pkg install python2 && pkg install python && pkg install ffmpeg` to install the requirements, then use `curl -L https://yt-dl.org/downloads/latest/youtube-dl -o /data/data/com.termux/files/usr/bin/youtube-dl && chmod a+rx /data/data/com.termux/files/usr/bin/youtube-dl && which youtube-dl` to install youtube-dl.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The bulk of the Linux installation script was introduced to me by [the youtube-dl Download Page](https://rg3.github.io/youtube-dl/download.html).
- The requirements for Termux and the bulk of the Termux installation script were introduced to me by [an article on ITrendbuzz by Santhosh Veer](https://itrendbuzz.com/install-youtube-dl-on-termux/).

[youtube-dl]: https://rg3.github.io/youtube-dl/
