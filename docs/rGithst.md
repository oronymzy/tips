# rewriting Git history

!!! warning
    This tip involves a lot of risky actions I do not fully understand. **Use at your own risk.**

Use `java -jar bfg-1.13.0.jar --no-blob-protection --replace-text foo.bar "/foo/bar/baz/"`, where *foo.bar* is a text file containing a list of lines of text to be removed, and */foo/bar/baz/* is the directory where the Git repository is stored.

!!! attention
    By default, BFG Repo-Cleaner protects `HEAD` from being modified, so `--no-blob-protection` is added to prevent this.

!!! tip
    By default, BFG Repo-Cleaner replaces the text lines with `**REMOVED**`, so append `==>` to a line to replace it with an empty string.

Then, `cd` into the directory where the Git repository is stored and use `git reflog expire --expire=now --all && git gc --prune=now --aggressive`. Push to remote with `git push foobar --force --all` and `git push foobar --force --tags`, where *foobar* is the shortname of the remote.

Optionally, then use `git commit --dry-run` to check for local changes and `git stash --include-untracked && git stash drop` to discard them.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- `git push foobar --force --all` and `git push foobar --force --tags` was introduced to me by [GitHub documentation on removing sensitive data from a repository](https://help.github.com/articles/removing-sensitive-data-from-a-repository/).
- `git reflog expire --expire=now --all && git gc --prune=now --aggressive` was introduced to me by [a page on the BFG Repo-Cleaner website](http://rtyley.github.io/bfg-repo-cleaner/#usage).
- `git stash --include-untracked && git stash drop` was introduced to me by [a question on Stack Overflow by spiderman](https://stackoverflow.com/questions/22620393/various-ways-to-remove-local-git-changes) and [an answer on Stack Overflow by Greg Hewgill](https://stackoverflow.com/questions/52704/how-do-i-discard-unstaged-changes-in-git/52719#52719).
- The `**REMOVED**` default replacement string was introduced to me by [a page on the BFG Repo-Cleaner website](http://rtyley.github.io/bfg-repo-cleaner/#examples)
- The bulk of the script was introduced to me by [an answer on Stack Overflow by Roberto Tyley](https://stackoverflow.com/questions/872565/remove-sensitive-files-and-their-commits-from-git-history/14656358#14656358)
