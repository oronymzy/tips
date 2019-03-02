# determining which files are affected by a [Git] commit

!!! note
    
    - {==foobar==} represents the 40-character commit object name.

Use `git diff-tree --no-commit-id --name-only -r foobar`. This is the preferred way, because it's a *plumbing* command; meant to be programmatic. Alternatively, use `git show --pretty="" --name-only foobar`. This is less preferred for scripts, because it's a *porcelain* command; meant to be user-facing.

## explanation
- The `--no-commit-id` suppresses the commit ID output.
- The `--pretty argument` specifies an empty format string to avoid the cruft at the beginning.
- The `--name-only argument` shows only the file names that were affected.
- The `-r` argument is to recurse into sub-trees.

## licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Includes significant content from [an answer on Stack Overflow by Ryan McGeary](https://stackoverflow.com/questions/424071/how-to-list-all-the-files-in-a-commit/424142#424142) with changes made, including converting the original HTML to Markdown and the removal of “Thanks Hank”.

[Git]: https://git-scm.com/
