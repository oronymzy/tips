# installing a [Linux] system
## [Ubuntu-based] systems

To install updates, use `sudo apt update && sudo apt full-upgrade && sudo apt autoremove`.

To install officially supported programs, use `sudo apt install audacity bless bzr cheese codeblocks curl duc easytag espeak-ng-espeak exfat-fuse exfat-utils exiftool extundelete eyed3 festival filelight filezilla flac focuswriter gedit gimp git-cola gnome-disk-utility gnome-terminal gnumeric gparted gprename graphviz grsync gsmartcontrol idle imagemagick inkscape jekyll jq kcharselect kmag krename lftp lolcat lynx mediainfo meld mercurial moreutils ncdu net-tools pngcrush qtqr recode recoll retext searchmonkey simplescreenrecorder sox surf tesseract-ocr testdisk texlive-fonts-recommended thunderbird tracker transmission-qt trash-cli tree uget unar unoconv unrar unrtf vlc vnstat zbar-tools -y`.

Also install additional programs using more specific instructions and installation methods:

- [Go](instlGo.md)
- [Node.js and npm with nvm](inNjspv.md)
- [pip](instpip.md)
- [Ruby Version Manager](insRVMr.md)

- Pandoc [from the latest GitHub software release](islGHsr.md)
- [VirtualBox](instVBx.md)
- [youtube-dl](insytdl.md)

### dpkg
- [Atom text editor](insAtom.md) (64-bit systems only)
- [Google Chrome](insGCrm.md) (64-bit systems only)
- [VSCodium](inVSCdm.md)

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

### RubyGems
- [Linguist](insLngst.md)

For Lubuntu, install additional packages using `sudo apt install dolphin kate openjdk-8-jre`.

??? info "Personal experience"
    Tested in Lubuntu 18.04.1.

## explanation

!!! note
    
    This is an incomplete explanation.

| package name                   | program name                                             | program category                                     | [interface]    | licensing                                                            | predominant programming language
|:-------------------------------|:---------------------------------------------------------|:-----------------------------------------------------|:---------------|:---------------------------------------------------------------------|:-
| `audacity`                     | [Audacity]                                               | [audio editing]                                      | [GUI]          | [GNU GPL v2.0] [^insLnxS6]                                           | [C]
| `bless`                        | [Bless]                                                  | [hex editing]                                        | [GUI]          | [GNU GPL v2.0] [^insLnxS2]                                           | [C#]
| `bzr`                          | [Bazaar]                                                 | [version control]                                    | [CLI]          | [GNU GPL v2.0] [^insLnxS81] or later [^insLnxS82]                    | [Python]
| `cheese`                       | [Cheese]                                                 | [webcam] recording                                   | [GUI]          | [GNU GPL v2.0] [^insLnxS7]                                           | [C]
| `codeblocks`                   | [Code::Blocks]                                           | [IDE]                                                | [GUI]          | [GNU GPL v3.0] [^insLnxS8] [^insLnxS67]                              | [C++]
| `curl`                         | [Curl]                                                   | [data transmission]                                  | [CLI]          | MIT/X-inspired license[^insLnxS10] [^insLnxS68]                      | [C]
| `duc`                          | [Duc]                                                    | [computer data storage] analysis                     | [CLI] or [GUI] | [GNU GPL v3.0] [^insLnxS47]                                          | [C]
| `easytag`                      | [EasyTag]                                                | [tag editing]                                        | [GUI]          | [GNU GPL v2.0] or later[^insLnxS14]                                  | [C]
| `espeak-ng-espeak`             | [eSpeak NG]                                              | [speech synthesis]                                   | [CLI]          | [GNU GPL v3.0] [^insLnxS23]                                          | [C]
| `exfat-fuse` and `exfat-utils` | [exfat]                                                  | implementation of [exFAT] [file system]              |                | [GNU GPL v2.0] [^insLnxS15]                                          | [C]
| `exiftool`                     | [ExifTool]                                               | [tag editing]                                        | [CLI]          | [GNU GPL v1.0] or later[^insLnxS16] [^insLnxS69]                     | [Perl]
| `extundelete`                  | [extundelete]                                            | [undeletion]                                         | [CLI]          | [GNU GPL v2.0] [^insLnxS17]                                          | [C++]
| `eyed3`                        | [eyeD3]                                                  | [tag editing]                                        | [GUI]          | [GNU GPL v3.0] [^insLnxS18]                                          | [Python]
| `festival`                     | [Festival Speech Synthesis System]                       | [speech synthesis]                                   | [CLI]          | MIT-like license[^insLnxS11]                                         | [C++]
| `filelight`                    | [Filelight]                                              | [computer data storage] analysis                     | [GUI]          | [GNU GPL v2.0] [^insLnxS19]                                          | [C++]
| `filezilla`                    | [FileZilla]                                              | [data transmission] for [FTP]                        | [GUI]          | [GNU GPL v2.0] [^insLnxS70] or later[^insLnxS20]                     | [C++]
| `flac`                         | [FLAC]                                                   | [lossless] [audio] compression [codec]               | [CLI]          | [GNU GPL] [^insLnxS21] [^insLnxS72]                                  | [C]
| `focuswriter`                  | [FocusWriter]                                            | [word processing]                                    | [GUI]          | [GNU GPL v3.0] [^insLnxS22]                                          | [C++]
| `gedit`                        | [gedit]                                                  | [text editing]                                       | [GUI]          | [GNU GPL v2.0] [^insLnxS24]                                          | [C]
| `gimp`                         | [GIMP]                                                   | [image editing] for [raster graphics]                | [GUI]          | [GNU GPL v3.0] [^insLnxS25] [^insLnxS73]                             | [C]
| `git-cola`                     | [Git Cola]                                               | [version control] for [Git]                          | [GUI]          | [GNU GPL v2.0] [^insLnxS9]                                           | [Python]
| `gnome-disk-utility`           | [gnome-disk-utility]                                     | [disk utility] package                               | [GUI]          | [GNU GPL v2.0] [^insLnxS26]                                          | [C]
| `gnome-terminal`               | [GNOME Terminal]                                         | [terminal emulation]                                 | [GUI]          | [GNU GPL v3.0] [^insLnxS27]                                          | [C]
| `gnumeric`                     | [Gnumeric]                                               | [spreadsheet]                                        | [GUI]          | [GNU GPL v3.0] [^insLnxS28]                                          | [C]
| `gparted`                      | [GParted]                                                | [partition editing]                                  | [GUI]          | [GNU GPL v2.0] [^insLnxS29]                                          | [C++]
| `gprename`                     | [GPRename]                                               | [batch renaming]                                     | [GUI]          | [GNU GPL v3.0] [^insLnxS4]                                           | [Perl]
| `graphviz`                     | [Graphviz]                                               | [graph visualization]                                | [CLI]          | [Eclipse Public License 1.0] [^insLnxS30] [^insLnxS31]               | [C]
| `grsync`                       | [Grsync]                                                 | [file synchronization]                               | [GUI]          | [GNU GPL v2.0] [^insLnxS32]                                          | [C]
| `gsmartcontrol`                | [GSmartControl]                                          | [computer data storage] analysis                     | [GUI]          | [GNU GPL v2.0] or [GNU GPL v3.0] [^insLnxS48] [^insLnxS74]           | [C++]
| `idle`                         | [IDLE]                                                   | [IDE]                                                | [GUI]          | [PSFL] [^insLnxS33]                                                  | [Python]
| `imagemagick`                  | [ImageMagick]                                            | [image editing]                                      | [CLI]          | [ImageMagick License] [^insLnxS34]                                   | [C]
| `inkscape`                     | [Inkscape]                                               | [image editing] for [vector graphics]                | [GUI]          | [GNU GPL v3.0] or later[^insLnxS35]                                  | [C++]
| `jekyll`                       | [Jekyll]                                                 | [static site generation]                             | [CLI]          | [MIT License] [^insLnxS36]                                           | [Ruby]
| `jq`                           | [jq]                                                     | [JSON] processing                                    | [CLI]          | [MIT License] for code and [CC BY 3.0] for documentation[^insLnxS37] | [C]
| `kcharselect`                  | [KCharSelect]                                            | [character] selection                                | [GUI]          | various licenses[^insLnxS85]                                         | [C++]
| `kmag`                         | [KMag]                                                   | [screen magnification]                               | [GUI]          | [GNU GPL v2.0] [^insLnxS60]                                          | [C++]
| `krename`                      | [KRename]                                                | [batch renaming]                                     | [GUI]          | [GNU GPL v2.0] [^insLnxS5]                                           | [C++]
| `lftp`                         | [LFTP]                                                   | [file transferring]                                  | [CLI]          | [GNU GPL v3.0] [^insLnxS38]                                          | [C++]
| `lolcat`                       | [lolcat]                                                 | text colorization ([toy program])                    | [CLI]          | unknown license[^insLnxS39]                                          | [Ruby]
| `lynx`                         | [Lynx]                                                   | [text-based web browsing]                            | [CLI]          | [GNU GPL v2.0] [^insLnxS40]                                          | [C]
| `mediainfo`                    | [MediaInfo]                                              | video file and audio file metadata displaying        | [CLI]          | [BSD 2-Clause license] [^insLnxS41] [^insLnxS42]                     | [Pascal]
| `meld`                         | [Meld]                                                   | [file comparison]                                    | [GUI]          | [GNU GPL v2.0] [^insLnxS43]                                          | [Python]
| `mercurial`                    | [Mercurial]                                              | [version control]                                    | [CLI]          | [GNU GPL v2.0] [^insLnxS79]
| `moreutils`                    | sponge, part of [moreutils]                              | [standard stream] manipulation                       | [CLI]          | various licenses (sponge is licensed [GNU GPL v2.0] [^insLnxS44])
| `ncdu`                         | [Ncdu]                                                   | [computer data storage] analysis                     | [CLI]          | [MIT License] [^insLnxS45]                                           | [C]
| `net-tools`                    | [ifconfig], part of [net-tools]                          | [networking] configuration                           | [CLI]          | [GNU GPL v2.0] [^insLnxS3]                                           | [C]
| `openjdk-8-jre`[^insLnxS1]     | the [Open Java Development Kit] Java Runtime Environment
| `pngcrush`                     | [pngcrush]                                               | [PNG] image optimization                             | [CLI]          | libpng-like license [^insLnxS75]                                     | [C]
| `qtqr`                         | QtQR (part of [QR Tools])                                | [QR code] encoding and decoding                      | [GUI]          | [GNU GPL v3.0] (for [QR Tools]) [^insLnxS49] [^insLnxS77]            | [Python]
| `recode`                       | [recode]                                                 | [character encoding] conversion                      | [CLI]          | [GNU GPL v2.0] [^insLnxS50]                                          | [C]
| `recoll`                       | [Recoll]                                                 | [desktop searching]                                  | [GUI]          | [GNU GPL v2.0] [^insLnxS46]                                          | [C++]
| `retext`                       | [ReText]                                                 | [text editing] for [Markdown] and [reStructuredText] | [GUI]          | [GNU GPL v3.0] [^insLnxS51]                                          | [Python]
| `searchmonkey`                 | [Searchmonkey] ([gSearchmonkey])                         | [desktop searching]                                  | [GUI]          | [GNU LGPL v2.1] [^insLnxS52]                                         | [C]
| `simplescreenrecorder`         | [SimpleScreenRecorder]                                   | [screen recording]                                   | [GUI]          | [GNU GPL v3.0] [^insLnxS54] [^insLnxS55]                             | [C++]
| `sox`                          | [SoX]                                                    | [audio editing]                                      | [CLI]          | [GNU GPL v2.0] [^insLnxS78] or later[^insLnxS12]                     | [C]
| `subversion`                   | [Apache Subversion]                                      | [version control]                                    | [CLI]          | [Apache License 2.0] [^insLnxS71]                                    | [C]
| `surf`                         | [surf]                                                   | [web browsing]                                       | [GUI]          | [MIT License] [^insLnxS56]                                           | [C]
| `tesseract-ocr`                | [Tesseract]                                              | [optical character recognition]                      | [CLI]          | [Apache License 2.0] [^insLnxS13]                                    | [C++]
| `testdisk`                     | [TestDisk]                                               | [data recovery]                                      | [CLI]          | [GNU GPL v2.0] [^insLnxS53]
| `texlive-fonts-recommended`    | recommended fonts for [TeX Live]                         |                                                      |                | [GNU GPL v2.0] [^insLnxS57]
| `thunderbird`                  | [Mozilla Thunderbird]                                    | [email]                                              | [GUI]          | [MPL 2.0] [^insLnxS84]
| `tracker`                      | [Tracker]                                                | [desktop searching]                                  | [CLI]          | [GNU LGPL v2.1] or later, [BSD 3-Clause license], and [GNU GPL v2.0] or later [^insLnxS76] | [C]
| `transmission-qt`              | [Transmission]                                           | [file sharing] for [BitTorrent]                      | [GUI] ([Qt])   | [GNU GPL v2.0] or [GNU GPL v3.0] [^insLnxS58]                        | [C]
| `trash-cli`                    | [trash-cli]                                              | [trashing]                                           | [CLI]          | [GNU GPL v2.0] [^insLnxS59]                                          | [Python]
| `tree`                         | [tree]                                                   | [computer data storage] analysis                     | [CLI]          | [GNU GPL v2.0]                                                       | [C]
| `uget`                         | [uGet]                                                   | [download management]                                | [GUI]          | [GNU LGPL v2.1] [^insLnxS83]                                         | [C]
| `unar`                         | [The Unarchiver]                                         | [archive file] unarchiving                           | [CLI]          | [GNU LGPL v2.1] [^insLnxS80]                                         | [C]
| `unoconv`                      | [unoconv]                                                | [file format] conversion                             | [CLI]          | [GNU GPL v2.0] [^insLnxS61]                                          | [Python]
| `unrar`                        | [UnRAR]                                                  | [RAR] unarchiving                                    | [CLI]          | [trialware]
| `unrtf`                        | [UnRTF]                                                  | [RTF] conversion                                     | [CLI]          | [GNU GPL v3.0] [^insLnxS62]                                          | [C]
| `vlc`                          | [VLC media player]                                       | [media playback]                                     | [GUI]          | [GNU LGPL v2.1] [^insLnxS63] or later [^insLnxS64]                   | [C]
| `vnstat`                       | [vnStat]                                                 | [networking] analysis                                | [CLI]          | [GNU GPL v2.0] [^insLnxS65]                                          | [C]
| `zbar-tools`                   | [ZBar bar code reader]                                   | [barcode reading]                                    | [CLI] or [GUI] | [GNU LGPL v2.1] or later [^insLnxS66]                                | [C]


## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The method of installing GPRename was introduced to me by [an answer on Ask Ubuntu by karel](https://askubuntu.com/questions/1030996/how-can-i-install-pyrenamer-for-bionic/1031003#1031003).
- The method of installing updates was introduced to me by [a post on Reddit by MyNameIsRichardCS54](https://www.reddit.com/r/Kubuntu/comments/99jfb5/every_new_install_of_kubuntu_1804_freezes_up_when/e4qsx0a/).

[MPL 2.0]: https://www.mozilla.org/en-US/MPL/2.0/
[email]: https://en.wikipedia.org/wiki/Email
[Mozilla Thunderbird]: https://en.wikipedia.org/wiki/Mozilla_Thunderbird
[Apache License 2.0]: https://choosealicense.com/licenses/apache-2.0/
[Apache Subversion]: https://en.wikipedia.org/wiki/Apache_Subversion
[Audacity]: https://www.audacityteam.org/
[BSD 2-Clause license]: https://choosealicense.com/licenses/bsd-2-clause/
[BSD 3-Clause license]: https://opensource.org/licenses/BSD-3-Clause
[Bazaar]: http://bazaar.canonical.com/en/
[BitTorrent]: https://en.wikipedia.org/wiki/BitTorrent
[Bless]: https://github.com/afrantzis/bless
[C#]: https://en.wikipedia.org/wiki/C_Sharp_(programming_language)
[C++]: https://en.wikipedia.org/wiki/C%2B%2B
[CC BY 3.0]: https://creativecommons.org/licenses/by/3.0/
[CLI]: https://en.wikipedia.org/wiki/Command-line_interface
[C]: https://en.wikipedia.org/wiki/C_(programming_language)
[character]: https://en.wikipedia.org/wiki/Character_(computing)
[Cheese]: https://wiki.gnome.org/Apps/Cheese
[Code::Blocks]: http://codeblocks.org/
[Curl]: https://curl.haxx.se/
[Duc]: https://duc.zevv.nl/
[EasyTag]: https://wiki.gnome.org/Apps/EasyTAG
[Eclipse Public License 1.0]: https://choosealicense.com/licenses/epl-1.0/
[ExifTool]: https://owl.phy.queensu.ca/~phil/exiftool/
[FLAC]: https://xiph.org/flac/
[FTP]: https://en.wikipedia.org/wiki/File_Transfer_Protocol
[Festival Speech Synthesis System]: http://www.cstr.ed.ac.uk/projects/festival/
[FileZilla]: https://filezilla-project.org/
[Filelight]: https://utils.kde.org/projects/filelight/
[FocusWriter]: https://gottcode.org/focuswriter/
[GIMP]: https://www.gimp.org/
[GNOME Terminal]: https://wiki.gnome.org/Apps/Terminal
[GNU GPL v1.0]: https://www.gnu.org/licenses/old-licenses/gpl-1.0.html
[GNU GPL v2.0]: https://choosealicense.com/licenses/gpl-2.0/
[GNU GPL v3.0]: https://choosealicense.com/licenses/gpl-3.0/
[GNU GPL]: http://www.gnu.org/licenses/licenses.html#GPL
[GNU LGPL v2.1]: https://www.gnu.org/licenses/old-licenses/lgpl-2.1.en.html
[GPRename]: http://gprename.sourceforge.net/
[GParted]: https://gparted.sourceforge.io/
[GSmartControl]: https://gsmartcontrol.sourceforge.io/home/index.php/
[GUI]: https://en.wikipedia.org/wiki/Graphical_user_interface
[Git Cola]: http://git-cola.github.io/
[Git]: https://en.wikipedia.org/wiki/Git
[Gnumeric]: http://www.gnumeric.org/
[Graphviz]: https://www.graphviz.org/
[Grsync]: http://www.opbyte.it/grsync/
[IDE]: https://en.wikipedia.org/wiki/Integrated_development_environment
[IDLE]: https://docs.python.org/3/library/idle.html
[ImageMagick License]: https://imagemagick.org/script/license.php
[ImageMagick]: http://www.imagemagick.org/
[Inkscape]: https://inkscape.org/
[JSON]: https://en.wikipedia.org/wiki/JSON
[Jekyll]: https://jekyllrb.com/
[KCharSelect]: https://utils.kde.org/projects/kcharselect/
[KMag]: https://kde.org/applications/utilities/kmag/
[KRename]: https://sourceforge.net/projects/krename/
[LFTP]: https://lftp.tech/
[Linux]: https://en.wikipedia.org/wiki/Linux_distribution
[Lynx]: https://lynx.invisible-island.net/
[MIT License]: https://choosealicense.com/licenses/mit/
[Markdown]: https://en.wikipedia.org/wiki/Markdown
[MediaInfo]: https://mediaarea.net/en/MediaInfo
[Meld]: http://meldmerge.org/
[Mercurial]: https://www.mercurial-scm.org/
[Ncdu]: https://dev.yorhel.nl/ncdu
[Open Java Development Kit]: https://en.wikipedia.org/wiki/OpenJDK
[PNG]: https://en.wikipedia.org/wiki/Portable_Network_Graphics
[PSFL]: https://docs.python.org/3/license.html
[Pascal]: https://en.wikipedia.org/wiki/Pascal_(programming_language)
[Perl]: https://en.wikipedia.org/wiki/Perl
[Python]: https://en.wikipedia.org/wiki/Python_(programming_language)
[QR Tools]: https://launchpad.net/qr-tools
[QR code]: https://en.wikipedia.org/wiki/QR_code
[Qt]: https://en.wikipedia.org/wiki/Qt_(software)
[RAR]: https://en.wikipedia.org/wiki/RAR_(file_format)
[RTF]: https://en.wikipedia.org/wiki/Rich_Text_Format
[ReText]: https://github.com/retext-project/retext
[Recoll]: https://www.lesbonscomptes.com/recoll/
[Ruby]: https://en.wikipedia.org/wiki/Ruby_(programming_language)
[Searchmonkey]: http://searchmonkey.embeddediq.com/
[SimpleScreenRecorder]: https://www.maartenbaert.be/simplescreenrecorder/
[SoX]: http://sox.sourceforge.net/
[TeX Live]: http://www.tug.org/texlive/
[Tesseract]: https://github.com/tesseract-ocr/tesseract
[TestDisk]: https://www.cgsecurity.org/wiki/TestDisk
[The Unarchiver]: https://bitbucket.org/kosovan/theunarchiver/src/default/
[Tracker]: https://wiki.gnome.org/Projects/Tracker
[Transmission]: https://transmissionbt.com/
[Ubuntu-based]: https://en.wikipedia.org/wiki/List_of_Linux_distributions#Ubuntu-based
[UnRAR]: https://www.rarlab.com/rar_add.htm
[UnRTF]: https://www.gnu.org/software/unrtf/
[VLC media player]: https://www.videolan.org/vlc/
[ZBar bar code reader]: http://zbar.sourceforge.net/
[archive file]: https://en.wikipedia.org/wiki/Archive_file
[audio editing]: https://en.wikipedia.org/wiki/Audio_editing_software
[audio]: https://en.wikipedia.org/wiki/Digital_audio
[barcode reading]: https://en.wikipedia.org/wiki/Barcode_reader
[batch renaming]: https://en.wikipedia.org/wiki/Batch_renaming
[character encoding]: https://en.wikipedia.org/wiki/Character_encoding
[codec]: https://en.wikipedia.org/wiki/Codec
[computer data storage]: https://en.wikipedia.org/wiki/Computer_data_storage
[data recovery]: https://en.wikipedia.org/wiki/Data_recovery
[data transmission]: https://en.wikipedia.org/wiki/Data_transmission
[desktop searching]: https://en.wikipedia.org/wiki/Desktop_search
[disk utility]: https://en.wikipedia.org/wiki/Disk_utility
[download management]: https://en.wikipedia.org/wiki/Download_manager
[eSpeak NG]: https://github.com/espeak-ng/espeak-ng
[exFAT]: https://en.wikipedia.org/wiki/ExFAT
[exfat]: https://github.com/relan/exfat
[extundelete]: http://extundelete.sourceforge.net/
[eyeD3]: https://github.com/nicfit/eyeD3
[file comparison]: https://en.wikipedia.org/wiki/File_comparison
[file format]: https://en.wikipedia.org/wiki/File_format
[file sharing]: https://en.wikipedia.org/wiki/File_sharing
[file synchronization]: https://en.wikipedia.org/wiki/File_synchronization
[file system]: https://en.wikipedia.org/wiki/File_system
[file transferring]: https://en.wikipedia.org/wiki/File_transfer
[gSearchmonkey]: https://sourceforge.net/p/searchmonkey/GTK/ci/master/tree/README
[gedit]: https://wiki.gnome.org/Apps/Gedit
[gnome-disk-utility]: https://gitlab.gnome.org/GNOME/gnome-disk-utility/
[graph visualization]: https://en.wikipedia.org/wiki/Graph_drawing
[hex editing]: https://en.wikipedia.org/wiki/Hex_editor
[ifconfig]: https://en.wikipedia.org/wiki/Ifconfig
[image editing]: https://en.wikipedia.org/wiki/Image_editing
[interface]: https://en.wikipedia.org/wiki/User_interface
[jq]: http://stedolan.github.io/jq/
[lolcat]: https://github.com/busyloop/lolcat
[lossless]: https://en.wikipedia.org/wiki/Lossless_compression
[media playback]: https://en.wikipedia.org/wiki/Media_player_(software)
[moreutils]: http://joeyh.name/code/moreutils/
[net-tools]: https://sourceforge.net/p/net-tools/code/ci/master/tree/README
[networking]: https://en.wikipedia.org/wiki/Computer_network
[optical character recognition]: https://en.wikipedia.org/wiki/Optical_character_recognition
[partition editing]: https://en.wikipedia.org/wiki/Disk_editor#Partition_editor
[pngcrush]: https://pmt.sourceforge.io/pngcrush/
[raster graphics]: https://en.wikipedia.org/wiki/Raster_graphics_editor
[reStructuredText]: https://en.wikipedia.org/wiki/ReStructuredText
[recode]: https://code.launchpad.net/ubuntu/+source/recode
[screen magnification]: https://en.wikipedia.org/wiki/Screen_magnifier
[screen recording]: https://en.wikipedia.org/wiki/Screencast
[speech synthesis]: https://en.wikipedia.org/wiki/Speech_synthesis
[spreadsheet]: https://en.wikipedia.org/wiki/Spreadsheet
[standard stream]: https://en.wikipedia.org/wiki/Standard_streams
[static site generation]: https://en.wikipedia.org/wiki/Web_template_system#Static_site_generators
[surf]: http://surf.suckless.org/
[tag editing]: https://en.wikipedia.org/wiki/Tag_editor
[terminal emulation]: https://en.wikipedia.org/wiki/Terminal_emulator
[text editing]: https://en.wikipedia.org/wiki/Text_editor
[text-based web browsing]: https://en.wikipedia.org/wiki/Text-based_web_browser
[toy program]: https://en.wikipedia.org/wiki/Toy_program
[trash-cli]: https://github.com/andreafrancia/trash-cli
[trashing]: https://en.wikipedia.org/wiki/Trash_(computing)
[tree]: http://mama.indstate.edu/users/ice/tree/
[trialware]: https://en.wikipedia.org/wiki/Shareware#Trialware
[uGet]: https://ugetdm.com
[undeletion]: https://en.wikipedia.org/wiki/Undeletion
[unoconv]: http://dag.wiee.rs/home-made/unoconv/
[vector graphics]: https://en.wikipedia.org/wiki/Vector_graphics_editor
[version control]: https://en.wikipedia.org/wiki/Version_control
[vnStat]: https://humdi.net/vnstat/
[web browsing]: https://en.wikipedia.org/wiki/Web_browser
[webcam]: https://en.wikipedia.org/wiki/Webcam
[word processing]: https://en.wikipedia.org/wiki/Word_processor

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
[^insLnxS22]: <https://github.com/gottcode/focuswriter/blob/master/COPYING>
[^insLnxS23]: <https://github.com/espeak-ng/espeak-ng/blob/master/COPYING>
[^insLnxS24]: <https://gitlab.gnome.org/GNOME/gedit/blob/master/COPYING>
[^insLnxS25]: <https://gitlab.gnome.org/GNOME/gimp/blob/master/COPYING>
[^insLnxS26]: <https://gitlab.gnome.org/GNOME/gnome-disk-utility/blob/master/COPYING>
[^insLnxS27]: <https://gitlab.gnome.org/GNOME/gnome-terminal/blob/master/COPYING>
[^insLnxS28]: <https://gitlab.gnome.org/GNOME/gnumeric/blob/master/COPYING>
[^insLnxS29]: <https://gitlab.gnome.org/GNOME/gparted/blob/master/COPYING>
[^insLnxS30]: <https://gitlab.com/graphviz/graphviz/blob/master/COPYING>
[^insLnxS31]: <https://gitlab.com/graphviz/graphviz/blob/master/epl-v10.txt>
[^insLnxS32]: <https://sourceforge.net/p/grsync/code/HEAD/tree/trunk/grsync/COPYING>
[^insLnxS33]: <https://github.com/python/cpython/blob/master/LICENSE>
[^insLnxS34]: <https://github.com/ImageMagick/ImageMagick/blob/master/LICENSE>
[^insLnxS35]: <https://gitlab.com/inkscape/inkscape/blob/master/COPYING>
[^insLnxS36]: <https://github.com/jekyll/jekyll/blob/master/LICENSE>
[^insLnxS37]: <https://github.com/stedolan/jq/blob/master/COPYING>
[^insLnxS38]: <https://github.com/lavv17/lftp/blob/master/COPYING>
[^insLnxS39]: <https://github.com/busyloop/lolcat/blob/master/LICENSE>
[^insLnxS40]: <https://lynx.invisible-island.net/lynx_help/about_lynx.html>
[^insLnxS41]: <https://mediaarea.net/en/MediaInfo/License>
[^insLnxS42]: <https://github.com/MediaArea/MediaInfo/blob/master/LICENSE>
[^insLnxS43]: <https://gitlab.gnome.org/GNOME/meld/blob/master/COPYING>
[^insLnxS44]: <https://metadata.ftp-master.debian.org/changelogs/main/m/moreutils/moreutils_0.63-1_copyright>
[^insLnxS45]: <https://g.blicky.net/ncdu.git/tree/COPYING>
[^insLnxS46]: <https://opensourceprojects.eu/p/recoll1/code/ci/7e3acf2d0aaa37413e9cc1d0eb32e7c104abc430/tree/src/COPYING>
[^insLnxS47]: <https://github.com/zevv/duc/blob/master/LICENSE>
[^insLnxS48]: <https://gsmartcontrol.sourceforge.io/home/index.php/License>
[^insLnxS49]: <https://launchpad.net/qr-tools>
[^insLnxS50]: <https://git.launchpad.net/ubuntu/+source/recode/tree/COPYING>
[^insLnxS51]: <https://github.com/retext-project/retext/blob/master/LICENSE_GPL>
[^insLnxS52]: <https://sourceforge.net/p/searchmonkey/GTK/ci/master/tree/COPYING.LESSER>
[^insLnxS53]: <https://git.cgsecurity.org/cgit/testdisk/tree/COPYING>
[^insLnxS54]: <https://www.maartenbaert.be/simplescreenrecorder/#license>
[^insLnxS55]: <https://github.com/MaartenBaert/ssr/blob/master/COPYING>
[^insLnxS56]: <http://git.suckless.org/surf/file/LICENSE.html>
[^insLnxS57]: <http://changelogs.ubuntu.com/changelogs/pool/main/t/texlive-base/texlive-base_2017.20180305-1/copyright>
[^insLnxS58]: <https://github.com/transmission/transmission/blob/master/COPYING>
[^insLnxS59]: <https://github.com/andreafrancia/trash-cli/blob/master/COPYING>
[^insLnxS60]: <https://cgit.kde.org/kmag.git/tree/COPYING>
[^insLnxS61]: <https://github.com/unoconv/unoconv/blob/master/COPYING>
[^insLnxS62]: <http://hg.savannah.gnu.org/hgweb/unrtf/file/850a32a10b8e/COPYING>
[^insLnxS63]: <https://git.videolan.org/?p=vlc.git;a=blob_plain;f=COPYING.LIB;hb=HEAD>
[^insLnxS64]: <https://www.videolan.org/press/lgpl-libvlc.html>
[^insLnxS65]: <https://github.com/vergoh/vnstat/blob/master/COPYING>
[^insLnxS66]: <https://sourceforge.net/p/zbar/code/ci/default/tree/COPYING>
[^insLnxS67]: <http://svn.code.sf.net/p/codeblocks/code/trunk/COPYING>
[^insLnxS68]: <https://github.com/curl/curl/blob/master/COPYING>
[^insLnxS69]: <https://github.com/exiftool/exiftool/blob/master/README>
[^insLnxS70]: <https://svn.filezilla-project.org/svn/FileZilla3/trunk/COPYING>
[^insLnxS71]: <https://svn.apache.org/viewvc/subversion/trunk/LICENSE?view=co>
[^insLnxS72]: <https://git.xiph.org/?p=flac.git;a=blob;f=COPYING.GPL;h=d159169d1050894d3ea3b98e1c965c4058208fe1;hb=HEAD>
[^insLnxS73]: <https://gitlab.gnome.org/GNOME/gimp/blob/master/COPYING>
[^insLnxS74]: <https://sourceforge.net/p/gsmartcontrol/code/HEAD/tree/trunk/gsmartcontrol/doc/LICENSE_gsmartcontrol.txt>
[^insLnxS75]: <https://sourceforge.net/p/pmt/code/ci/pngcrush/tree/LICENSE>
[^insLnxS76]: <https://gitlab.gnome.org/GNOME/tracker/blob/master/COPYING>
[^insLnxS77]: <https://bazaar.launchpad.net/~qr-tools-developers/qr-tools/trunk/view/head:/LICENCE>
[^insLnxS78]: <https://sourceforge.net/p/sox/code/ci/master/tree/COPYING>
[^insLnxS79]: <https://www.mercurial-scm.org/repo/hg-stable/file/tip/COPYING>
[^insLnxS80]: <https://bitbucket.org/kosovan/theunarchiver/src/default/License.txt>
[^insLnxS81]: <https://bazaar.launchpad.net/~bzr-pqm/bzr/bzr.dev/view/head:/COPYING.txt>
[^insLnxS82]: <http://wiki.bazaar.canonical.com/Welcome>
[^insLnxS83]: <https://sourceforge.net/p/urlget/uget2/ci/master/tree/COPYING>
[^insLnxS84]: <https://www.mozilla.org/en-US/foundation/licensing/>
[^insLnxS85]: <https://community.kde.org/Policies/Licensing_Policy>
