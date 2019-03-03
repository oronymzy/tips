# converting multiple files

## converting multiple PNG files to PNG files with a width of 400 pixels
`for i in !(*-small.png) ; do if test ! -s "${i%.*}-small.png" ; then convert "$i" -resize '400' "${i%.*}-small.png" ; fi ; done`

## converting multiple TIFF files to PNG files
In the current directory, each file with the `.tiff` file extension not already accompanied by a file with `.png` in place of `.tiff` or `-intermediate.png` in place of `.tiff` will be converted into two PNG files.

`for i in *.tiff ; do if { test ! -s "${i%.*}-intermediate.png" && test ! -s "${i%.*}.png"; } ; then convert "$i" "${i%.*}-intermediate.png" && pngcrush "${i%.*}-intermediate.png" "${i%.*}.png" ; fi ; done`

## explanation

!!! note
    
    This is an incomplete explanation.

- `*-small.png` uses [the asterisk (`*`) special character](https://www.tldp.org/LDP/abs/html/special-chars.html#ASTERISKREF) for filename expansion, matching every filename ending in `-small.png`.
- The `-resize '400'` [option](https://imagemagick.org/script/command-line-options.php#resize) changes the [image geometry](https://imagemagick.org/script/command-line-processing.php#geometry) to a width of 400 pixels.

## prior work
- The `test` command was introduced to me by [a comment on a question I asked on Stack Overflow by fmw42](https://stackoverflow.com/questions/53981630/can-imagemagick-be-prevented-from-overwriting-an-existing-image#comment94802728_53981630).
- The bulk of the contents of the script's for-loop construct was introduced to me by [an answer on Super User by Kevin Cox](https://superuser.com/questions/71028/batch-converting-png-to-jpg-in-linux/542671#542671).
- The bulk of the contents of the script's if-construct was introduced to me by [the test (Unix)§Examples page on Wikipedia](https://en.wikipedia.org/wiki/Test_(Unix)#Examples).
- The correct syntax for the if-contruct was introduced to me by [an answer on Stack Overflow by Shawn Chin](https://stackoverflow.com/questions/4986109/inline-if-shell-script/4986141#4986141).

## licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Includes significant content from [an answer on Super User by Kevin Cox](https://superuser.com/questions/71028/batch-converting-png-to-jpg-in-linux/542671#542671) and [test (Unix)§Examples](https://en.wikipedia.org/w/index.php?title=Test_(Unix)&oldid=884867993#Examples) on Wikipedia, with changes made.
