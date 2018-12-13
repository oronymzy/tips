# listing all files containing specific text
Use `grep -rnw '/foo/bar/' -e 'baz'`, where */foo/bar/* is the directory to recursively search within, and *baz* is the text to search for.

## explanation

- `-r` or `-R` enables recursion
- `-n` prefixes each outputted line with a line number[^lsfctxt1]
- `-w` specifies selction of whole words[^lsfctxt2]
- `-e` specifies a pattern[^lsfctxt2]

## licensing ###
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Includes significant content from [a question on Stack Overflow by Nathan](https://stackoverflow.com/questions/16956810/how-do-i-find-all-files-containing-specific-text-on-linux/) and [an answer on Stack Overflow by rakib_](https://stackoverflow.com/questions/16956810/how-do-i-find-all-files-containing-specific-text-on-linux/16957078#16957078) with changes made, including conversion the original HTML to Markdown.

## prior work
- The wording of the title comes from [a question on Stack Overflow by Nathan](https://stackoverflow.com/questions/16956810/how-do-i-find-all-files-containing-specific-text-on-linux/).
- The bulk of the script explanation comes from [an answer on Stack Overflow by rakib_](https://stackoverflow.com/questions/16956810/how-do-i-find-all-files-containing-specific-text-on-linux/16957078#16957078).

[^lsfctxt1]: https://www.gnu.org/software/grep/manual/grep.html#Output-Line-Prefix-Control-1
[^lsfctxt2]: https://www.gnu.org/software/grep/manual/grep.html#Matching-Control-1
