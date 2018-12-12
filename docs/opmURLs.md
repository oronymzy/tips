# opening multiple URLs

!!! bug
    If a private browsing window is not already open when the script is run, one of the URLs in the list will not open in Firefox.

!!! attention
    If [Restore previous session](https://support.mozilla.org/en-US/kb/restore-previous-session) is enabled in Firefox, the tabs will need to be closed individually or with ++"File > Exit"++ in the menu to avoid re-opening all the tabs the next time Firefox is closed and reopened.

!!! attention
    If Firefox is not already open, running the command will open Firefox, and the command prompt will be inaccessible until Firefox is closed.

For Firefox, use `for i in $(</foo/bar/baz.txt); do firefox --private-window $i; done`, where */foo/bar/baz.txt* is the path to the text file containing the list of URLs to be opened. By default, the script opens the tabs in a new private window. Omit `--private-window` to open the URLs in an ordinary window instead.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The idea of using [Firefox with the command line](https://developer.mozilla.org/en-US/docs/Mozilla/Command_Line_Options) was introduced to me by [an answer on Super User by WakiMiko](https://superuser.com/questions/385207/how-to-open-a-list-of-urls-in-firefox-or-seamonkey/385218#385218).
- The way to use a [for loop](https://en.wikipedia.org/wiki/For_loop) in Bash was explained to me in [the Linux Documentation Project](http://tldp.org/HOWTO/Bash-Prog-Intro-HOWTO-7.html).
