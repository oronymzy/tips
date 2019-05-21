# using [Termux]

Use `pkg install curl espeak flac fortune git gnupg golang imagemagick libqrencode nano ncdu parted play-audio python sox tesseract tree wget zbar -y` to install essential packages.

To list all packages, use `pkg list-all`.

To request read/write permissions, use `termux-setup-storage`.

To open files in external applications, use `termux-open`.

Termux's effective [temporary directory](https://en.wikipedia.org/wiki/Temporary_folder) is `/data/data/com.termux/files/usr/tmp`.

Termux uses the volume-down button to emulate the control key, and the volume-up button is a special key to produce certain inputs.

## explanation

!!! note
    
    This is an incomplete explanation.

| package name | program name | program category                         | licensing
|:-------------|:-------------|:-----------------------------------------|:-
| [espeak]     | [eSpeak NG]  | [speech synthesis]                       | [GNU GPL v3.0] [^usgTrmx2]
| [python]     | [Python]     | [programming language]                   | [PSFL] [^usgTrmx3]
| [tesseract]  | [Tesseract]  | [optical character recognition] software | [Apache License 2.0] [^usgTrmx1]

[Apache License 2.0]: https://choosealicense.com/licenses/apache-2.0/
[GNU GPL v3.0]: https://choosealicense.com/licenses/gpl-3.0/
[PSFL]: https://docs.python.org/3/license.html
[Tesseract]: https://github.com/tesseract-ocr/tesseract
[eSpeak NG]: https://github.com/espeak-ng/espeak-ng
[espeak]: https://github.com/termux/termux-packages/tree/master/packages/espeak
[optical character recognition]: https://en.wikipedia.org/wiki/Optical_character_recognition
[programming language]: https://en.wikipedia.org/wiki/Programming_language
[python]: https://github.com/termux/termux-packages/tree/master/packages/python
[Python]: https://github.com/python/cpython
[speech synthesis]: https://en.wikipedia.org/wiki/Speech_synthesis
[tesseract]: https://github.com/termux/termux-packages/tree/master/packages/tesseract

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
