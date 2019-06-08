# listing all files containing specific text

!!! note
    
    - {==/foo/bar/==} represents a directory to recursively search within.
    - {==baz==} represents the text to search for.

Use `grep -inr '/foo/bar/' -e 'baz'`.

## explanation

- The `-e` [option](https://www.gnu.org/software/grep/manual/grep.html#Matching-Control-1) specifies a regular expression.
- The `-i` [option](https://www.gnu.org/software/grep/manual/grep.html#Matching-Control-1) disables case sensitivity.
- The `-n` [option](ttps://www.gnu.org/software/grep/manual/grep.html#Output-Line-Prefix-Control-1) prefixes each outputted line with a line number.
- The `-r` [option](https://www.gnu.org/software/grep/manual/grep.html#File-and-Directory-Selection-1) enables recursion.

## prior work
- The wording of the title comes from [a question on Stack Overflow by Nathan](https://stackoverflow.com/questions/16956810/how-do-i-find-all-files-containing-specific-text-on-linux/).
- The bulk of the script explanation comes from [an answer on Stack Overflow by rakib_](https://stackoverflow.com/questions/16956810/how-do-i-find-all-files-containing-specific-text-on-linux/16957078#16957078).

## licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Includes significant content from [a question on Stack Overflow by Nathan](https://stackoverflow.com/questions/16956810/how-do-i-find-all-files-containing-specific-text-on-linux/) and [an answer on Stack Overflow by rakib_](https://stackoverflow.com/questions/16956810/how-do-i-find-all-files-containing-specific-text-on-linux/16957078#16957078) with changes made, including converting the original HTML to Markdown.
