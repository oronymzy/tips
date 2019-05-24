# using [Termux]

Use `pkg install curl espeak flac git gnupg golang imagemagick libqrencode nano ncdu parted play-audio python sox tesseract tree wget zbar -y` to install essential packages.

If [pip](https://pip.pypa.io/en/stable/) was installed with [Termux's Python package](https://github.com/termux/termux-packages/tree/master/packages/python), use `pip install --upgrade pip`. If not, [install pip](instpip.md).

To list all packages, use `pkg list-all`.

To request read/write permissions, use `termux-setup-storage`.

To open files in external applications, use `termux-open`.

Termux's effective [temporary directory](https://en.wikipedia.org/wiki/Temporary_folder) is `/data/data/com.termux/files/usr/tmp`.

Termux uses the volume-down button to emulate the control key, and the volume-up button is a special key to produce certain inputs.

## explanation

!!! note
    
    This is an incomplete explanation.

| package name  | program name  | program category                         | licensing
|:--------------|:--------------|:-----------------------------------------|:-
| [espeak]      | [eSpeak NG]   | [speech synthesis]                       | [GNU GPL v3.0] [^usgTrmx2]
| [git]         | [Git]         | [distributed version control]            | [GNU GPL v2.0] [^usgTrmx4]
| [golang]      | [Go]          | [programming language]                   | [BSD]-style license [^usgTrmx5] with [patent] grant [^usgTrmx6]
| [imagemagick] | [ImageMagick] | [image editing]                          | [ImageMagick License] [^usgTrmx7]
| [libqrencode] | [Libqrencode] | [QR code] encoding                       | [GNU LGPL v2.1] [^usgTrmx8]
| [nano]        | [GNU nano]    | [text editing]                           | [GNU GPL v3.0] [^usgTrmx9]
| [python]      | [Python]      | [programming language]                   | [PSFL] [^usgTrmx3]
| [tesseract]   | [Tesseract]   | [optical character recognition] software | [Apache License 2.0] [^usgTrmx1]

[Apache License 2.0]: https://choosealicense.com/licenses/apache-2.0/
[BSD]: https://en.wikipedia.org/wiki/BSD_licenses
[GNU GPL v2.0]: https://choosealicense.com/licenses/gpl-2.0/
[GNU GPL v3.0]: https://choosealicense.com/licenses/gpl-3.0/
[GNU LGPL v2.1]: https://www.gnu.org/licenses/old-licenses/lgpl-2.1.en.html
[GNU nano]: https://nano-editor.org/
[Git]: https://git-scm.com/
[Go]: https://golang.org/
[ImageMagick License]: https://imagemagick.org/script/license.php
[ImageMagick]: http://www.imagemagick.org/
[Libqrencode]: https://github.com/fukuchi/libqrencode
[PSFL]: https://docs.python.org/3/license.html
[Python]: https://github.com/python/cpython
[QR code]: https://en.wikipedia.org/wiki/QR_code
[Tesseract]: https://github.com/tesseract-ocr/tesseract
[distributed version control]: https://git-scm.com/
[eSpeak NG]: https://github.com/espeak-ng/espeak-ng
[espeak]: https://github.com/termux/termux-packages/tree/master/packages/espeak
[git]: https://github.com/termux/termux-packages/tree/master/packages/git
[golang]: https://github.com/termux/termux-packages/tree/master/packages/golang
[imagemagick]: https://github.com/termux/termux-packages/tree/master/packages/imagemagick
[image editing]: https://en.wikipedia.org/wiki/Image_editing
[libqrencode]: https://github.com/termux/termux-packages/tree/master/packages/libqrencode
[nano]: https://github.com/termux/termux-packages/tree/master/packages/nano
[optical character recognition]: https://en.wikipedia.org/wiki/Optical_character_recognition
[patent]: https://en.wikipedia.org/wiki/Software_patent
[programming language]: https://en.wikipedia.org/wiki/Programming_language
[python]: https://github.com/termux/termux-packages/tree/master/packages/python
[speech synthesis]: https://en.wikipedia.org/wiki/Speech_synthesis
[tesseract]: https://github.com/termux/termux-packages/tree/master/packages/tesseract
[text editing]: https://en.wikipedia.org/wiki/Text_editor

## prior work
The method of opening files in external applications and the method of requesting read/write permissions was introduced to me by [the “Sharing Data” page on the Termux wiki](https://wiki.termux.com/wiki/Sharing_Data).

## licensing
**Some rights reserved: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).** Includes significant content from [the “Touch Keyboard” page on the Termux wiki](https://wiki.termux.com/wiki/Touch_Keyboard), with changes made. Specifically, the following content falls under this license:

> Termux uses the volume-down button to emulate the control key, and the volume-up button is a special key to produce certain inputs.

If the above content is omitted, the rest is licensed **no rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[Termux]: https://termux.com/
[^usgTrmx1]: <https://github.com/tesseract-ocr/tesseract/blob/master/LICENSE>
[^usgTrmx2]: <https://github.com/espeak-ng/espeak-ng/blob/master/COPYING>
[^usgTrmx3]: <https://github.com/python/cpython/blob/master/LICENSE>
[^usgTrmx4]: <https://git.kernel.org/pub/scm/git/git.git/tree/COPYING>
[^usgTrmx5]: <https://golang.org/LICENSE>
[^usgTrmx6]: <https://golang.org/PATENTS>
[^usgTrmx7]: <https://github.com/ImageMagick/ImageMagick/blob/master/LICENSE>
[^usgTrmx8]: <https://github.com/fukuchi/libqrencode/blob/master/COPYING>
[^usgTrmx9]: <http://git.savannah.gnu.org/cgit/nano.git/tree/COPYING>
