# getting an input device's information
In Kubuntu, use `xinput --list` to determine which [X](https://en.wikipedia.org/wiki/X_Window_System) input devices are available, then record the *device id* number of the target device (for example `1`) and use `xinput test 1` to get more information about specific inputs. Alternatively, use `xev` to get information about different inputs by interacting with a specially-created window.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**
