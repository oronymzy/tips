# installing software from the latest GitHub software release

!!! attention
    This is a suboptimal solution, relying on the assumption that the filenames of 64-bit *.deb* releases will contain `64.deb` or `64-bit.deb`. **It is not certain to work.**

!!! attention
    A software file and a text file (islGHsr-log.txt) will be saved to the [current directory](https://en.wikipedia.org/wiki/Working_directory).

For 64-bit *.deb* releases, use `curl -s https://api.github.com/repos/foo/bar/releases/latest | jq -r '.assets[].browser_download_url' | grep '64.deb\|64-bit.deb' | xargs -n1 wget | tee ./islGHsr-log.txt && <./islGHsr-log.txt grep 'Saving to' | sed 's/^............//' | sed 's/.$//' | xargs -n1 sudo dpkg -i`, where *foo/bar* is the username and repository name.

!!! bug
    `sed 's/^............//'` is used instead of `cut -cfoobar` (where *foobar* is the number of characters to be removed from the beginning of the string) because [*cut* does not properly handle UTF-8 characters](https://unix.stackexchange.com/questions/163721/can-not-use-cut-c-characters-with-utf-8/163725#163725).

## examples
| software | repository
|:-|:-
| [Brackets](http://brackets.io/) | `https://github.com/adobe/brackets`
| [Pandoc](http://pandoc.org/)[^islGHsr1] | `https://github.com/jgm/pandoc`

## explanation

!!! note
    This is an incomplete explanation.

- `curl -s https://api.github.com/repos/foo/bar/releases/latest | jq -r '.assets[].browser_download_url' | grep '64.deb\|64-bit.deb'` usually (but not always) gets the URL of the software file to be downloaded.
- - `grep '64.deb\|64-bit.deb'` uses the regular expression alternation operator to return lines containing `64.deb` or `64-bit.deb`.
- `islGHsr-log.txt` contains the log messages of wget.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The `-s` cURL option was introduced to me by [an answer on Stack Overflow by Putna](https://stackoverflow.com/questions/24987542/is-there-a-link-to-github-for-downloading-a-file-in-the-latest-release-of-a-repo/26738019#26738019).
- The basic method of using jq to select a URL from a GitHub JSON file was introduced to me by [an answer on Stack Overflow by IanB](https://stackoverflow.com/questions/24987542/is-there-a-link-to-github-for-downloading-a-file-in-the-latest-release-of-a-repo/29360657#29360657).
- The correct way of selecting from multiple arrays with jq was introduced to me by [an answer on Stack Overflow by hek2mgl](https://stackoverflow.com/questions/34543829/jq-cannot-index-array-with-string/34544406#34544406).
- The method of using sed to remove the first 12 characters from a string was introduced to me by [an answer on Stack Overflow by Phil](https://stackoverflow.com/questions/3795512/delete-the-first-five-characters-on-any-line-of-a-text-file-in-linux-with-sed/3806107#3806107).
- The necessity of using a backslash-escape with the regular expression alternation operator was introduced to me by [an answer on Stack Exchange by Gilles](https://unix.stackexchange.com/questions/37313/how-do-i-grep-for-multiple-patterns-with-pattern-having-a-pipe-character/37316#37316).
- The possibility of using xargs to make standard output into an option for another program was introduced to me by [an answer on Stack Overflow by Kyle Jones](https://stackoverflow.com/questions/8957744/wget-or-curl-from-stdin/8957796#8957796) and [a post on Ubuntu Forums by llamakc](https://ubuntuforums.org/archive/index.php/t-1174793.html).

[^islGHsr1]: http://pandoc.org/installing.html
