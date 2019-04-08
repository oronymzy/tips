# getting hardware information
Use `lsusb` to display information about connected USB devices.

[S.M.A.R.T. tests](https://en.wikipedia.org/wiki/S.M.A.R.T.#Self-tests) can be performed on storage devices using [GNOME Disks](https://en.wikipedia.org/wiki/GNOME_Disks), but not if they are connected through USB.[^ghdinfo1] For USB-connected devices, use [GSmartControl](https://gsmartcontrol.sourceforge.io/home/index.php/).

## input devices
In Kubuntu, use `xinput --list` to determine which [X](https://en.wikipedia.org/wiki/X_Window_System) input devices are available, then record the *device id* number of the target device (for example `1`) and use `xinput test 1` to get more information about specific inputs. Alternatively, use `xev` to get information about different inputs by interacting with a specially-created window.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[^ghdinfo1]: <https://askubuntu.com/questions/156013/how-do-i-get-disk-utility-to-read-smart-data-from-usb-drives/156023#156023>
