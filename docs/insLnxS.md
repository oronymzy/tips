# installing a [Linux] system
## [Ubuntu-based] systems

To install updates, use `sudo apt update && sudo apt full-upgrade && sudo apt autoremove`.

To install officially supported programs, use `sudo apt install audacity cheese csstidy curl easytag elinks exfat-fuse exfat-utils exiftool extundelete eyed3 festival filelight filezilla flac focuswriter fortune gedit gimp git-cola gnome-disk-utility gnome-terminal gnumeric gparted graphviz grsync idle imagemagick inkscape jekyll jq krename lftp lolcat lynx mediainfo meld moreutils ncdu net-tools pmount qtqr recode retext searchmonkey simplescreenrecorder sox surf testdisk texlive-fonts-recommended transmission-qt trash-cli tree unoconv unrar unrtf vlc vnstat zbar-tools -y`.

Also install additional programs using more specific instructions:

- [pip](instpip.md)
- [beets](insbeet.md)
- Brackets and Pandoc [from the latest GitHub software release](islGHsr.md)
- [Git (PPA)](instGit.md)
- [Go](instlGo.md)
- [Google Chrome](insGCrm.md) (64-bit systems only)
- [Krita (PPA)](insKrta.md)
- [MkDocs](insMkDc.md)
- [qBittorrent (PPA)](insqBtr.md)
- [uGet (PPA)](instuGt.md)
- [youtube-dl](insytdl.md)

For Lubuntu, install additional packages using `sudo apt install dolphin kate openjdk-8-jre`.

??? info "Personal experience"
    Tested in Lubuntu 18.04.1.

## explanation

!!! note
    This is an incomplete explanation.

- `net-tools` installs [ifconfig](https://en.wikipedia.org/wiki/Ifconfig).
- `openjdk-8-jre`[^insLnxS1] installs the [Open Java Development Kit](https://en.wikipedia.org/wiki/OpenJDK) Java Runtime Environment.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
The method of installing updates was introduced to me by [a post on Reddit by MyNameIsRichardCS54](https://www.reddit.com/r/Kubuntu/comments/99jfb5/every_new_install_of_kubuntu_1804_freezes_up_when/e4qsx0a/).

[Linux]: https://en.wikipedia.org/wiki/Linux_distribution
[Ubuntu-based]: https://en.wikipedia.org/wiki/List_of_Linux_distributions#Ubuntu-based
[^insLnxS1]: http://openjdk.java.net/install/
