# installing a [Linux] system
## [Ubuntu-based] systems

To install updates, use `sudo apt update && sudo apt full-upgrade && sudo apt autoremove`.

To install officially supported programs, use `sudo apt install audacity bless cheese codeblocks curl easytag exfat-fuse exfat-utils exiftool extundelete eyed3 festival filelight filezilla flac focuswriter fortune gedit gimp git-cola gnome-disk-utility gnome-terminal gnumeric gparted graphviz grsync idle imagemagick inkscape jekyll jq krename lftp lolcat lynx mediainfo meld moreutils ncdu net-tools pmount pngcrush qtqr recode retext searchmonkey simplescreenrecorder sox surf tesseract-ocr testdisk texlive-fonts-recommended transmission-qt trash-cli tree unoconv unrar unrtf vlc vnstat zbar-tools -y`.

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

| package name                   | program name                                             | program category                         | licensing
|:-------------------------------|:---------------------------------------------------------|:-----------------------------------------|:-
| `audacity`                     | [Audacity]                                               | [audio editor]                           | [GNU GPL v2.0][^insLnxS6]
| `bless`                        | [Bless]                                                  | [hex editor]                             | [GNU GPL v2.0][^insLnxS2]
| `cheese`                       | [Cheese]                                                 | [webcam] software                        | [GNU GPL v2.0][^insLnxS7]
| `codeblocks`                   | [Code::Blocks]                                           | [IDE]                                    | [GNU GPL v3.0][^insLnxS8]
| `curl`                         | [Curl]                                                   | data transfer tool                       | MIT/X-inspired license[^insLnxS10]
| `easytag`                      | [EasyTag]                                                | [tag editor]                             | [GNU GPL v2.0] or later[^insLnxS14]
| `exfat-fuse` and `exfat-utils` | [exfat]                                                  | [exFAT] [file system] implementation     | [GNU GPL v2.0][^insLnxS15]
| `exiftool`                     | [ExifTool]                                               | [tag editor]                             | [GNU GPL v1.0] or later[^insLnxS16]
| `extundelete`                  | [extundelete]                                            | [undeletion] software                    | [GNU GPL v2.0][^insLnxS17]
| `eyed3`                        | [eyeD3]                                                  | [tag editor]                             | [GNU GPL v3.0][^insLnxS18]
| `festival`                     | [Festival Speech Synthesis System]                       | [speech synthesis]                       | MIT-like license[^insLnxS11]
| `filelight`                    | [Filelight]                                              | [computer data storage] analyzer         | [GNU GPL v2.0][^insLnxS19]
| `filezilla`                    | [FileZilla]                                              | [FTP] software                           | [GNU GPL v2.0] or later[^insLnxS20]
| `flac`                         | [FLAC]                                                   | [lossless] [audio] compression [codec]   | [GNU GPL][^insLnxS21]
| `git-cola`                     | [Git Cola]                                               | [version control] software               | [GNU GPL v2.0][^insLnxS9]
| `gprename`                     | [GPRename]                                               | [batch renamer]                          | [GNU GPL v3.0][^insLnxS4]
| `krename`                      | [KRename]                                                | [batch renamer]                          | [GNU GPL v2.0][^insLnxS5]
| `net-tools`                    | [ifconfig], part of [net-tools]                          | administration utility                   | [GNU GPL v2.0][^insLnxS3]
| `openjdk-8-jre`[^insLnxS1]     | the [Open Java Development Kit] Java Runtime Environment
| `pngcrush`                     | [pngcrush]                                               | [PNG] image optimizer                    | libpng-like license
| `sox`                          | [SoX]                                                    | [audio editor]                           | [GNU GPL v2.0] or later[^insLnxS12]
| `tesseract-ocr`                | [Tesseract]                                              | [optical character recognition] software | [Apache License 2.0][^insLnxS13]

[Apache License 2.0]: https://choosealicense.com/licenses/apache-2.0/
[Audacity]: https://www.audacityteam.org/
[Bless]: https://github.com/afrantzis/bless
[Cheese]: https://wiki.gnome.org/Apps/Cheese
[Code::Blocks]: http://codeblocks.org/
[Curl]: https://curl.haxx.se/
[EasyTag]: https://wiki.gnome.org/Apps/EasyTAG
[ExifTool]: https://owl.phy.queensu.ca/~phil/exiftool/
[FLAC]: https://xiph.org/flac/
[FTP]: https://en.wikipedia.org/wiki/File_Transfer_Protocol
[Festival Speech Synthesis System]: http://www.cstr.ed.ac.uk/projects/festival/
[FileZilla]: https://filezilla-project.org/
[Filelight]: https://utils.kde.org/projects/filelight/
[GNU GPL v1.0]: https://www.gnu.org/licenses/old-licenses/gpl-1.0.html
[GNU GPL v2.0]: https://choosealicense.com/licenses/gpl-2.0/
[GNU GPL v3.0]: https://choosealicense.com/licenses/gpl-3.0/
[GNU GPL]: http://www.gnu.org/licenses/licenses.html#GPL
[GPRename]: http://gprename.sourceforge.net/
[Git Cola]: http://git-cola.github.io/
[IDE]: https://en.wikipedia.org/wiki/Integrated_development_environment
[KRename]: https://www.krename.net/home/
[Open Java Development Kit]: https://en.wikipedia.org/wiki/OpenJDK
[PNG]: https://en.wikipedia.org/wiki/Portable_Network_Graphics
[SoX]: http://sox.sourceforge.net/
[Tesseract]: https://github.com/tesseract-ocr/tesseract
[audio editor]: https://en.wikipedia.org/wiki/Audio_editing_software
[audio]: https://en.wikipedia.org/wiki/Digital_audio
[batch renamer]: https://en.wikipedia.org/wiki/Batch_renaming
[codec]: https://en.wikipedia.org/wiki/Codec
[computer data storage]: https://en.wikipedia.org/wiki/Computer_data_storage
[exFAT]: https://en.wikipedia.org/wiki/ExFAT
[exfat]: https://github.com/relan/exfat
[extundelete]: http://extundelete.sourceforge.net/
[eyeD3]: https://github.com/nicfit/eyeD3
[file system]: https://en.wikipedia.org/wiki/File_system
[hex editor]: https://en.wikipedia.org/wiki/Hex_editor
[ifconfig]: https://en.wikipedia.org/wiki/Ifconfig
[lossless]: https://en.wikipedia.org/wiki/Lossless_compression
[net-tools]: https://sourceforge.net/p/net-tools/code/ci/master/tree/README
[optical character recognition]: https://en.wikipedia.org/wiki/Optical_character_recognition
[pngcrush]: https://pmt.sourceforge.io/pngcrush/
[speech synthesis]: https://en.wikipedia.org/wiki/Speech_synthesis
[tag editor]: https://en.wikipedia.org/wiki/Tag_editor
[undeletion]: https://en.wikipedia.org/wiki/Undeletion
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
[^insLnxS11]: <http://www.cstr.ed.ac.uk/projects/festival/freecopyright.html>
[^insLnxS12]: <http://sox.sourceforge.net/sox.html#LICENSE>
[^insLnxS13]: <https://github.com/tesseract-ocr/tesseract/blob/master/LICENSE>
[^insLnxS14]: <https://gitlab.gnome.org/GNOME/easytag/blob/master/README>
[^insLnxS15]: <https://github.com/relan/exfat/blob/master/COPYING>
[^insLnxS16]: <https://owl.phy.queensu.ca/~phil/exiftool/#license>
[^insLnxS17]: <https://sourceforge.net/p/extundelete/code/ci/master/tree/LICENSE>
[^insLnxS18]: <https://github.com/nicfit/eyeD3/blob/master/LICENSE>
[^insLnxS19]: <https://github.com/KDE/filelight/blob/master/COPYING>
[^insLnxS20]: <https://filezilla-project.org/license.php>
[^insLnxS21]: <https://xiph.org/flac/license.html>
