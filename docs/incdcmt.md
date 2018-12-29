# including code comments

??? warning "Protologism ahead"
    
    This is a [protologistic](https://en.wikipedia.org/wiki/Protologism) [compound word](https://en.wiktionary.org/wiki/compound_word) I have created out of the following need:
    
    - In my experience, a **[comment](https://en.wikipedia.org/wiki/Comment_(computer_programming))** in the context of writing computer instructions is not just a <q>programmer-readable explanation or annotation</q> and can be found in more places than just <q>the source code of a computer program</q>.
    
    It is based on [Wikipedia's definition of comment (computer programming)](https://en.wikipedia.org/wiki/Comment_(computer_programming)):
    > In [computer programming](https://en.wikipedia.org/wiki/Computer_programming), a **comment** is a programmer-readable explanation or *[annotation](https://en.wikipedia.org/wiki/Annotation)* in the [source code](https://en.wikipedia.org/wiki/Source_code) of a [computer program](https://en.wikipedia.org/wiki/Computer_program). They are added with the purpose of making the source code easier for humans to understand, and are generally ignored by [compilers](https://en.wikipedia.org/wiki/Compiler) and [interpreters](https://en.wikipedia.org/wiki/Interpreter_(computing)).[^incdcmt1] [^incdcmt2]
    
    *Code* refers to any kind of computer instructions, and is based on [one of Wiktionary's definitions of *code*](https://en.wiktionary.org/wiki/code#Noun):
    > ([programming](https://en.wiktionary.org/wiki/programming#Noun), [uncountable](https://en.wiktionary.org/wiki/Appendix:Glossary#uncountable)). Instructions for a [computer](https://en.wiktionary.org/wiki/computer), written in a [programming language](https://en.wiktionary.org/wiki/programming_language); the [input](https://en.wiktionary.org/wiki/input) of a [translator](https://en.wiktionary.org/wiki/translator), an [interpreter](https://en.wiktionary.org/wiki/interpreter) or a [browser](https://en.wiktionary.org/wiki/browser), namely: [source code](https://en.wiktionary.org/wiki/source_code), [machine code](https://en.wiktionary.org/wiki/machine_code), [bytecode](https://en.wiktionary.org/wiki/bytecode).
    
    *Source code* refers to any set of computer instructions before they are carried out, including HTML[^incdcmt3].

A *code comment* is any textual material relevant to and included with computer instructions that is intended to be omitted or hidden when those instructions are carried out.

## [CSS code comments]
Use `/* foobar */`, where *foobar* is the code comment. The strings `/*` and `*/` surround one or more lines of text to make a code comment. CSS code comments may not be nested[^incdcmt4], and it is not valid CSS to indicate a comment with only the string `//` at the beginning of a line[^incdcmt5].

## [HTML code comments]
Use `<!-- foobar -->`, where *foobar* is the code comment. The strings `<!--` and `-->` surround one or more lines of text to make a code comment. HTML comments are ignored by the browser and are usually invisible to the user, but they can be viewed [in Firefox](https://developer.mozilla.org/en-US/docs/Tools/View_source) or [Google Chrome](https://support.google.com/surveys/answer/6172725?hl=en) using the ++"view source"++ tool.

## formats lacking support for code comments

- [JSON](https://json.org/)

## licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Includes significant content from:

- [code](https://en.wiktionary.org/w/index.php?title=code&oldid=51126382) on Wiktionary, with changes made.
- [Comment (computer programming)](https://en.wikipedia.org/w/index.php?title=Comment_(computer_programming)&oldid=875338006) on Wikipedia, with changes made.
- [Getting started with HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started$revision/1436132) by Mozilla Contributors, with changes made, including rewording things to eliminate the need for em dashes. **Originally licensed [CC BY-SA 2.5](https://creativecommons.org/licenses/by-sa/2.5/) or later.**
- [HTML element§Comments](https://en.wikipedia.org/w/index.php?title=HTML_element&oldid=874852200) on Wikipedia, with changes made.

## prior work
The fact that JSON does not support comments was introduced to me by [an answer on Stack Overflow by Eli](https://stackoverflow.com/questions/244777/can-comments-be-used-in-json/244858#244858).

[^incdcmt1]: Source code can be divided into *program code* (which consists of machine-translatable instructions); and *comments* (which include human-readable notes and other kinds of annotations in support of the program code).Penny Grubb, Armstrong Takang (2003). *Software Maintenance: Concepts and Practice*. World Scientific. pp. 7, plese start120--121. [ISBN](https://en.wikipedia.org/wiki/International_Standard_Book_Number) [981-238-426-X](https://en.wikipedia.org/wiki/Special:BookSources/981-238-426-X).
[^incdcmt2]: For purposes of this article, programming language comments are treated as indistinct from comments that appear in [markup languages](https://en.wikipedia.org/wiki/Markup_language), [configuration files](https://en.wikipedia.org/wiki/Configuration_file) and other similar contexts. Moreover, markup language is often closely integrated with programming language code, especially in the context of [code generation](https://en.wikipedia.org/wiki/Automatic_programming). See e.g., Ganguli, Madhushree (2002). *Making Use of Jsp*. New York: Wiley. [ISBN](https://en.wikipedia.org/wiki/International_Standard_Book_Number) [0-471-21974-6](https://en.wikipedia.org/wiki/Special:BookSources/0-471-21974-6).
[^incdcmt3]: https://support.google.com/surveys/answer/6172725?hl=en
[^incdcmt4]: https://www.w3.org/TR/CSS21/syndata.html#comments
[^incdcmt5]: https://stackoverflow.com/questions/11218808/do-double-forward-slashes-direct-ie-to-use-specific-css/11218889#11218889

[CSS code comments]: https://developer.mozilla.org/en-US/docs/Web/CSS/Comments
[HTML code comments]: https://en.wikipedia.org/wiki/HTML_element#Comments
