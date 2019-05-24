# exporting data from [Wikisource]
## exporting text using [WSexport]

Open [WSexport on Toolforge](https://tools.wmflabs.org/wsexport/tool/book.php) and locate the [text box](https://developer.mozilla.org/en-US/docs/Mozilla/Tech/XUL/textbox) [labelled](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label) `Title of the page`, then enter the [post-endmost-slash path component](glossry.md#postendmostslashpathcomponentdef) of the relevant page, for example `On_the_Origin_of_Species_(1859)`.

??? info "Additional options"
    
    - For the [drop-down list](https://en.wikipedia.org/wiki/Drop-down_list) [labelled](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label) `File format`, select `txt (in beta)` or `htmlz (zip archive with an html file inside, in beta)` instead of the default `epub 3`.
    - Select the [checkbox](https://en.wikipedia.org/wiki/Checkbox) [labelled](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label) `Do not include images`.

Press the ++"Export"++ button.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[Wikisource]: https://en.wikisource.org/wiki/Main_Page
[WSexport]: https://wikisource.org/wiki/Wikisource:WSexport
