# installing a [CentOS] system

!!! attention
    By default, CentOS 7 installs the *Minimal Install* *Base Environment*, without a GUI. I recommend a KDE-based GUI. Under *Base Environment*, choose *KDE Plasma Workspaces*, and select all under *Add-Ons for Selected Environment*.

!!! warning
    To run properly a virtual machine using VirtualBox, CentOS will need:
    
    - At least 1024 MB of memory to run correctly (2048 MB of memory may be too much).
    - At least 16 GB of disk space is necessary to correctly install updates.

After selecting an *Installation Destination* and making a *Software Selection*, select ++"Begin Installation"++ and, if necessary, create a user and set a root password.

!!! attention
    If using the same password for user and root password, create the user first and the root password second, otherwise the installer may crash.

After rebooting, you will need to accept the EULA before continuing.

To install updates, use `sudo yum check-update && sudo yum upgrade`.

For CentOS 7, install officially supported programs with:

`sudo yum install gedit gimp ImageMagick inkscape lynx recode tree`

!!! attention
    By default, CentOS 7 includes Python 2.7.5, which may need to be [updated](insPyth.md).

Additionally, some packages will need to be installed from the [Extra Packages for Enterprise Linux (EPEL)](https://fedoraproject.org/wiki/EPEL) repository and the [Nux Dextop](https://li.nux.ro/repos.html) repository. To enable access, use:

`sudo yum install epel-release && sudo rpm -Uvh http://li.nux.ro/download/nux/dextop/el7/x86_64/nux-dextop-release-0-5.el7.nux.noarch.rpm`

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

Also install additional programs using more specific instructions:

- [pip](instpip.md)
- [beets](insbeet.md)
- [Git](instGit.md)
- [Go](instlGo.md)
- [Google Chrome](insGCrm.md)

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The fact that a *Minimal Install* *Base Environment* is installed by default was introduced to me by [an answer on Stack Exchange by Nasir Riley](https://unix.stackexchange.com/questions/434912/newly-installed-centos-7-boots-to-command-line-and-unable-to-enter-gui/434923#434923).
- The method of enabling access to the EPEL and Nux Dextop repositories was introduced to me by [a page on the Fedora Project Wiki](https://fedoraproject.org/wiki/EPEL#How_can_I_use_these_extra_packages.3F) and [the My RPM repositories homepage](https://li.nux.ro/repos.html).

[CentOS]: https://www.centos.org/
[^insCOSs1]: https://li.nux.ro/repos.html
