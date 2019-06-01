# using transput connections
## using [standard streams]

!!! note
    
    - {==foobar==} represents a [command] that may produce content in [stdout] and [stderr].
    - {==barbaz.txt==} represents an output text file containing the contents of [stdout] and [stderr].

Use `foobar 2>&1 | tee barbaz.txt` to do the following things with the contents of [stdout] and [stderr]:

1. write them to a file
2. display them on the console

## prior work
The method of writing the contents of [stdout] and [stderr] to a file while also displaying the contents of [stdout] and [stderr] on the console was introduced to me by [an answer on Ask Ubuntu by Seth](https://askubuntu.com/questions/420981/how-do-i-save-terminal-output-to-a-file/420983#420983).

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[command]: https://en.wikipedia.org/wiki/Command_(computing)
[standard streams]: https://en.wikipedia.org/wiki/Standard_streams
[stdout]: https://en.wikipedia.org/wiki/Standard_streams#Standard_output_(stdout)
[stderr]: https://en.wikipedia.org/wiki/Standard_streams#Standard_error_(stderr)
