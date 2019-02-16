# installing a [Linux] system
## [Ubuntu-based] systems

To install updates, use `sudo apt update && sudo apt full-upgrade && sudo apt autoremove`.

To install officially supported programs, use `sudo apt install audacity bless cheese codeblocks curl easytag elinks exfat-fuse exfat-utils exiftool extundelete eyed3 festival filelight filezilla flac focuswriter fortune gedit gimp git-cola gnome-disk-utility gnome-terminal gnumeric gparted graphviz grsync idle imagemagick inkscape jekyll jq krename lftp lolcat lynx mediainfo meld moreutils ncdu net-tools pmount qtqr recode retext searchmonkey simplescreenrecorder sox surf testdisk texlive-fonts-recommended transmission-qt trash-cli tree unoconv unrar unrtf vlc vnstat zbar-tools -y`.

Also install additional programs using more specific instructions and installation methods:

- [Go](instlGo.md)
- [Node.js and npm with nvm](inNjspv.md)
- [pip](instpip.md)

- Pandoc [from the latest GitHub software release](islGHsr.md)
- [VirtualBox](instVBx.md)
- [youtube-dl](insytdl.md)

### dpkg
- [Atom text editor](insAtom.md) (64-bit systems only)
- [Google Chrome](insGCrm.md) (64-bit systems only)

### npm
- [Lloyd Brookes's renamer](inLBrnm.md)

### pip
- [beets](insbeet.md)
- [MkDocs](insMkDc.md)
- [sqlitebiter](inqbitr.md)

### PPA
- [DB Browser for SQLite](inDBSQL.md)
- [Git](instGit.md)
- [Krita](insKrta.md)
- [qBittorrent](insqBtr.md)
- [uGet](instuGt.md)

For Lubuntu, install additional packages using `sudo apt install dolphin kate openjdk-8-jre`.

??? info "Personal experience"
    Tested in Lubuntu 18.04.1.

## explanation

!!! note
    
    This is an incomplete explanation.

| package name               | program name                                             | program category           | licensing
|:---------------------------|:---------------------------------------------------------|:---------------------------|:-
| `audacity`                 | [Audacity]                                               | [audio editor]             | [GNU GPL v2.0][^insLnxS6]
| `bless`                    | [Bless]                                                  | [hex editor]               | [GNU GPL v2.0][^insLnxS2]
| `cheese`                   | [Cheese]                                                 | [webcam] software          | [GNU GPL v2.0][^insLnxS7]
| `codeblocks`               | [Code::Blocks]                                           | [IDE]                      | [GNU GPL v3.0][^insLnxS8]
| `curl`                     | [Curl]                                                   | data transfer tool         | MIT/X-inspired license[^insLnxS10]
| `git-cola`                 | [Git Cola]                                               | [version control] software | [GNU GPL v2.0][^insLnxS9]
| `gprename`                 | [GPRename]                                               | [batch renamer]            | [GNU GPL v3.0][^insLnxS4]
| `krename`                  | [KRename]                                                | [batch renamer]            | [GNU GPL v2.0][^insLnxS5]
| `net-tools`                | [ifconfig], part of [net-tools]                          | administration utility     | [GNU GPL v2.0][^insLnxS3]
| `openjdk-8-jre`[^insLnxS1] | the [Open Java Development Kit] Java Runtime Environment

[Audacity]: https://www.audacityteam.org/
[Bless]: https://github.com/afrantzis/bless
[Cheese]: https://wiki.gnome.org/Apps/Cheese
[Code::Blocks]: http://codeblocks.org/
[Curl]: https://curl.haxx.se/
[Git Cola]: http://git-cola.github.io/
[GNU GPL v2.0]: https://choosealicense.com/licenses/gpl-2.0/
[GNU GPL v3.0]: https://choosealicense.com/licenses/gpl-3.0/
[GPRename]: http://gprename.sourceforge.net/
[IDE]: https://en.wikipedia.org/wiki/Integrated_development_environment
[KRename]: https://www.krename.net/home/
[Open Java Development Kit]: https://en.wikipedia.org/wiki/OpenJDK
[audio editor]: https://en.wikipedia.org/wiki/Audio_editing_software
[batch renamer]: https://en.wikipedia.org/wiki/Batch_renaming
[hex editor]: https://en.wikipedia.org/wiki/Hex_editor
[ifconfig]: https://en.wikipedia.org/wiki/Ifconfig
[net-tools]: https://sourceforge.net/p/net-tools/code/ci/master/tree/README
[version control]: https://en.wikipedia.org/wiki/Version_control
[webcam]: https://en.wikipedia.org/wiki/Webcam

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The method of installing GPRename was introduced to me by [an answer on Ask Ubuntu by karel](https://askubuntu.com/questions/1030996/how-can-i-install-pyrenamer-for-bionic/1031003#1031003).
- The method of installing updates was introduced to me by [a post on Reddit by MyNameIsRichardCS54](https://www.reddit.com/r/Kubuntu/comments/99jfb5/every_new_install_of_kubuntu_1804_freezes_up_when/e4qsx0a/).

[Linux]: https://en.wikipedia.org/wiki/Linux_distribution
[Ubuntu-based]: https://en.wikipedia.org/wiki/List_of_Linux_distributions#Ubuntu-based
[^insLnxS1]: <http://openjdk.java.net/install/>
[^insLnxS2]: <https://github.com/afrantzis/bless/blob/master/COPYING>
[^insLnxS3]: <https://sourceforge.net/p/net-tools/code/ci/master/tree/COPYING>
[^insLnxS4]: <https://sourceforge.net/p/gprename/code/HEAD/tree/trunk/COPYING.TXT>
[^insLnxS5]: <https://sourceforge.net/p/krename/code/HEAD/tree/trunk/COPYING>
[^insLnxS6]: <https://github.com/audacity/audacity/blob/master/LICENSE.txt>
[^insLnxS7]: <https://gitlab.gnome.org/GNOME/cheese/blob/master/COPYING>
[^insLnxS8]: <http://codeblocks.org/license>
[^insLnxS9]: <https://github.com/git-cola/git-cola/blob/master/COPYING>
[^insLnxS10]: <https://curl.haxx.se/docs/copyright.html>
