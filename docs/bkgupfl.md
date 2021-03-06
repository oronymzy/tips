# [backing up] files
## backing up a local [Git] repository

!!! note
    
    - {==foobar==} represents the name of the relevant Git repository to be backed up.
    - {==/foo/bar/baz/foobar==} represents the directory containing the relevant Git repository to be backed up.
    - {==foobar.bundle==} represents the intermediate Git bundle to be created during the course of backing up the relevant Git repository.
    - {==/baz/bar/foo/foobar==} represents the directory containing a backup of the relevant Git repository.

Use `cd "/foo/bar/baz/foobar" && git bundle create "/tmp/foobar.bundle" --all && git clone "/tmp/foobar.bundle" "/baz/bar/foo/foobar"` to back up Git data, excluding any unstaged changes. Then use `rsync -c -r -s -t -v --progress --exclude="/.git/" --exclude="/.gitignore/" "/foo/bar/baz/foobar/" "/baz/bar/foo/foobar"`

!!! info "Additional option"
    
    In rsync, the `-n` [option] enables a dry run, producing information on how the backup would be performed without making any changes to the directory containing a backup of the relevant Git repository.

## explanation

!!! note
    
    This is an incomplete explanation.

- The `-c` [option] enables the checksum-based file skipping.
- The `-r` [option] enables recursion.
- The `-s` [option] disables space-splitting.
- The `-t` [option] preserves file modification time.
- The `-v` [option] increases verbosity.
- The `--exclude="/.git/"` and `--exclude="/.gitignore/"` [options][option] exclude the `.git` directory and `.gitignore` file.
- The `--progress` [option] enables the displaying of transfer progress.

[option]: https://git.samba.org/rsync.git/?p=rsync.git;a=blob;f=rsync.yo;h=207d487eb11fbca9a26a4afa4058794519f17360;hb=HEAD

## prior work
- The bulk of the [rsync](https://rsync.samba.org/) portion of the script was generated by [grsync](http://www.opbyte.it/grsync/).
- The method of using [`git-bundle`](https://git-scm.com/docs/git-bundle) was introduced to me by [an answer to “Backup a GitHub repository” on Stack Overflow by VonC](https://stackoverflow.com/questions/1251713/backup-a-github-repository/1251717#1251717) and [an answer to “How to backup a local Git repository?” on Stack Overflow by VonC](https://stackoverflow.com/questions/2129214/how-to-backup-a-local-git-repository/2129286#2129286).
- The method of using [`git-clone`](https://git-scm.com/docs/git-clone) was introduced to me by [an answer on Stack Overflow by fbicknel](https://stackoverflow.com/questions/9807367/restoring-git-repository-from-bundle-backup/17030169#17030169).

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[backing up]: https://en.wikipedia.org/wiki/Backup
[Git]: https://git-scm.com/
