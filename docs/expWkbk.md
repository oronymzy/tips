# exporting data from [Wikibooks]
## collecting multiple pages for exporting using *[Special:Allpages]*
Open [Special:Allpages] and locate the [text box](https://developer.mozilla.org/en-US/docs/Mozilla/Tech/XUL/textbox) [labelled](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label) `Display pages starting at:`, and enter the [post-endmost-slash path component](glossry.md#postendmostslashpathcomponentdef) of the relevant page, for example `Git`. For the [drop-down list](https://en.wikipedia.org/wiki/Drop-down_list) [labelled](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label) `Namespace:`, select `(Main)`. Press the ++"Go"++ button. This will produce a list of available pages with URLs starting with the post-endmost-slash path component. These pages are probably related, and can be copied into a separate document. The page's URL will be similar to `https://en.wikibooks.org/wiki/Special:AllPages?from=Git&to=&namespace=0`.

## exporting one or more pages using *[Special:Export]*
The [Special:Export] page can be used to produce an XML file with MediaWiki-formatted text inside it. Open [Special:Export] and locate the [text box](https://developer.mozilla.org/en-US/docs/Mozilla/Tech/XUL/textbox) [labelled](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label) `Add pages manually:`. Enter any relevant pages' [post-endmost-slash path components](glossry.md#postendmostslashpathcomponentdef) into the text box. Select the [checkboxes](https://en.wikipedia.org/wiki/Checkbox) [labelled](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label) `Include only the current revision, not the full history` and `Save as file`, and press the ++"Export"++ button.

## prior work
- The method of collecting multiple pages for exporting using *Special:Allpages* was introduced to me by [the “Help:Export§Using 'Special:Export'” page](https://en.wikibooks.org/wiki/Help:Export#Using_'Special:Export') on Wikibooks.
- The method of exporting one or more pages using *Special:Export* was introduced to me by [the “Help:Export§Using 'Special:Export'” page](https://en.wikibooks.org/wiki/Help:Export#Using_'Special:Export') on Wikibooks.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[Special:Allpages]: https://en.wikibooks.org/wiki/Special:AllPages
[Special:Export]: https://en.wikibooks.org/wiki/Special:Export
[Wikibooks]: https://en.wikibooks.org/wiki/Main_Page
