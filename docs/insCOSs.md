# installing a CentOS system
For CentOS 7, install officially supported programs with:

`sudo yum install gedit gimp ImageMagick inkscape lynx recode tree`

Additionally, some packages will need to be installed from the [Extra Packages for Enterprise Linux (EPEL)](https://fedoraproject.org/wiki/EPEL) repository and the [Nux Dextop](https://li.nux.ro/repos.html) repository. To enable access, use:

`sudo yum install epel-release && rpm -Uvh http://li.nux.ro/download/nux/dextop/el7/x86_64/nux-dextop-release-0-5.el7.nux.noarch.rpm`

!!! warning
    Nux Dextop can coexist with EPEL, but any other repositories are likely to cause conflict.[^insCOSs1]

!!! note
    These repositories were chosen arbitrarily. Audacity was the first in an alphabetical list of programs I considered important to have in CentOS, and EPEL was the only repository I found with an Audacity package available. Better repositories may exist, I just haven't found any.

then install the following packages from EPEL:

`sudo yum install audacity filezilla gparted grsync jq meld moreutils pandoc qbittorrent testdisk transmission uget`

!!! note
    The Audacity EPEL package does not include MP3 support unless ffmpeg is also installed from Nux Dextop.

and install the following packages from Nux Dextop:

`sudo yum install ffmpeg kupfer vlc`

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The method of enabling access to the EPEL and Nux Dextop repositories was introduced to me by [a page on the Fedora Project Wiki](https://fedoraproject.org/wiki/EPEL#How_can_I_use_these_extra_packages.3F) and [the My RPM repositories homepage](https://li.nux.ro/repos.html).

[^insCOSs1]: https://li.nux.ro/repos.html
