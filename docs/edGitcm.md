# editing a [Git] commit message

!!! note
    
    - {==foobar==} represents the forty-character commit object name of the commit to be edited.

Make sure all unstaged changes are committed or stashed, then use `git rebase -i foobar^` to open the default text editor with a list of commits. Using the first seven digits of the forty-character commit object name, identify the line with the commit message to be edited, then change the default `pick` action to `reword`. Save the file and quit the text editor. The editor will then be reopened with an option to edit the specified commit message. Edit the commit message, then save the file and quit the text editor. The command prompt will reappear, and a new tree will exist with the updated message.

## licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Includes significant content from [an answer on Stack Overflow by Mureinik](https://superuser.com/questions/751699/is-there-a-way-to-edit-a-commit-message-in-github/751909#751909), with changes made.

[Git]: https://git-scm.com/
