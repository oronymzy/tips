# replacing [non-breaking spaces] in a text file

!!! note
    
    - {==foo.txt==} represents the input file containing at least one non-breaking space.
    - {==bar.txt==} represents the output file not containing any non-breaking spaces.

Isolate the suspected non-breaking space in `foo.txt`, then use `cat foo.txt | perl -C7 -ne 'for(split(//)){print sprintf("U+%04X", ord)." ".$_."\n"}'` to view the Unicode code points for all letters in the file. Look for `U+00A0`, the Unicode code point of the non-breaking space. Because the UTF-8 equivalent is `C2` `A0`, use `sed 's/\xC2\xA0/ /g' foo.txt > bar.txt` to replace all non-breaking spaces with ordinary spaces.

## licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Includes significant content from [a question](https://superuser.com/questions/377793/view-unicode-codepoints-for-all-letters-in-file-on-bash/) and [answer on Super User by Karel Bílek](https://superuser.com/questions/377793/view-unicode-codepoints-for-all-letters-in-file-on-bash/377805#377805), with changes made.

## prior work
- The method of replacing all non-breaking spaces with ordinary spaces was introduced to me by [an answer on Super User by Thor](https://superuser.com/questions/517847/use-sed-to-replace-nbsp-160-hex-00a0-octal-240-non-breaking-space/517852#517852).
- The method of viewing the Unicode code points for all letters in a file was introduced to me by [an answer on Super User by Karel Bílek](https://superuser.com/questions/377793/view-unicode-codepoints-for-all-letters-in-file-on-bash/377805#377805).
- The Unicode and UTF-8 code points were introduced to me by [Non-breaking space§Encodings](https://en.wikipedia.org/wiki/Non-breaking_space#Encodings) on Wikipedia.

[non-breaking spaces]: https://en.wikipedia.org/wiki/Non-breaking_space
