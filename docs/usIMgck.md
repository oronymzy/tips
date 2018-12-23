# using [ImageMagick]

!!! attention
    
    If the error messages `width or height exceeds limit` and `cache resources exhausted` are encountered, it may be necessary to change the resource limits that ImageMagick has set for itself. In Kubuntu, this can be done by editing the default resource policies stored in the `policy.xml` [configuration file](https://imagemagick.org/script/resources.php) located in `/etc/ImageMagick-6/`. Use `cd /etc/ImageMagick-6/` to navigate to the directory, `sudo cp policy.xml policy.xml.bak` to make a backup file, and `sudo nano policy.xml` to open the file using [nano](https://www.nano-editor.org/). Set the width and height values to `32KP` and the memory and disk values to `2GiB`, all under `<policymap>`.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
The possibility of changing ImageMagick's resource limits was introduced to me by [a thread on the ImageMagick forums](http://www.imagemagick.org/discourse-server/viewtopic.php?t=34044) and [an issue on GitHub](https://github.com/ImageMagick/ImageMagick/issues/396).

[ImageMagick]: https://www.imagemagick.org/script/index.php
