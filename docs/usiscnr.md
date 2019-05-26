# using an [image scanner]

## [Epson Perfection V600 Photo]

This scanner is not supported by [SANE](https://en.wikipedia.org/wiki/Scanner_Access_Now_Easy)[^usiscnr1], but there is [a proprietary Linux driver](http://download.ebz.epson.net/dsc/du/02/DriverDownloadInfo.do?LG2=EN&CN2=&DSCMI=47262&DSCCHK=d177e2e8a56fec619d2b1b033dd50bae38ffc60f) packaged with the [Image Scan! for Linux](http://download.ebz.epson.net/man/linux/iscan_e.html) software.

For Kubuntu, download [the deb package](http://support.epson.net/linux/en/iscan.php?model=gt-x820&version=1.0.1), unarchive the [archive file](https://en.wikipedia.org/wiki/Archive_file) with the [.tar.gz](https://en.wikipedia.org/wiki/Tar_(computing)#Suffixes_for_compressed_files) [extension](https://en.wikipedia.org/wiki/Filename_extension), navigate into the unarchived directory, and run the installation script with `./install.sh`.

!!! attention
    
    At some point, Kubuntu made a change that broke compatibility with [Image Scan! for Linux](http://download.ebz.epson.net/man/linux/iscan_e.html), seemingly related to a naming change of the `libsane` library to `libsane1`.[^usiscnr2] For Kubuntu 17.10 “Artful Aardvark” and Kubuntu 18.04 “Bionic Beaver”, a workaround is to add the following line to `/etc/apt/sources.list`:[^usiscnr3] `deb http://archive.ubuntu.com/ubuntu/ artful-proposed restricted main multiverse universe`. Use `sudo apt-get update`, `sudo apt install libsane1`, `sudo cp /usr/lib/sane/libsane-epkowa.* /usr/lib/x86_64-linux-gnu/sane/`. Then use `sudo nano /etc/udev/rules.d/79-udev-epson.rules` to create `79-udev-epson.rules`, and add the following content to the file:
    ```
    # chmod device EPSON group
    ATTRS{manufacturer}=="EPSON", DRIVERS=="usb", SUBSYSTEMS=="usb", ATTRS{idVendor}=="04b8", ATTRS{idProduct}=="*", MODE="0777"
    ```
    Reboot.

[Epson Perfection V600 Photo]: https://epson.com/Support/Scanners/Perfection-Series/Epson-Perfection-V600-Photo/s/SPT_B11B198011

[image scanner]: https://en.wikipedia.org/wiki/Image_scanner
[^usiscnr1]: <http://www.sane-project.org/sane-mfgs.html#Z-EPSON>
[^usiscnr2]: <https://www.kubuntuforums.net/showthread.php/72554-libsane-libsane1-problem-for-scanners?s=a68e8f54bf9469cae48ec608fbfd7953&p=406113&viewfull=1#post406113>
[^usiscnr3]: <https://wiki.ubuntu.com/Testing/EnableProposed>
