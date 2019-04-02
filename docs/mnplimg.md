# manipulating images
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
The method of rotating an image with ImageMagick was introduced to me by [an answer on Stack Exchange by GAD3R](https://unix.stackexchange.com/questions/365592/how-to-rotate-a-set-of-pictures-from-the-command-line/365595#365595) and [a page on the ImageMagick website](https://imagemagick.org/Usage/warping/).

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**
