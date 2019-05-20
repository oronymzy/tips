# getting the source text
## getting the [Markdown]-formatted source text of a [Stack Exchange] answer

!!! attention
    
    The source text may include [ASCII control characters](https://en.wikipedia.org/wiki/Control_character#In_ASCII) and [HTML character entity references](https://en.wikipedia.org/wiki/List_of_XML_and_HTML_character_entity_references#Character_entity_references_in_HTML). It is possible to [convert the HTML character entity references to UTF-8 characters](cnvcenc.md#HTMLcertoUTF8).

!!! info
    
    - {==foo==} represents the answer identifier, for example `1732454`.
    - {==bar==} represents the answer site, for example `stackoverflow`.

Use `http://api.stackexchange.com/2.2/answers/foo?order=desc&sort=activity&site=bar&filter=!.UDo6l2ikDi7iGlf`.

## prior work
- The method of getting the source text of a [Stack Exchange] answer was introduced to me by [an answer on Meta Stack Exchange by user259867](https://meta.stackexchange.com/questions/264295/stack-exchange-api-get-answers-markdown/264298#264298).

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[Markdown]: https://en.wikipedia.org/wiki/Markdown
[Stack Exchange]: https://en.wikipedia.org/wiki/Stack_Exchange
