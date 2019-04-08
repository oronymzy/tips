# maximizing [data integrity]
## maximizing filesystem consistency

!!! warning
    
    [Fsck](https://en.wikipedia.org/wiki/Fsck) should not be used with [mounted](https://en.wikipedia.org/wiki/Mount_(computing)) storage devices[^vfdatai1] and, even when used correctly, may cause [data loss](https://en.wikipedia.org/wiki/Data_loss).

!!! note
    
    {==/foo/bar==} represents the path of the relevant storage device.

Use `df -T` to [get filesystem information](gflsysi.md) about [mounted](https://en.wikipedia.org/wiki/Mount_(computing)) storage devices. Find the path of the relevant storage device, for example */foo/bar*. [Create a backup archive file](arcvfle.md) of the files stored on the device and, if enough storage space is available, also create a backup disk image with [TestDisk](https://www.cgsecurity.org/wiki/TestDisk). Use `sudo umount /foo/bar` to unmount the storage device. Use `sudo fsck -fv /foo/bar` to run fsck interactively, and answer any resulting prompts. Fsck may create a file with the `.REC` extension on the relevant storage device.

## prior work
The method of unmounting a storage device with umount was introduced to me by [an answer on Unix & Linux Stack Exchange by student](https://unix.stackexchange.com/questions/45820/how-to-umount-a-usb-drive/45821#45821).

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[data integrity]: https://en.wikipedia.org/wiki/Data_integrity
[^vfdatai1]: <https://askubuntu.com/questions/47953/can-i-run-fsck-or-e2fsck-when-linux-file-system-is-mounted/47974#47974>
