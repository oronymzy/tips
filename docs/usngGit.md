# using Git
[Install Git](instGit.md), then set your user name and email address with `git config --global user.email "foo@bar.baz" && git config --global user.name "foobarbaz"`, where *foo@bar.baz* is your email and *foobarbaz* is your user name.

Create a repository in a local directory, ideally including a `README.md` and a `LICENSE.md` file, and a `.gitignore` file if necessary. Navigate to the repository's directory with `cd`, use `git init` to create an empty Git repository, then use `git add .` to update the index. Use `git commit -m "Initial commit"` to establish an initial Git commit with the message *Initial commit*. Single-line commit messages act as summaries, the recommendation is to write using [imperative mood](https://en.wikipedia.org/wiki/Imperative_mood), start with a capital letter, and end without a period[^usngGit1].

To connect a local repository with a remote repository on GitHub, use `git remote add origin https://github.com/foo/bar.git`, where *foo* is the username and *bar* is the repository name. To change the remote repository, use `git remote set-url origin https://github.com/foo/bar.git`.

To push the local repository to the connected remote repository on GitHub, use `git push -u origin master` and enter your GitHub username and password at the resulting prompt. It may be useful to first simulate the Git command by including the “dry run” `-n` option, as with `git push -n -u origin master`.

To list all of the already committed files being tracked by your git repository, use `git ls-tree --full-tree -r HEAD`. To detect changes, use `git ls-files -m`.

To amend the most recent commit message before pushing it to a remote repository, use `git commit --amend -m "foobar"`, where *foobar* is the new message.

## licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Specificially, the following content falls under this license:

- [An answer on Stack Overflow by karlphillip](https://stackoverflow.com/questions/8533202/list-files-in-local-git-repo/8533413#8533413), with changes made, including rewording of the original text:
> To list all of the already committed files being tracked by your git repository, use `git ls-tree --full-tree -r HEAD`.

If the above content is omitted, the rest is licensed **no rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- Amending the most recent commit message before pushing it to a remote repository was introduced to me by [an answer on Stack Overflow](https://stackoverflow.com/questions/179123/how-to-modify-existing-unpushed-commits/179147#179147).
- Detecting changes was introduced to me by [an answer on Stack Overflow by Christoffer Hammarström](https://stackoverflow.com/questions/3882838/whats-an-easy-way-to-detect-modified-files-in-a-git-workspace/3882880#3882880).
- Setting the email and user name was introduced to me by [a page on git-scm.com](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup#_your_identity).
- The `-n` or `--dry-run` Git option was introduced to me by [an answer on Stack Overflow by YSC](https://stackoverflow.com/questions/40926945/how-to-know-what-differences-that-git-push-is-going-to-push/40927917#40927917).
- The connection of a local repository with a remote repository on GitHub was introduced to me by the default repository instructions on [GitHub](https://github.com/), and further explained in [“A step-by-step guide to Git”](https://opensource.com/article/18/1/step-step-guide-git) by Kedar Vijay Kulkarn on Opensource.com.
- The explanation of how to list files in Git was introduced to me by [an answer on Stack Overflow by karlphillip](https://stackoverflow.com/questions/8533202/list-files-in-local-git-repo/8533413#8533413).
- The importance of starting a repository with a `README.md`, `LICENSE.md`, and `.gitignore` file was introduced to me by the default repository instructions on [GitHub](https://github.com/).
- The recommendation to write single-line Git commit messages using [imperative mood](https://en.wikipedia.org/wiki/Imperative_mood), to start them with a capital letter, and to end them without a period was introduced to me by [a page on the GitHub Erlang/OTP wiki](https://github.com/erlang/otp/wiki/writing-good-commit-messages).

[^usngGit1]: https://github.com/erlang/otp/wiki/writing-good-commit-messages
