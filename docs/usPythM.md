# using [Python-Markdown]

!!! bug
    
    [Attribute Lists](https://python-markdown.github.io/extensions/attr_list/) behave oddly within pipe tables.
    - If an attribute is applied to plain text within a table cell, such as `foo{ .bar }`, the *bar* class will be applied to the table cell. If text is added after the attribute, such as `foo{ .bar } baz`, then *baz* will not appear, but one or more reference style links, such as `foo{ .bar } [baz]`, *will* appear.
    - It does not apply the *foo* class to a table cell containing `{ .foo } [bar] (baz)`, where *bar* has a working link definition.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[Python-Markdown]: https://python-markdown.github.io/
