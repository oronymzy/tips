# using [Git]
[Install Git](instGit.md), then set your user name and email address with `git config --global user.email "foo@bar.baz" && git config --global user.name "foobarbaz"`, where *foo@bar.baz* is your email and *foobarbaz* is your user name.

Create a repository in a local directory, ideally including a `README.md` and a `LICENSE.md` file, and a `.gitignore` file if necessary. Navigate to the repository's directory with `cd`, use `git init` to create an empty Git repository, then use `git add .` to update the index. Use `git commit -m "Initial commit"` to establish an initial Git commit with the message *Initial commit*. Single-line commit messages act as summaries, the convention is to write using [imperative mood](https://en.wikipedia.org/wiki/Imperative_mood), start with a capital letter, and end without a period[^usngGit1].

To ignore an already-committed directory or file, add it to `.gitignore`, commit the `.gitignore` file, then use `git rm --cached foobar`, where *foobar* is the directory or file to be ignored. The directory or file will not be deleted, and it will now be ignored by Git.

| action                                                                        | script                                                 | representation                                                                                                                                    | notes
|:------------------------------------------------------------------------------|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|:-
| amend the most recent commit message before pushing it to a remote repository | `git commit --amend -m "foobar"`                       | {==foobar==} represents the new message
| create a maximally-compressed [zip] archive of the local repository           | `git archive --format=zip -9 -o /foo/bar/baz.zip HEAD` | {==/foo/bar/baz.zip==} represents the path to the zip archive file.
| detect changes                                                                | `git ls-files -m`
| download a copy of all the versioned data in a Git repository                 | `git clone git://foo.bar/baz.git /foo/bar`[^usngGit2]  | {==git://foo.bar/baz.git==} represents the URI of the Git repository, and {==/foo/bar==} represents the directory the data will be downloaded to. | If {==/foo/bar==} is omitted, the data will be downloaded to a newly-created {==baz==} directory.
| get the commit count across all branches                                      | `git rev-list --all --count`
| list all commits in the commit history of branches and tags                   | `git log --all`
| list all commits with deleted files                                           | `git log --diff-filter=D --summary`
| rename the shortname of a remote                                              | `git remote rename foo bar`                            | {==foo==} represents the original shortname and {==bar==} represents the new shortname.
| set the default text editor                                                   | `git config --global core.editor "foobar"`             | {==foobar==} represents the command that will launch the text editor from the command line.
| verify the data integrity of a Git repository                                 | `git fsck`                                             |                                                                                                                                                   | **fsck** is an abbreviation of **f**ile **s**ystem **c**onsistency **c**heck.[^usngGit-note1] The `--full` [option](https://git-scm.com/docs/git-fsck#Documentation/git-fsck.txt---full) is enabled by default.
| view a specified commit                                                       | `git show foobar`                                      | {==foobar==} represents the 40-character commit object name.

## [GitHub]-specific information

| action                                                                 | script                                                  | representation                                                                                                                     | notes
|:-----------------------------------------------------------------------|:--------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|:-
| change the remote repository on GitHub                                 | `git remote set-url baz https://github.com/foo/bar.git` | {==foo==} represents the username, {==bar==} represents the repository name, and {==baz==} represents the shortname of the remote.
| connect a local repository with a remote repository on GitHub          | `git remote add baz https://github.com/foo/bar.git`     | {==foo==} represents the username, {==bar==} represents the repository name, and {==baz==} represents the shortname of the remote.
| push the local repository to the connected remote repository on GitHub | `git push -u baz master`                                | {==baz==} represents the shortname of the remote.                                                                                  | Enter the user's GitHub username and password at the resulting prompt. It may be useful to first simulate the Git command by including the “dry run” `-n` option, as with `git push -n -u baz master`.


## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/),** excepting [the section below](#lps).

## prior work
- The `-n` or `--dry-run` Git option was introduced to me by [an answer on Stack Overflow by YSC](https://stackoverflow.com/questions/40926945/how-to-know-what-differences-that-git-push-is-going-to-push/40927917#40927917).
- The convention of writing single-line Git commit messages using [imperative mood](https://en.wikipedia.org/wiki/Imperative_mood), to start them with a capital letter, and to end them without a period was introduced to me by [a page on the GitHub Erlang/OTP wiki](https://github.com/erlang/otp/wiki/writing-good-commit-messages).
- The functionality of `git log --all` was introduced to me by [an answer on Stack Overflow by user743382](https://stackoverflow.com/questions/29756637/what-does-git-log-all-do/29756754#29756754).
- The importance of starting a repository with a `README.md`, `LICENSE.md`, and `.gitignore` file was introduced to me by the default repository instructions on [GitHub](https://github.com/).
- The method of amending the most recent commit message before pushing it to a remote repository was introduced to me by [an answer on Stack Overflow](https://stackoverflow.com/questions/179123/how-to-modify-existing-unpushed-commits/179147#179147).
- The method of connecting a local repository with a remote repository on GitHub was introduced to me by the default repository instructions on [GitHub](https://github.com/), and further explained in [“A step-by-step guide to Git”](https://opensource.com/article/18/1/step-step-guide-git) by Kedar Vijay Kulkarn on Opensource.com.
- The method of creating a maximally-compressed zip archive of the local repository was introduced to me by [a comment on GitHub by scofield-ua](https://gist.github.com/kristofferh/1442717#gistcomment-2345577) and [a page on git-scm.com](https://git-scm.com/docs/git-archive).
- The method of detecting changes was introduced to me by [an answer on Stack Overflow by Christoffer Hammarström](https://stackoverflow.com/questions/3882838/whats-an-easy-way-to-detect-modified-files-in-a-git-workspace/3882880#3882880).
- The method of downloading a copy of all the versioned data in a Git repository was introduced to me by [a page on git-scm.com](https://git-scm.com/book/en/v1/Git-Basics-Getting-a-Git-Repository#Cloning-an-Existing-Repository).
- The method of getting the commit count across all branches was introduced to me by [an answer on Stack Overflow](https://stackoverflow.com/questions/677436/how-do-i-get-the-git-commit-count/4061706#4061706).
- The method of ignoring an already-committed directory or file was introduced to me by [an answer on Stack Overflow by manojlds](https://stackoverflow.com/questions/6535362/gitignore-after-commit/6535459#6535459).
- The method of listing all commits in the commit history of branches and tags was introduced to me by [an answer on Stack Overflow by Biffen](https://stackoverflow.com/questions/27324243/how-to-get-all-commit-messages-in-a-repo-by-one-author/27324312#27324312).
- The method of listing all commits with deleted files was introduced to me by [an answer on Stack Overflow by I82Much](https://stackoverflow.com/questions/6017987/how-can-i-list-all-the-deleted-files-in-a-git-repository/6018043#6018043) and [an answer on Stack Overflow by Robert Munteanu](https://stackoverflow.com/questions/953481/find-and-restore-a-deleted-file-in-a-git-repository/953573#953573).
- The method of renaming a shortname of a remote was introduced to me by [a page on git-scm.com](https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes#_renaming_and_removing_remotes).
- The method of setting the default text editor for Git was introduced to me by [an answer on Stack Overflow by digitaldreamer](https://stackoverflow.com/questions/2596805/how-do-i-make-git-use-the-editor-of-my-choice-for-commits/2596835#2596835).
- The method of setting the email and user name was introduced to me by [a page on git-scm.com](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup#_your_identity).
- The method of verifying the data integrity of a Git repository was introduced to me by [an answer on Stack Overflow by CodeWizard](https://stackoverflow.com/questions/42479034/how-to-verify-integrity-of-a-git-folder/42480222#42480222).
- The method of viewing a specified commit was introduced to me by [an answer on Stack Overflow by Graham Borland](https://stackoverflow.com/questions/7663451/view-a-specific-git-commit/7663506#7663506).

[Git]: https://git-scm.com/
[GitHub]: https://github.com/
[zip]: https://en.wikipedia.org/wiki/Zip_(file_format)
[^usngGit1]: <https://github.com/erlang/otp/wiki/writing-good-commit-messages>
[^usngGit2]: <https://git-scm.com/book/en/v1/Git-Basics-Getting-a-Git-Repository#Cloning-an-Existing-Repository>
[^usngGit-note1]: This is based on information from [Wikipedia's “fsck” page](https://en.wikipedia.org/wiki/Fsck).

## [less-freely-licensed](https://creativecommons.org/licenses/by-sa/3.0/) section {: #lps }

To discard unstaged changes that are not in the index, use `git stash save --keep-index --include-untracked`, then drop the stash with `git stash drop`.

| action                                                                        | script                            | representation | notes
|:------------------------------------------------------------------------------|:----------------------------------|:---------------|:-
| list all of the already committed files being tracked by one's Git repository | `git ls-tree --full-tree -r HEAD`
| show files managed by Git                                                     | `git ls-files`                    |                | It is limited to the current directory and any subdirectories.
| undo the initial Git commit by deleting the branch one is on                  | `git update-ref -d HEAD`

### licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Includes significant content from:

- [A question on Stack Overflow by Readonly](https://stackoverflow.com/questions/52704/how-do-i-discard-unstaged-changes-in-git)
- [An answer on Stack Overflow by CB Bailey](https://stackoverflow.com/questions/6632191/how-to-revert-initial-git-commit/6637891#6637891)
- [An answer on Stack Overflow by Greg Hewgill](https://stackoverflow.com/questions/52704/how-do-i-discard-unstaged-changes-in-git/52719#52719)
- [An answer on Stack Overflow by karlphillip](https://stackoverflow.com/questions/8533202/list-files-in-local-git-repo/8533413#8533413)
- [An answer on Stack Overflow by vonbrand](https://stackoverflow.com/questions/15606955/how-can-i-make-git-show-a-list-of-the-files-that-are-being-tracked/15606998#15606998)

with changes made.

### prior work
- The listing of files in Git was introduced to me by [an answer on Stack Overflow by karlphillip](https://stackoverflow.com/questions/8533202/list-files-in-local-git-repo/8533413#8533413).
- The method of discarding unstaged changes that are not in the index was introduced to me by [a question on Stack Overflow by Readonly](https://stackoverflow.com/questions/52704/how-do-i-discard-unstaged-changes-in-git) and [an answer on Stack Overflow by Greg Hewgill](https://stackoverflow.com/questions/52704/how-do-i-discard-unstaged-changes-in-git/52719#52719).
