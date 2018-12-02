# using [pup]
To extract the URLs from one or more links based on their [anchor text](https://en.wikipedia.org/wiki/Anchor_text), use `pup -f foobar.html ':contains("baz") attr{href}'`, where *foobar.html* is the HTML source file containing the links and *baz* is the anchor text.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The availability of a `contains()` pseudo class was introduced to me by [the Pseudo Classes section of the pup README on GitHub](https://github.com/ericchiang/pup#pseudo-classes).
- The possibility of extracting the value of an `href` attribute from an anchor element was introduced to me by [the attr{attrkey} section of the pup README on GitHub](https://github.com/ericchiang/pup#attrattrkey).

[pup]: https://github.com/ericchiang/pup
