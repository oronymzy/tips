# getting a list of URLs from a website
Use `lynx -dump -listonly -nonumbers foo.bar | grep -e barfoo > foobar.txt`, where *foo.bar* is the web page's URL, *barfoo* is a text string to base included URLs on, for example a file extension, and *foobar.txt* is the outputted list of URLs.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
The `-dump` and `-listonly` options for [Lynx](http://lynx.invisible-island.net/) were introduced to me by [a comment on Stack Exchange by michas](https://unix.stackexchange.com/questions/116987/how-do-i-use-wget-to-download-all-links-from-my-site-and-save-to-a-text-file/116990#116990).
