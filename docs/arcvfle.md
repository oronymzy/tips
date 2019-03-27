# [archiving files]

!!! note
    
    - {==foobar.txt==} represents the filename of a text file containing a list of any files and/or directories to be excluded from the ZIP archive file to be created.
    - {==foobar.zip==} represents the filename of the ZIP archive file to be created.

In Ubuntu, use `zip -r ../foobar.zip . -x@foobar.txt` to create a [ZIP archive](https://en.wikipedia.org/wiki/Zip_(file_format)) file of the contents of the current directory, including [hidden files and hidden directories](https://en.wikipedia.org/wiki/Hidden_file_and_hidden_directory) but excluding any files and/or directories specified in *foobar.txt*, saving the file into the parent directory. This requires [Info-ZIP](http://infozip.sourceforge.net/Zip.html).

## explanation
- The `-r` option enables recursion.
- The `-x@foobar.txt` option enables the exclusion of any files and/or directories specified in *foobar.txt*.

## prior work
- The method of excluding files and/or directories from a ZIP archive to be created was introduced to me by [an answer on Ask Ubuntu by Isaiah](https://askubuntu.com/questions/28476/how-do-i-zip-up-a-folder-but-exclude-the-git-subfolder/28482#28482).
- The method of including hidden files and hidden directories in a ZIP archive to be created was introduced to me by [an answer on Stack Overflow by Gunnar](https://stackoverflow.com/questions/12493206/zip-including-hidden-files/12493244#12493244).
- The method of including the contents of the current directory in a ZIP archive to be created was introduced to me by [an answer on Unix & Linux Stack Exchange by Romeo Ninov](https://unix.stackexchange.com/questions/182032/zip-the-contents-of-a-folder-without-including-the-folder-itself/182036#182036).

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[archiving files]: https://en.wikipedia.org/wiki/File_archiver
