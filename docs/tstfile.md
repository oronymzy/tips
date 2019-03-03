# testing for the existence of a file

In Ubuntu, the [`test`](https://en.wikipedia.org/wiki/Test_(Unix)) command can be used to test for the existence of a file. For example, the following script uses `test` and an if-construct to test for the existence of a file named {==foo.bar==}:

`FNAME="foo.bar" ; if test ! -s "$FNAME" ; then echo "$FNAME does not exist or is empty." ; else echo "$FNAME exists." ; fi`

### explanation

!!! note
    
    This is an incomplete explanation.

- The `test ! -s "$FNAME"` [command](https://en.wikipedia.org/wiki/Test_(Unix)) tests for the existence of a file with a name stored in the `$FNAME` variable, returning true if the filename exists. This directs the script's control flow to either show a message indicating that the file does not exist or is empty, or show a message indicating that the file exists.

## prior work
- The `test` command was introduced to me by [a comment on a question I asked on Stack Overflow by fmw42](https://stackoverflow.com/questions/53981630/can-imagemagick-be-prevented-from-overwriting-an-existing-image#comment94802728_53981630).
- The bulk of the contents of the script's if-construct was introduced to me by [the test (Unix)§Examples page on Wikipedia](https://en.wikipedia.org/wiki/Test_(Unix)#Examples).
- The correct syntax for the if-contruct was introduced to me by [an answer on Stack Overflow by Shawn Chin](https://stackoverflow.com/questions/4986109/inline-if-shell-script/4986141#4986141).

## licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Includes significant content from [test (Unix)§Examples](https://en.wikipedia.org/w/index.php?title=Test_(Unix)&oldid=884867993#Examples) on Wikipedia, with changes made.
