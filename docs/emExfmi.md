# embedding Exif metadata into an image
Use `exiftool -url='foo.bar' '/foo/bar/foobar.png' && exiftool '/foo/bar/foobar.png'` to add a web page's URL to a PNG file's TextualData tag and verify its inclusion[^gwebscr3], where *foo.bar* is the web page's URL and */foo/bar/foobar.png* is the complete path to the PNG image.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[^gwebscr3]: http://owl.phy.queensu.ca/~phil/exiftool/TagNames/PNG.html
