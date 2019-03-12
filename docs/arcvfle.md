# [archiving files]

!!! note
    
    - {==foobar.zip==} represents the filename of the ZIP archive file to be created.

In Ubuntu, use `zip -r ../foobar.zip .` to create a [ZIP archive](https://en.wikipedia.org/wiki/Zip_(file_format)) file of the contents of the current directory, including [hidden files and hidden directories](https://en.wikipedia.org/wiki/Hidden_file_and_hidden_directory), saving the file into the parent directory. This requires [Info-ZIP](http://infozip.sourceforge.net/Zip.html).

## prior work
- The method of creating a ZIP archive of the contents of the current directory was introduced to me by [an answer on Unix & Linux Stack Exchange by Romeo Ninov](https://unix.stackexchange.com/questions/182032/zip-the-contents-of-a-folder-without-including-the-folder-itself/182036#182036).
- The method of including hidden files and hidden directories in a ZIP archive was introduced to me by [an answer on Stack Overflow by Gunnar](https://stackoverflow.com/questions/12493206/zip-including-hidden-files/12493244#12493244).

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[archiving files]: https://en.wikipedia.org/wiki/File_archiver
