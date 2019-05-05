# [backing up] files
## backing up a local [Git] repository

!!! warning
    
    This does not back up unstaged changes.

!!! note
    
    - {==/foo/bar/baz/foobar==} represents the directory containing the relevant Git repository to be backed up.
    - {==foobar.bundle==} represents the intermediate Git bundle to be created during the course of backing up the relevant Git repository.
    - {==/baz/bar/foo/foobar==} represents the directory containing a backup of the relevant Git repository.

Use `cd "/foo/bar/baz/foobar" && git bundle create "/tmp/foobar.bundle" --all && git clone "/tmp/foobar.bundle" "/baz/bar/foo/foobar"`.

## prior work
- The method of using [`git-bundle`](https://git-scm.com/docs/git-bundle) was introduced to me by [an answer to “Backup a GitHub repository” on Stack Overflow by VonC](https://stackoverflow.com/questions/1251713/backup-a-github-repository/1251717#1251717) and [an answer to “How to backup a local Git repository?” on Stack Overflow by VonC](https://stackoverflow.com/questions/2129214/how-to-backup-a-local-git-repository/2129286#2129286).
- The method of using [`git-clone`](https://git-scm.com/docs/git-clone) was introduced to me by [an answer on Stack Overflow by fbicknel](https://stackoverflow.com/questions/9807367/restoring-git-repository-from-bundle-backup/17030169#17030169).

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[backing up]: https://en.wikipedia.org/wiki/Backup
[Git]: https://git-scm.com/
