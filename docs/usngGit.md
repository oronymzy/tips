# using [Git]
[Install Git](instGit.md), then set your user name and email address with `git config --global user.email "foo@bar.baz" && git config --global user.name "foobarbaz"`, where *foo@bar.baz* is your email and *foobarbaz* is your user name.

Create a repository in a local directory, ideally including a `README.md` and a `LICENSE.md` file, and a `.gitignore` file if necessary. Navigate to the repository's directory with `cd`, use `git init` to create an empty Git repository, then use `git add .` to update the index. Use `git commit -m "Initial commit"` to establish an initial Git commit with the message *Initial commit*. Single-line commit messages act as summaries, the convention is to write using [imperative mood](https://en.wikipedia.org/wiki/Imperative_mood), start with a capital letter, and end without a period[^usngGit1].

To connect a local repository with a remote repository on GitHub, use `git remote add baz https://github.com/foo/bar.git`, where *foo* is the username, *bar* is the repository name, and *baz* is the shortname of the remote. To change the remote repository, use `git remote set-url baz https://github.com/foo/bar.git`.

To rename the shortname of a remote, use `git remote rename foo bar`, where *foo* is the original shortname and *bar* is the new shortname.

To push the local repository to the connected remote repository on GitHub, use `git push -u baz master` and enter your GitHub username and password at the resulting prompt. It may be useful to first simulate the Git command by including the “dry run” `-n` option, as with `git push -n -u baz master`.

To list all of the already committed files being tracked by your git repository, use `git ls-tree --full-tree -r HEAD`. To detect changes, use `git ls-files -m`.

To amend the most recent commit message before pushing it to a remote repository, use `git commit --amend -m "foobar"`, where *foobar* is the new message.

To create a maximally-compressed [zip](https://en.wikipedia.org/wiki/Zip_(file_format)) archive of the local repository, use `git archive --format=zip -9 -o /foo/bar/baz.zip HEAD`, where */foo/bar/baz.zip* is the path to the zip archive file.

To discard unstaged changes that are not in the index, use `git stash save --keep-index --include-untracked`, then drop the stash with `git stash drop`.

## licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Specifically, the following content falls under this license:

- [An answer on Stack Overflow by karlphillip](https://stackoverflow.com/questions/8533202/list-files-in-local-git-repo/8533413#8533413), with changes made, including rewording of the original text:
> To list all of the already committed files being tracked by your git repository, use `git ls-tree --full-tree -r HEAD`.
- [A question on Stack Overflow by Readonly](https://stackoverflow.com/questions/52704/how-do-i-discard-unstaged-changes-in-git) and [an answer on Stack Overflow by Greg Hewgill](https://stackoverflow.com/questions/52704/how-do-i-discard-unstaged-changes-in-git/52719#52719), with changes made:
> To discard unstaged changes that are not in the index, use `git stash save --keep-index --include-untracked`, then drop the stash with `git stash drop`.

If the above content is omitted, the rest is licensed **no rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The `-n` or `--dry-run` Git option was introduced to me by [an answer on Stack Overflow by YSC](https://stackoverflow.com/questions/40926945/how-to-know-what-differences-that-git-push-is-going-to-push/40927917#40927917).
- The amending of the most recent commit message before pushing it to a remote repository was introduced to me by [an answer on Stack Overflow](https://stackoverflow.com/questions/179123/how-to-modify-existing-unpushed-commits/179147#179147).
- The conntecting of a local repository with a remote repository on GitHub was introduced to me by the default repository instructions on [GitHub](https://github.com/), and further explained in [“A step-by-step guide to Git”](https://opensource.com/article/18/1/step-step-guide-git) by Kedar Vijay Kulkarn on Opensource.com.
- The convention of writing single-line Git commit messages using [imperative mood](https://en.wikipedia.org/wiki/Imperative_mood), to start them with a capital letter, and to end them without a period was introduced to me by [a page on the GitHub Erlang/OTP wiki](https://github.com/erlang/otp/wiki/writing-good-commit-messages).
- The creating of a maximally-compressed zip archive of the local repository was introduced to me by [a comment on GitHub by scofield-ua](https://gist.github.com/kristofferh/1442717#gistcomment-2345577) and [a page on git-scm.com](https://git-scm.com/docs/git-archive).
- The detecting of changes was introduced to me by [an answer on Stack Overflow by Christoffer Hammarström](https://stackoverflow.com/questions/3882838/whats-an-easy-way-to-detect-modified-files-in-a-git-workspace/3882880#3882880).
- The importance of starting a repository with a `README.md`, `LICENSE.md`, and `.gitignore` file was introduced to me by the default repository instructions on [GitHub](https://github.com/).
- The listing of files in Git was introduced to me by [an answer on Stack Overflow by karlphillip](https://stackoverflow.com/questions/8533202/list-files-in-local-git-repo/8533413#8533413).
- The method of discarding unstaged changes that are not in the index was introduced to me by [a question on Stack Overflow by Readonly](https://stackoverflow.com/questions/52704/how-do-i-discard-unstaged-changes-in-git) and [an answer on Stack Overflow by Greg Hewgill](https://stackoverflow.com/questions/52704/how-do-i-discard-unstaged-changes-in-git/52719#52719).
- The renaming of a shortname of a remote was introduced to me by [a page on git-scm.com](https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes#_renaming_and_removing_remotes).
- The setting of email and user name was introduced to me by [a page on git-scm.com](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup#_your_identity).

[Git]: https://git-scm.com/
[^usngGit1]: https://github.com/erlang/otp/wiki/writing-good-commit-messages
