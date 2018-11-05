# installing VirtualBox
For Kubuntu 18.04, add `deb https://download.virtualbox.org/virtualbox/debian bionic contrib` to `/etc/apt/sources.list`, then use `wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | sudo apt-key add - && sudo apt-get update ; sudo apt-get install virtualbox-5.2`.

!!! attention
    Running a virtual machine may require enabling hardware virtualization in BIOS.

??? info "Personal experience"
    - Works in Kubuntu 18.04 on Slim.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The installation instructions and the bulk of the installation script were introduced to me by [a page on the VirtualBox website](https://www.virtualbox.org/wiki/Linux_Downloads#Debian-basedLinuxdistributions).
- The possibility of enabling hardware virtualization in BIOS was introduced to me by [an answer on Super User by duDE](https://superuser.com/questions/866962/why-does-virtualbox-only-have-32-bit-option-no-64-bit-option-on-windows-7/866963#866963).
