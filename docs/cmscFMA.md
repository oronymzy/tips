# ~~collecting music from the [Free Music Archive]~~
~~Use `lynx -dump -listonly -nonumbers foo.bar | grep -e music/download | wget --content-disposition -i -`, where *foo.bar* is the URL of the page containing the music to be downloaded.~~

!!! attention
    **The Free Music Archive [is closing](http://freemusicarchive.org/member/cheyenne_h/blog/Big_Changes_Ahead_for_FMA)**, so these instructions are no longer useful. Refer to [Archiveteam's page ](https://www.archiveteam.org/index.php?title=Free_Music_Archive) for further information.

!!! warning
    [Be polite](https://en.wikipedia.org/wiki/Web_crawler#Politeness_policy) when using this script on multiple pages in a short period of time.

## explanation
- `lynx -dump -listonly -nonumbers foo.bar` [gets a list of URLs](glsURLs.md) from *foo.bar*.
- `grep -e music/download` returns URLs containing *music/download*.
- `wget --content-disposition -i -` retrieves music files.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The `--content-disposition` and `-i` options for [Wget](https://www.gnu.org/software/wget/) were introduced to me by [an answer on Stack Overflow by dim-0](https://stackoverflow.com/questions/40986340/how-to-wget-a-list-of-urls-in-a-text-file/40986501#40986501) and [an answer on Super User by EightBitTony](https://superuser.com/questions/301044/how-to-wget-a-file-with-correct-name-when-redirected/301051#301051).
- The `-dump` and `-listonly` options for [Lynx](http://lynx.invisible-island.net/) were introduced to me by [an answer on Stack Exchange by michas](https://unix.stackexchange.com/questions/116987/how-do-i-use-wget-to-download-all-links-from-my-site-and-save-to-a-text-file/116990#116990).

[Free Music Archive]: http://www.freemusicarchive.org/
