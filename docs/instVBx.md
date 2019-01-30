# installing [VirtualBox]
For Kubuntu 18.04, add `deb https://download.virtualbox.org/virtualbox/debian bionic contrib` to `/etc/apt/sources.list`, then use `wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | sudo apt-key add - && sudo apt-get update && sudo apt-get install virtualbox-5.2`.

To enable USB 2.0 and 3.0, download the proprietary [VirtualBox Extension Pack](https://www.virtualbox.org/wiki/Downloads#VirtualBox6.0.2OracleVMVirtualBoxExtensionPack) (matching up its version number with the VirtualBox version already installed, found with ++"Help > About VirtualBox..."++) and install it with ++"File > Preferences > Extensions"++. Use `sudo usermod -aG vboxusers foobar` to include the host user in the `vboxusers` group, where *foobar* is the username. Reboot. Use ++"Settings > USB > USB 2.0 (EHCI) Controller"++ to set USB 2.0 instead of 1.0.

!!! attention
    Running a virtual machine may require enabling hardware virtualization in BIOS.

??? info "Personal experience"
    - Works in Kubuntu 18.04 on Slim.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The installation instructions and the bulk of the installation script were introduced to me by [a page on the VirtualBox website](https://www.virtualbox.org/wiki/Linux_Downloads#Debian-basedLinuxdistributions).
- The method of installing the VirtualBox Extension Pack was introduced to me by [an answer on Ask Ubuntu by Takkat](https://askubuntu.com/questions/25596/how-to-set-up-usb-for-virtualbox/25600#25600).
- The possibility of enabling hardware virtualization in BIOS was introduced to me by [an answer on Super User by duDE](https://superuser.com/questions/866962/why-does-virtualbox-only-have-32-bit-option-no-64-bit-option-on-windows-7/866963#866963).

[VirtualBox]: https://www.virtualbox.org/
