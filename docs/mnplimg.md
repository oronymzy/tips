# manipulating images
## combining images

!!! note
    
    - {==foobar.png==} represents a combined output image.

For sequentially-named images in a single directory, use `convert -append *.png foobar.png` to combine images vertically or `convert +append *.png foobar.png` to combine images horizontally.

## rotating images

!!! note
    
    - {==foo.png==} represents an unrotated input image.
    - {==bar.png==} represents a rotated output image.
    - {==baz==} represents the rotation angle to be applied. Recommended values are:
        - `90`
        - `180`
        - `-90`
        - `-180`

Use `convert foo.png -rotate baz bar.png`.

## prior work
- The `-append` and `+append` [options](https://imagemagick.org/script/command-line-options.php#append) were introduced to me by [an answer on Super User by 3498DB](https://superuser.com/questions/316132/appending-images-vertically-in-imagemagick/316189#316189).
- The method of combining sequentially-named images with ImageMagick was introduced to me by [a comment on Stack Overflow by ChillarAnand](https://stackoverflow.com/questions/20075087/how-to-merge-images-in-command-line/20075227#20075227).
- The method of rotating an image with ImageMagick was introduced to me by [an answer on Stack Exchange by GAD3R](https://unix.stackexchange.com/questions/365592/how-to-rotate-a-set-of-pictures-from-the-command-line/365595#365595) and [a page on the ImageMagick website](https://imagemagick.org/Usage/warping/).

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**
