# quick reference for [Markdown]

This is intended as a quick reference and showcase. For more complete info, see [John Gruber's original spec](http://daringfireball.net/projects/markdown/).

The idea is that this:

```
Why is there a `cat` command, but no *bird* command?
```

is more human-readable than this:

```
Why is there a <code>cat</code> command, but no <em>bird</em> command?
```

## admonitions {: #admonitions }

```
!!! attention
    
    Admonitions interrupt the flow of a document to communicate something contextually significant. They can be grouped into categories, and are often accompanied by specific icons and colors.
```

<div class="admonition attention">
<p class="admonition-title">Attention</p>
<p>Admonitions interrupt the flow of a document to communicate something contextually significant. They can be grouped into categories, and are often accompanied by specific icons and colors.</p>
</div>

Admonitions do not have a direct HTML equivalent, but [the *aside* element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/aside) may suffice.[^qrMkdown1] [^qrMkdown2]

!!! note
    
    A line containing just four spaces can be added to the beginning of an admonition for compatibility with Markdown implementations that do not support admonitions, causing them to be rendered as [code blocks](#bcode).

## blockquotes {: #blockquotes }

```
> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote.
```

??? tip "Result"
    
    > Blockquotes are very handy in email to emulate reply text.
    > This line is part of the same quote.
    
    Quote break.
    
    > This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote.

## code {: #code }

Code blocks are part of the Markdown spec, but syntax highlighting isn't. However, many renderers -- like Github's and *Markdown Here* -- support syntax highlighting. Which languages are supported and how those language names should be written will vary from renderer to renderer.

### inline code {: #icode }

```
Inline `code` has `back-ticks around` it.
```

??? tip "Result"
    
    Inline `code` has `back-ticks around` it.

### blocks of code {: #bcode }
 Blocks of code are fenced by lines with three back-ticks (<code>```</code>).

```
 ```javascript
 var s = "JavaScript syntax highlighting";
 alert(s);
 ```

 ```python
 s = "Python syntax highlighting"
 print s
 ```

 ```
 No language indicated, so no syntax highlighting. 
 But let's throw in a <b>tag</b>.
 ```
```

!!! note
    The raw Markdown is indented by a single space to allow nesting of a code block within a code block.

??? tip "Result"
     
     ```javascript
     var s = "JavaScript syntax highlighting";
     alert(s);
     ```
     
     ```python
     s = "Python syntax highlighting"
     print s
     ```
     
     ```
     No language indicated, so no syntax highlighting in Markdown Here (varies on Github). 
     But let's throw in a <b>tag</b>.
     ```

Alternatively, code blocks can be fenced by three tildes (`~~~`) or be indented by four spaces.

```
~~~
The quick
brown fox
~~~

    jumps over
    the lazy dog.
```

??? tip "Result"
    
    ~~~
    The quick
    brown fox
    ~~~
    
        jumps over
        the lazy dog.

## emphasis {: #emphasis }

```
Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

Combined emphasis with **asterisks and _underscores_**.
```

??? tip "Result"
    
    Emphasis, aka italics, with *asterisks* or _underscores_.
    
    Strong emphasis, aka bold, with **asterisks** or __underscores__.
    
    Combined emphasis with **asterisks and _underscores_**.

## footnotes {: #footnotes }

!!! attention
    
    Unlike most other Markdown elements, a footnote does not directly correspond with any existing HTML element.[^qrMkdown3] This means that:
    
    1. Markdown offers a more standardized way of creating footnotes than HTML.
    2. HTML renderings of footnotes will differ significantly between different implementations of Markdown.

!!! note
    
    **Footnotes usually include hyperlinks**, but because footnotes do not work within admonitions, the *Result* admonition contains raw Markdown formatted differently than in the example, with manually-added superscripts and ordered lists.

### inline-style footnote {: #ifootnote }
This style of footnote creates a self-contained footnote beside the text it references.

```
An inline-style footnote consists of a caret (`^`) outside a pair of square brackets.
It can be created on a single line^[It will be formatted like this.].
```

### reference-style footnote {: #rfootnote }
This style of footnote resembles a reference-style link, but works differently. Instead of combining into a hyperlink, the reference becomes a numbered superscript and the link definition becomes a numbered footnote at the end of the page.

```
The reference identifier[^1] is an string that begins with a caret (`^`).
A number often follows the caret, but other characters are also allowed[^character-limitations].

[^1]: In Python-Markdown, identifiers are called *labels*.
[^character-limitations]:
    Not all characters are allowed within the identifier.
    Pandoc's Markdown does not allow spaces, tabs, or newlines in the identifier.
```

??? tip "Result"
    
    The reference identifier^1^ is an string that begins with a caret (`^`).
    A number often follows the caret,
    but other characters are also allowed^2^.
    
    1. In Python-Markdown, identifiers are called *labels*.
    2. Not all characters are allowed within the identifier.
    
        Pandoc's Markdown does not allow spaces, tabs, or newlines in the identifier.

!!! attention
    
    [Python-Markdown](https://python-markdown.github.io/) expects an indentation of four spaces (or one tab) for footnotes with multiple blocks.[^qrMkdown4]

## headings {: #headings }

```
# H1
## H2
### H3
#### H4
##### H5
###### H6
```

??? tip "Result"
    
    <span class="h1workaround">H1</span>
    
    <span class="h2workaround">H2</span>
    
    <span class="h3workaround">H3</span>
    
    <span class="h4workaround">H4</span>
    
    <span class="h5workaround">H5</span>
    
    <span class="h6workaround">H6</span>

Alternatively, for H1 and H2, an underline-ish style:

```
Alt-H1
======

Alt-H2
------
```

??? tip "Result"
    
    <span class="h1workaround">Alt-H1</span>
    
    <span class="h2workaround">Alt-H2</span>

!!! note
    
    To avoid adding extraneous entries to the table of contents, several *Result* admonitions contain specially-styled HTML instead of heading elements.

## horizontal rules {: #hrule }

```
Three or more...

---

Hyphens

***

Asterisks

___

Underscores
```

??? tip "Result"
    
    Three or more...
    
    ---
    
    Hyphens
    
    ***
    
    Asterisks
    
    ___
    
    Underscores

## images {: #images }

```
Here's our logo (hover to see the title text):

Inline-style: 
![alt text](qrMkdwn.png "Logo Title Text 1")

Reference-style: 
![alt text][logo]

[logo]: qrMkdwn.png "Logo Title Text 2"
```

??? tip "Result"
    
    Here's our logo (hover to see the title text):
    
    Inline-style: 
    ![alt text](qrMkdwn.png "Logo Title Text 1")
    
    Reference-style: 
    ![alt text][logo]

[logo]: qrMkdwn.png "Logo Title Text 2"

## inline HTML {: #html }
You can also use raw HTML in your Markdown, and it'll mostly work pretty well.

```
<figure>
<img src="../qrMkdwn.png">
<figcaption>This colorful image could use a caption.<br>
Markdown in HTML does *not* work **very** well.
Use HTML <em>tags</em> <strong>instead</strong>.</figcaption>
</figure>
```

??? tip "Result"
    
    <figure>
    <img src="../qrMkdwn.png">
    <figcaption>This colorful image could use a caption.<br>
    Markdown in HTML does *not* work **very** well.
    Use HTML <em>tags</em> <strong>instead</strong>.</figcaption>
    </figure>

!!! note
    
    Because Markdown *is* rendered within HTML when inside an admonition, the *Result* admonition contains raw Markdown formatted differently than in the example, with backslash-escapes added.

## line breaks {: #lines }

!!! note
    
    Leading and trailing spaces are shown with dots (`⋅`).

Try experimenting to learn how line breaks work -- hit ++enter++ once (i.e., insert one newline), then hit it twice (i.e., insert two newlines), and see what happens.

Here are some things to try out:

``` tab="Markdown with dots"
Here's a line for us to start with.

This line is separated from the one above by two newlines, so it will be a *separate paragraph*.

This line is also a separate paragraph, but...⋅⋅
This line is separated by a single newline and two spaces, so it's a separate line in the *same paragraph*.
```

``` tab="Markdown without dots"
Here's a line for us to start with.

This line is separated from the one above by two newlines, so it will be a *separate paragraph*.

This line is also a separate paragraph, but...  
This line is separated by a single newline and two spaces, so it's a separate line in the *same paragraph*.
```

??? tip "Result"
    
    Here's a line for us to start with.
    
    This line is separated from the one above by two newlines, so it will be a *separate paragraph*.
    
    This line is also a separate paragraph, but...  
    This line is separated by a single newline and two spaces, so it's a separate line in the *same paragraph*.

!!! note
    
    Most Markdown implementations require lines on the same paragraph to be separated by **two spaces** just before the newline, but ending a line with a backslash (`\`) is also supported by [Pandoc's Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown) (with an extension)[^qrMkdown5].

It is also possible to [indicate page breaks in Markdown](ipbkMkd.md).

## links {: #links }
### automatic link {: #alink }

```
URLs in angle brackets will automatically get turned into links: <https://freedomdefined.org/Definition>.
```

??? tip "Result"
    
    URLs in angle brackets will automatically get turned into links: <https://freedomdefined.org/Definition>.

### inline-style link {: #ilink }

```
[I'm an inline-style link](https://freedomdefined.org/Definition), and
[I'm an inline-style link with a title](https://freedomdefined.org/Definition "Definition of Free Cultural Works").
```

??? tip "Result"
    
    [I'm an inline-style link](https://freedomdefined.org/Definition), and
    [I'm an inline-style link with a title](https://freedomdefined.org/Definition "Definition of Free Cultural Works").

### reference-style link {: #rlink }

```
[I'm a reference-style link][with a separate link definition], and
[I'm a reference-style link and definition all in one].

The link definition for a reference-style link is included separately, usually at the bottom of the document.

[with a separate link definition]: https://freedomdefined.org/Definition
[I'm a reference-style link and definition all in one]: https://freedomdefined.org/Definition
```

??? tip "Result"
    
    [I'm a reference-style link](https://freedomdefined.org/Definition), and
    [I'm a reference-style link and definition all in one](https://freedomdefined.org/Definition).
    
    The link definition for a reference-style link is included separately, usually at the bottom of the document.

!!! note
    
    Because reference-style links do not work within admonitions, several *Result* admonitions contain raw Markdown formatted differently than in the example, with reference-style links replaced with inline-style links.

## lists {: #lists }
### description lists {: #dlists }

```
Description lists are made of terms and details
: We don't need to go into much detail about it.

Each term and its details can represent attribute-value pairs.

Here is an attribute.
: And here is a value.
: It starts with a colon.
```

??? tip "Result"
    
    Description lists are made of terms and details
    : We don't need to go into much detail about it.
    
    Each term and its details can represent attribute-value pairs.
    
    Here is an attribute.
    : And here is a value.
    : It starts with a colon.

### ordered lists {: #olists }

!!! note
    
    Leading and trailing spaces are shown with dots (`⋅`).

``` tab="Markdown with dots"
1. First ordered list item
2. Another item
⋅⋅⋅⋅* Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
⋅⋅⋅⋅1. Ordered sub-list
4. And another item.

⋅⋅⋅⋅You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces.
⋅⋅⋅⋅
⋅⋅⋅⋅To have a line break without a paragraph, you will need to use two trailing spaces.⋅⋅
⋅⋅⋅⋅Note that this line is separate, but within the same paragraph.
```

``` tab="Markdown without dots"
1. First ordered list item
2. Another item
    * Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
    1. Ordered sub-list
4. And another item.

    You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces.
    
    To have a line break without a paragraph, you will need to use two trailing spaces.
    Note that this line is separate, but within the same paragraph.
```

??? tip "Result"
    
    1. First ordered list item
    2. Another item
        * Unordered sub-list. 
    1. Actual numbers don't matter, just that it's a number
        1. Ordered sub-list
    4. And another item.
    
        You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces.
        
        To have a line break without a paragraph, you will need to use two trailing spaces.
        Note that this line is separate, but within the same paragraph.

!!! attention
    
    [Python-Markdown](https://python-markdown.github.io/) expects an indentation of four spaces (or one tab) for nested block level elements, which includes lists and sub-lists.[^qrMkdown6]

### unordered lists {: #ulists }

```
* Unordered list can use asterisks
- Or minuses
+ Or pluses
```

??? tip "Result"
    
    * Unordered list can use asterisks
    - Or minuses
    + Or pluses

## strikethrough {: #strikethrough }

```
Strikethrough uses two tildes. ~~Scratch this.~~
```

??? tip "Result"
    
    Strikethrough uses two tildes. ~~Scratch this.~~

## tables {: #tables }

Tables aren't part of the core Markdown spec, but they are part of GFM and *Markdown Here* supports them. They are an easy way of adding tables -- a task that would otherwise require copy-pasting from another application.

```
Colons can be used to align columns.

| Tables        | Are           | Cool  |
|---------------|:-------------:|------:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |
```

??? tip "Result"
    
    Colons can be used to align columns.
    
    | Tables        | Are           | Cool  |
    |---------------|:-------------:|------:|
    | col 3 is      | right-aligned | $1600 |
    | col 2 is      | centered      |   $12 |
    | zebra stripes | are neat      |    $1 |

The table will render correctly even if the raw Markdown does not line up prettily. The rightmost pipe (`|`) and any extra spaces can be omitted. Only one dash is required to separate each header cell. You can also use inline Markdown.
```
| Markdown | Less | Pretty
|-|-|-
| *Still* | `renders` | **nicely**
| 1 | 2 | 3
```

??? tip "Result"
    
    | Markdown | Less | Pretty
    |-|-|-
    | *Still* | `renders` | **nicely**
    | 1 | 2 | 3

## comparison of Markdown implementations

<!-- This table depends on CSS tweaks to display correctly. -->

|                                                                     | [GitHub Flavored Markdown]                                              | [John Gruber’s Markdown]                     | [Pandoc's Markdown]                     | [PyMdown]                                       | [Python-Markdown]                       |
|:--------------------------------------------------------------------|:------------------------------------------------------------------------|:---------------------------------------------|:----------------------------------------|:------------------------------------------------|:----------------------------------------|
|{: .fth } [admonitions]                                              | no{: .no }                                                              | no{: .no }                                   | no{: .no }                              | no{: .no }                                      | yes (with extension){: .yes }[^pynadmo] |
|{: .fth } [blockquotes]                                              | yes{: .yes}[^gfmblkq]                                                   | yes{: .yes }[^jgmblkq]                       | yes{: .yes }[^pdmblkq]                  | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [code]  [(inline)][inline code]                            | yes{: .yes}[^gfmcodi]                                                   | yes{: .yes }[^jgmcodi]                       | yes{: .yes }[^pdmcodi]                  | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [code]  [(blocks)][blocks of code]                         | yes{: .yes}[^gfmcodb]                                                   | partial (indent only){: .partial }[^jgmcodb] | yes (with extension){: .yes }[^pdmcodb] | yes (with extension){: .yes }[^pymexra]         | yes (with extension){: .yes }[^pyncodb] |
|{: .fth } [emphasis]                                                 | yes{: .yes}[^gfmemph]                                                   | yes{: .yes }[^jgmemph]                       | yes{: .yes }[^pdmemph]                  | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [footnotes]  [(inline-style)][inline-style footnote]       | no{: .no }                                                              | no{: .no }                                   | yes (with extension){: .yes }[^pdmftnt] | partial (with extension){: .partial }[^pymfnis] | no{: .no }[^pynfnis]                    |
|{: .fth } [footnotes]  [(reference-style)][reference-style footnote] | no{: .no }                                                              | no{: .no }                                   | yes (with extension){: .yes }[^pdmftnt] | yes (with extension){: .yes }[^pymexra]         | yes (with extension){: .yes }[^pynfnrs] |
|{: .fth } [headings]                                                 | yes{: .yes }[^gfmhdng]                                                  | yes{: .yes }[^jgmhdng]                       | yes{: .yes }[^pdmhdng]                  | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [horizontal rules]                                         | yes{: .yes }[^gfmhzrl]                                                  | yes{: .yes }[^jgmhzrl]                       | yes{: .yes }[^pdmhzrl]                  | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [images]                                                   | yes{: .yes }[^gfmimag]                                                  | yes{: .yes }[^jgmimag]                       | yes{: .yes }[^pdmimag]                  | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [inline HTML]                                              | partial (some tags are filtered out){: .partial } [^gfmhtm1] [^gfmhtm2] | yes{: .yes }[^jgmhtml]                       | yes (with extension){: .yes }[^pdmhtml] | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [links]  [(automatic)][automatic link]                     | yes{: .yes }[^gfmlka1] [^gfmlka2]                                       | yes{: .yes }[^jgmlkao]                       | yes{: .yes }[^pdmlkao]                  | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [links]  [(inline-style)][inline-style link]               | yes{: .yes }[^gfmlkis]                                                  | yes{: .yes }[^jgmlink]                       | yes{: .yes }[^pdmlkis]                  | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [links]  [(reference-style)][reference-style link]         | yes{: .yes }[^gfmlkrs]                                                  | yes{: .yes }[^jgmlink]                       | yes{: .yes }[^pdmlkrs]                  | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [lists]  [(description lists)][description lists]          | no{: .no }                                                              | no{: .no }                                   | yes (with extension){: .yes }[^pdmldsc] | yes (with extension){: .yes }[^pymexra]         | yes (with extension){: .yes }[^pynldsc] |
|{: .fth } [lists]  [(ordered lists)][ordered lists]                  | yes{: .yes }[^gfmlist]                                                  | yes{: .yes }[^jgmlist]                       | yes{: .yes }[^pdmlord]                  | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [lists]  [(unordered lists)][unordered lists]              | yes{: .yes }[^gfmlist]                                                  | yes{: .yes }[^jgmlist]                       | yes{: .yes }[^pdmlurd]                  | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [strikethrough]                                            | yes (with extension){: .yes }[^gfmstrk]                                 | no{: .no }                                   | yes (with extension){: .yes }[^pdmstrk] | yes (with extension){: .yes }[^pymtlde]         | no{: .no }                              |
|{: .fth } [tables]                                                   | yes (with extension){: .yes }[^gfmtabl]                                 | no{: .no }                                   | yes (with extension){: .yes }[^pdmtabl] | yes (with extension){: .yes }[^pymexra]         | yes (with extension){: .yes }[^pyntabl] |

[admonitions]: #admonitions
[automatic link]: #alink
[blockquotes]: #blockquotes
[blocks of code]: #bcode
[code]: #code
[description lists]: #dlists
[emphasis]: #emphasis
[footnotes]: #footnotes
[headings]: #headings
[horizontal rules]: #hrule
[images]: #images
[inline-style footnote]: #ifootnote
[inline-style link]: #ilink
[inline code]: #icode
[inline HTML]: #html
[links]: #links
[lists]: #lists
[ordered lists]: #olists
[reference-style footnote]: #rfootnote
[reference-style link]: #rlink
[strikethrough]: #strikethrough
[tables]: #tables
[unordered lists]: #ulists
[GitHub Flavored Markdown]: https://github.github.com/gfm/
[John Gruber’s Markdown]: https://daringfireball.net/projects/markdown/syntax
[Pandoc's Markdown]: https://pandoc.org/MANUAL.html#pandocs-markdown
[PyMdown]: https://facelessuser.github.io/PyMdown/
[Python-Markdown]: https://python-markdown.github.io/
[^gfmblkq]: https://github.github.com/gfm/#block-quotes
[^gfmcodb]: https://github.github.com/gfm/#fenced-code-blocks
[^gfmcodi]: https://github.github.com/gfm/#code-spans
[^gfmemph]: https://github.github.com/gfm/#emphasis-and-strong-emphasis
[^gfmhdng]: https://github.github.com/gfm/#atx-headings
[^gfmhzrl]: https://github.github.com/gfm/#thematic-break
[^gfmimag]: https://github.github.com/gfm/#images
[^gfmhtm1]: https://github.github.com/gfm/#raw-html
[^gfmhtm2]: https://github.github.com/gfm/#disallowed-raw-html-extension-
[^gfmlka1]: https://github.github.com/gfm/#autolink
[^gfmlka2]: https://github.github.com/gfm/#autolinks-extension-
[^gfmlkis]: https://github.github.com/gfm/#links
[^gfmlkrs]: https://github.github.com/gfm/#link-reference-definitions
[^gfmlist]: https://github.github.com/gfm/#lists
[^gfmstrk]: https://github.github.com/gfm/#strikethrough-extension-
[^gfmtabl]: https://github.github.com/gfm/#tables-extension-
[^jgmblkq]: https://daringfireball.net/projects/markdown/syntax#blockquote
[^jgmcodi]: https://daringfireball.net/projects/markdown/syntax#code
[^jgmcodb]: https://daringfireball.net/projects/markdown/syntax#precode
[^jgmemph]: https://daringfireball.net/projects/markdown/syntax#em
[^jgmhdng]: https://daringfireball.net/projects/markdown/syntax#header
[^jgmhtml]: https://daringfireball.net/projects/markdown/syntax#html
[^jgmhzrl]: https://daringfireball.net/projects/markdown/syntax#hr
[^jgmimag]: https://daringfireball.net/projects/markdown/syntax#img
[^jgmlink]: https://daringfireball.net/projects/markdown/syntax#link
[^jgmlist]: https://daringfireball.net/projects/markdown/syntax#list
[^jgmlkao]: https://daringfireball.net/projects/markdown/syntax#autolink
[^pymexra]: https://facelessuser.github.io/pymdown-extensions/extensions/extra/
[^pymfnis]: Inline-style footnotes can be approximated using the [Caret extension](https://facelessuser.github.io/pymdown-extensions/extensions/caret/) to create numbered superscripts and an ordered list. Links between the superscript and footnote will not be available.
[^pynadmo]: https://python-markdown.github.io/extensions/admonition/
[^pymtlde]: https://facelessuser.github.io/pymdown-extensions/extensions/tilde/
[^pyncodb]: https://python-markdown.github.io/extensions/fenced_code_blocks/
[^pynfnis]: https://github.com/Python-Markdown/markdown/issues/658
[^pynfnrs]: https://python-markdown.github.io/extensions/footnotes/
[^pynldsc]: https://python-markdown.github.io/extensions/definition_lists/
[^pyntabl]: https://python-markdown.github.io/extensions/tables/
[^pdmblkq]: https://pandoc.org/MANUAL.html#block-quotations
[^pdmcodi]: https://pandoc.org/MANUAL.html#verbatim
[^pdmcodb]: https://pandoc.org/MANUAL.html#verbatim-code-blocks
[^pdmemph]: https://pandoc.org/MANUAL.html#emphasis
[^pdmftnt]: https://pandoc.org/MANUAL.html#footnotes
[^pdmhdng]: https://pandoc.org/MANUAL.html#headers
[^pdmhtml]: https://pandoc.org/MANUAL.html#raw-html
[^pdmhzrl]: https://pandoc.org/MANUAL.html#horizontal-rules
[^pdmimag]: https://pandoc.org/MANUAL.html#images
[^pdmldsc]: https://pandoc.org/MANUAL.html#definition-lists
[^pdmlkao]: https://pandoc.org/MANUAL.html#automatic-links
[^pdmlkis]: https://pandoc.org/MANUAL.html#inline-links
[^pdmlkrs]: https://pandoc.org/MANUAL.html#reference-links
[^pdmlord]: https://pandoc.org/MANUAL.html#ordered-lists
[^pdmlurd]: https://pandoc.org/MANUAL.html#bullet-lists
[^pdmstrk]: https://pandoc.org/MANUAL.html#strikeout
[^pdmtabl]: https://pandoc.org/MANUAL.html#tables

## licensing
**Some rights reserved: [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/).** Includes significant content from [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) on GitHub with modifications, including the following:

!!! attention
    
    These are just the changes made prior to the first Git commit.

- Changed attribute formatting.
- Removed at least one reference to Markdown Here and Github-flavored Markdown.
- Removed table of contents.
- Removed secton on YouTube videos.
- Substituted the original [Markdown Here](https://github.com/adam-p/markdown-here) logo with the [Definition of Free Cultural Works](https://en.wikipedia.org/wiki/Definition_of_Free_Cultural_Works) [logo](https://commons.wikimedia.org/wiki/File:Definition_of_Free_Cultural_Works_logo_notext.svg), which was released under a public domain dedication.
- Tweaked the less pretty Markdown table.

??? info "Additional removals"
    
    - {--"Markdown Toggle" is your friend.--}
    - {--(Technical note: *Markdown Here* uses GFM line breaks, so there's no need to use MD's two-space line breaks.)--}
    - {--(This is contrary to the typical GFM line break behaviour, where trailing spaces are not required.)--}
    - {--*Markdown Here* supports highlighting for dozens of languages (and not-really-languages, like diffs and HTTP headers); to see the complete list, and how to write the language names, see the [highlight.js demo page](http://softwaremaniacs.org/media/soft/highlight/test.html).--}
    - {--I recommend only using the fenced code blocks -- they're easier and only they support syntax highlighting.--}
    - {--License: [CC-BY](https://creativecommons.org/licenses/by/3.0/)--}
    - {--Referencing a bug by #bugID in your git commit links it to the slip. For example #1.--}
    - {--You'll soon learn to get what you want.--}

??? info "Additional substitutions"
    
    - {~~(In this example, leading and trailing spaces are shown with with dots: `⋅`)~>Leading and trailing spaces are shown with dots (`⋅`).~~}
    - {~~&lt;Enter&gt;~>++enter++~~}
    - {~~My basic recommendation for learning how line breaks work is to experiment and discover -- hit ++enter++ once (i.e., insert one newline), then hit it twice (i.e., insert two newlines), see what happens. You'll soon learn to get what you want.~>Try experimenting to learn how line breaks work -- hit ++enter++ once (i.e., insert one newline), then hit it twice (i.e., insert two newlines), and see what happens. You'll soon learn to get what you want.~~}
    - {~~Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).~>Notice the blank line above, and the leading spaces.~~}
    - {~~There must be at least 1 dash separating each header cell. The rightmost pipe (`|`) is optional, and you don't need to make the raw Markdown line up prettily. You can also use inline Markdown.~>The table will render correctly even if the raw Markdown does not line up prettily. The rightmost pipe (`|`) and any extra spaces can be omitted, and only one dash is required to separate each header cell. You can also use inline Markdown.~~}
    - {~~There must be at least 3 dashes separating each header cell.~>There must be at least 1 dash separating each header cell.~~}
    - {~~They are an easy way of adding tables to your email -- a task that would otherwise require copy-pasting from another application.~>They are an easy way of adding tables -- a task that would otherwise require copy-pasting from another application.~~}
    - {~~The outer pipes (|) are optional~>The rightmost pipe (`|`) is optional~~}
    - {~~This line is only separated by a single newline, so it's a separate line in the *same paragraph*.~>This line is separated by a single newline and two spaces, so it's a separate line in the *same paragraph*.~~}

## prior work
- The bulk of the instructions were introduced to me through [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet), part of the [Markdown Here](https://github.com/adam-p/markdown-here) [wiki](https://github.com/adam-p/markdown-here/wiki) on GitHub.
- The HTML versions of the Markdown examples were produced with [pandoc](https://pandoc.org/), except for [admonitions](#admonitions), which was produced with MkDocs.

[Markdown]: https://en.wikipedia.org/wiki/Markdown
[^jgmblkq]: https://daringfireball.net/projects/markdown/syntax#blockquote
[^qrMkdown1]: https://stackoverflow.com/questions/7579826/which-semantic-html-tag-for-displaying-side-notes-and-admonitions/7579894#7579894
[^qrMkdown2]: https://stackoverflow.com/questions/7579826/which-semantic-html-tag-for-displaying-side-notes-and-admonitions/8297157#8297157
[^qrMkdown3]: https://en.wikipedia.org/wiki/Note_(typography)#HTML
[^qrMkdown4]: https://python-markdown.github.io/extensions/footnotes/#syntax
[^qrMkdown5]: https://pandoc.org/MANUAL.html#paragraphs
[^qrMkdown6]: https://python-markdown.github.io/#differences

