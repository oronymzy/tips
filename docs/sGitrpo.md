# searching a [Git] repository

## searching for Git commits applied to a single file

!!! note
    
    - {==foobar.baz==} represents the single file whose Git commits should be searched.

Use `git log -- foobar.baz`.

### explanation

!!! note
    
    This is an incomplete explanation.

- The `--` [option](https://git-scm.com/docs/git-log#Documentation/git-log.txt---ltpathgt82308203) causes only commits that are enough to explain how the files that match the path(s) following it came to be to be shown.

## searching for Git commits in which a string was added or removed

!!! note
    
    - {==foobar==} represents the string that was added or removed.

Use `git log --all --reverse --source -i -p -G "foobar"`.

### explanation

!!! note
    
    This is an incomplete explanation.

- The `-G` [option](https://git-scm.com/docs/git-log#Documentation/git-log.txt--Gltregexgt) searches for patch text differences containing added or removed lines matching a string. [Regular expressions](https://en.wikipedia.org/wiki/Regular_expression) are supported.
- The `-i` [option](https://git-scm.com/docs/git-log#Documentation/git-log.txt--i) enables case insensitivity for the `-G` search.
- The `-p` [option](https://git-scm.com/docs/git-log#Documentation/git-log.txt--p) generates a patch.
- The `--reverse` [option](https://git-scm.com/docs/git-log#Documentation/git-log.txt---reverse) outputs commits in reverse order.

## prior work
- The functionality of the `-G` option was introduced to me by [an answer on Stack Overflow by Jakub Narębski](https://stackoverflow.com/questions/1337320/how-to-grep-git-commit-diffs-or-contents-for-a-certain-word/1340245#1340245).
- The functionality of the `-p` option was introduced to me by [an answer on Stack Overflow by Nathan Kinsinger](https://stackoverflow.com/questions/4468361/search-all-of-git-history-for-a-string/4472267#4472267).
- The method of searching for Git commits applied to a single file was introduced to me by [an answer on Stack Overflow by ralphtheninja](https://stackoverflow.com/questions/10215197/git-search-for-string-in-a-single-files-history/10216050#10216050).
- The method of searching for Git commits in which a string was added or removed was introduced to me by [an answer on Stack Overflow by Mark Longair](https://stackoverflow.com/questions/5816134/how-to-find-the-git-commit-that-introduced-a-string-in-any-branch/5816177#5816177) and [an answer on Stack Overflow by Ciro Santilli](https://stackoverflow.com/questions/5816134/how-to-find-the-git-commit-that-introduced-a-string-in-any-branch/31621921#31621921).

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[Git]: https://git-scm.com/
