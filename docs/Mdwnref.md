# [Markdown] reference

The idea is that this:

```
Why is there a `cat` command, but no *bird* command?
```

is more human-readable than this:

```
Why is there a <code>cat</code> command, but no <em>bird</em> command?
```

??? note
    
    - The HTML versions of the Markdown examples were produced with [pandoc](https://pandoc.org/), except for the [admonition](#admonition) and [attribute list](#alist) sections, which were produced with MkDocs, and a result in *blocks of code*, which was left as raw Markdown in order to produce syntax highlighting. For results with only one paragraph, HTML paragraph tags have been removed.
    - The HTML results of the Markdown examples are presented inside [admonitions without an icon or title](https://squidfunk.github.io/mkdocs-material/extensions/admonition/#removing-the-title), and with [admonitions](#admonition) this is accomplished with an extra nested `<div>` element. To avoid adding extraneous entries to the table of contents[^Mdwnref1], several [heading](#heading) admonitions contain specially-styled HTML instead of heading elements.

## admonition {: #admonition }

``` tab="Markdown"
!!! attention
    
    An admonition interrupts the flow of a document to communicate something contextually significant. Admonitions can be grouped into categories, and are often accompanied by specific icons and colors.
```

``` tab="HTML"
<div class="admonition attention">
<p class="admonition-title">Attention</p>
<p>An admonition interrupts the flow of a document to communicate something contextually significant. Admonitions can be grouped into categories, and are often accompanied by specific icons and colors.</p>
</div>
```

<div class="admonition note">
<div class="admonition attention">
<p class="admonition-title">Attention</p>
<p>An admonition interrupts the flow of a document to communicate something contextually significant. Admonitions can be grouped into categories, and are often accompanied by specific icons and colors.</p>
</div>
</div>

An admonition does not have a direct HTML equivalent. Closest in meaning is the [`<aside>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/aside) element.[^Mdwnref2] [^Mdwnref3] Admonitions [are also supported by reStructuredText](http://docutils.sourceforge.net/0.4/docs/ref/rst/directives.html#admonitions), and Wikipedia has them in the form of [article message boxes](https://en.wikipedia.org/wiki/Template:Ambox).

??? danger "Compatibility hack"
    
    ``` tab="Markdown"
    | **Note:**
    |:-
    | Because most Markdown implementations do not support admonitions, they can be approximated with tables, although these can only contain inline elements.
    ```
    
    ``` tab="HTML"
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th style="text-align: left;"><strong>Note:</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td style="text-align: left;">Because most Markdown implementations do not support admonitions, they can be approximated with tables, although these can only contain inline elements.</td>
    </tr>
    </tbody>
    </table>
    ```
    
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th style="text-align: left;"><strong>Note:</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td style="text-align: left;">Because most Markdown implementations do not support admonitions, they can be approximated with tables, although these can only contain inline elements.</td>
    </tr>
    </tbody>
    </table>
    
    Alternatively, a line containing just four spaces can be added to the beginning of an admonition to make all the lines within the admonition render as an [indented code block](#ibcode) in Markdown implementations that do not support admonitions.


## blockquote {: #blockquote }

``` tab="Markdown"
> A blockquote is very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote.
```

``` tab="HTML"
<blockquote>
<p>A blockquote is very handy in email to emulate reply text. This line is part of the same quote.</p>
</blockquote>
<p>Quote break.</p>
<blockquote>
<p>This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can <em>put</em> <strong>Markdown</strong> into a blockquote.</p>
</blockquote>
```

!!! note ""
    
    <blockquote>
    <p>A blockquote is very handy in email to emulate reply text. This line is part of the same quote.</p>
    </blockquote>
    <p>Quote break.</p>
    <blockquote>
    <p>This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can <em>put</em> <strong>Markdown</strong> into a blockquote.</p>
    </blockquote>

A blockquote is equivalent to the [`<blockquote>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote) (block quotation) element in HTML.

## break {: #break }
### hard line break {: #hlbreak }

A hard line break is equivalent to the [`<br>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/br) (line break) element in HTML.

#### hard line break with two spaces {: #hlbreaktwospace }

!!! note
    
    Trailing spaces are shown with dots (`⋅`).

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

``` tab="HTML"
<p>Here's a line for us to start with.</p>
<p>This line is separated from the one above by two newlines, so it will be a <em>separate paragraph</em>.</p>
<p>This line is also a separate paragraph, but…<br />
This line is separated by a single newline and two spaces, so it's a separate line in the <em>same paragraph</em>.</p>
```

!!! note ""
    
    <p>Here's a line for us to start with.</p>
    <p>This line is separated from the one above by two newlines, so it will be a <em>separate paragraph</em>.</p>
    <p>This line is also a separate paragraph, but…<br />
    This line is separated by a single newline and two spaces, so it's a separate line in the <em>same paragraph</em>.</p>

#### hard line break with a backslash {: #hlbreakbslash }

``` tab="Markdown"
Ending a line with a backslash is also possible.\
This is less pretty, but more visible.
```

``` tab="HTML"
Ending a line with a backslash is also possible.<br />
This is less pretty, but more visible.
```

!!! note ""
    
    Ending a line with a backslash is also possible.<br />
    This is less pretty, but more visible.

### page break {: #pbreak }

A page break [can be indicated in Markdown using inline HTML or LaTeX formatting](ipbkMkd.md).

### thematic break {: #tbreak }

``` tab="Markdown"
Three or more...

---

Hyphens

***

Asterisks

___

Underscores
```

``` tab="HTML"
<p>Three or more…</p>
<hr />
<p>Hyphens</p>
<hr />
<p>Asterisks</p>
<hr />
<p>Underscores</p>
```

!!! note ""
    
    <p>Three or more…</p>
    <hr />
    <p>Hyphens</p>
    <hr />
    <p>Asterisks</p>
    <hr />
    <p>Underscores</p>

A thematic break is equivalent to the [`<hr>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/hr) (horizontal rule) element in HTML.

## code {: #code }

Code blocks are part of the Markdown spec, but syntax highlighting isn't. However, many renderers -- like Github's and *Markdown Here* -- support syntax highlighting. Which languages are supported and how those language names should be written will vary from renderer to renderer.

### block of code {: #bcode }
A block of code is equivalent to the [`<pre>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/pre) and [`<code>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/code) (preformatted code) elements in HTML.[^Mdwnref7]

#### fenced block of code {: #fbcode }
Three back-ticks (<code>```</code>) or three tildes (<code>\~\~\~</code>) can function as fences for producing one or more lines of code.

``` tab="Markdown"
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

``` tab="HTML"
<div class="sourceCode" id="cb1"><pre class="sourceCode javascript"><code class="sourceCode javascript"><a class="sourceLine" id="cb1-1" data-line-number="1"><span class="kw">var</span> s <span class="op">=</span> <span class="st">&quot;JavaScript syntax highlighting&quot;</span><span class="op">;</span></a>
<a class="sourceLine" id="cb1-2" data-line-number="2"><span class="at">alert</span>(s)<span class="op">;</span></a></code></pre></div>
<div class="sourceCode" id="cb2"><pre class="sourceCode python"><code class="sourceCode python"><a class="sourceLine" id="cb2-1" data-line-number="1">s <span class="op">=</span> <span class="st">&quot;Python syntax highlighting&quot;</span></a>
<a class="sourceLine" id="cb2-2" data-line-number="2"><span class="bu">print</span> s</a></code></pre></div>
<pre><code>No language indicated, so no syntax highlighting. 
But let&#39;s throw in a &lt;b&gt;tag&lt;/b&gt;.</code></pre>
```

!!! note ""
    
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

!!! note
    
    The raw Markdown is indented by a single space to allow nesting of a code block within a code block.

``` tab="Markdown"
~~~
These fences are more squiggly, but they still work.
~~~
```

``` tab="HTML"
<pre><code>These fences are more squiggly, but they still work.</code></pre>
```

!!! note ""
    
    <pre><code>These fences are more squiggly, but they still work.</code></pre>

#### indented block of code {: #ibcode }
A four-space indent produces one or more lines of code.

``` tab="Markdown"
    This formatting syntax works,
    but can be a pain to select as raw Markdown
    when spanning multiple lines of text.
```

``` tab="HTML"
<pre><code>This formatting syntax works,
but can be a pain to select as raw Markdown
when spanning multiple lines of text.</code></pre>
```

!!! note ""
    
    <pre><code>This formatting syntax works,
    but can be a pain to select as raw Markdown
    when spanning multiple lines of text.</code></pre>

### inline code {: #icode }

``` tab="Markdown"
Inline `code` has `back-ticks around` it.
```

``` tab="HTML"
Inline <code>code</code> has <code>back-ticks around</code> it.
```

!!! note ""
    
    Inline <code>code</code> has <code>back-ticks around</code> it.

Inline code is equivalent to the [`<code>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/code) (code) element in HTML.

## code comment {: #codecomment }
A code comment [can be included in Markdown using HTML formatting](incdcmt.md#Markdowncomment).

## emphasis {: #emphasis }

``` tab="Markdown"
Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

Combined emphasis with **asterisks and _underscores_**.
```

``` tab="HTML"
<p>Emphasis, aka italics, with <em>asterisks</em> or <em>underscores</em>.</p>
<p>Strong emphasis, aka bold, with <strong>asterisks</strong> or <strong>underscores</strong>.</p>
<p>Combined emphasis with <strong>asterisks and <em>underscores</em></strong>.</p>
```

!!! note ""
    
    <p>Emphasis, aka italics, with <em>asterisks</em> or <em>underscores</em>.</p>
    <p>Strong emphasis, aka bold, with <strong>asterisks</strong> or <strong>underscores</strong>.</p>
    <p>Combined emphasis with <strong>asterisks and <em>underscores</em></strong>.</p>

Emphasis is equivalent to the [`<em>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/em) (emphasis) element in HTML, and strong emphasis is equivalent to the [`<strong>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/strong) (strong importance) element in HTML.

## footnote {: #footnote }

!!! attention
    
    Unlike most other Markdown elements, a footnote does not have a direct HTML equivalent.[^Mdwnref4] This means that:
    
    1. Markdown offers a more standardized way of creating footnotes than HTML.
    2. HTML renderings of footnotes will differ significantly between different implementations of Markdown.

### inline-style footnote {: #ifootnote }
This style of footnote creates a self-contained footnote beside the text it references.

``` tab="Markdown"
An inline-style footnote consists of a caret (`^`) outside a pair of square brackets.
It can be created on a single line^[It will be formatted like this.].
```

``` tab="HTML"
<p>An inline-style footnote consists of a caret (<code>^</code>) outside a pair of square brackets. It can be created on a single line<a href="#fn1" class="footnote-ref" id="fnref1"><sup>1</sup></a>.</p>
<section class="footnotes">
<hr />
<ol>
<li id="fn1"><p>It will be formatted like this.<a href="#fnref1" class="footnote-back">↩</a></p></li>
</ol>
</section>
```

!!! note ""
    
    <p>An inline-style footnote consists of a caret (<code>^</code>) outside a pair of square brackets. It can be created on a single line<a href="#fn1" class="footnote-ref" id="fnref1"><sup>1</sup></a>.</p>
    <section class="footnotes">
    <hr />
    <ol>
    <li id="fn1"><p>It will be formatted like this.<a href="#fnref1" class="footnote-back">↩</a></p></li>
    </ol>
    </section>

### reference-style footnote {: #rfootnote }
This style of footnote resembles a [reference-style link](#rlink), but works differently. Instead of combining into a hyperlink, the reference becomes a numbered superscript and the link definition becomes a numbered footnote at the end of the page.

``` tab="Markdown"
The reference identifier[^1] is an string that begins with a caret (`^`).
A number often follows the caret, but other characters are also allowed[^character-limitations].

[^1]: In Python-Markdown, identifiers are called *labels*.
[^character-limitations]:
    Not all characters are allowed within the identifier.
    Pandoc's Markdown does not allow spaces, tabs, or newlines in the identifier.
```

``` tab="HTML"
<p>The reference identifier<a href="#fn1" class="footnote-ref" id="fnref1"><sup>1</sup></a> is an string that begins with a caret (<code>^</code>). A number often follows the caret, but other characters are also allowed<a href="#fn2" class="footnote-ref" id="fnref2"><sup>2</sup></a>.</p>
<section class="footnotes">
<hr />
<ol>
<li id="fn1"><p>In Python-Markdown, identifiers are called <em>labels</em>.<a href="#fnref1" class="footnote-back">↩</a></p></li>
<li id="fn2"><p>Not all characters are allowed within the identifier. Pandoc's Markdown does not allow spaces, tabs, or newlines in the identifier.<a href="#fnref2" class="footnote-back">↩</a></p></li>
</ol>
</section>
```

!!! note ""
    
    <p>The reference identifier<a href="#fn1" class="footnote-ref" id="fnref1"><sup>1</sup></a> is an string that begins with a caret (<code>^</code>). A number often follows the caret, but other characters are also allowed<a href="#fn2" class="footnote-ref" id="fnref2"><sup>2</sup></a>.</p>
    <section class="footnotes">
    <hr />
    <ol>
    <li id="fn1"><p>In Python-Markdown, identifiers are called <em>labels</em>.<a href="#fnref1" class="footnote-back">↩</a></p></li>
    <li id="fn2"><p>Not all characters are allowed within the identifier. Pandoc's Markdown does not allow spaces, tabs, or newlines in the identifier.<a href="#fnref2" class="footnote-back">↩</a></p></li>
    </ol>
    </section>

!!! attention
    
    [Python-Markdown](https://python-markdown.github.io/) expects an indentation of four spaces (or one tab) for footnotes with multiple blocks.[^Mdwnref5]

## heading {: #heading }
Headings can make a long document more readable by dividing it into sections, and the sections can be collected into a [table of contents](https://en.wikipedia.org/wiki/Table_of_contents). Most Markdown implementations will assign each heading a unique identifier using [the `id` attribute](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/id) so that each section can be directly hyperlinked to with a [fragment identifier](https://en.wikipedia.org/wiki/Fragment_identifier).

### [ATX]-style heading {: #ATXheading }
The use of number signs (`#`) is inspired by [the atx markup language](http://www.aaronsw.com/2002/atx/intro) created by [Aaron Swartz](https://en.wikipedia.org/wiki/Aaron_Swartz).

``` tab="Markdown"
# ATX level 1
## ATX level 2
### ATX level 3
#### ATX level 4
##### ATX level 5
###### ATX level 6
```

``` tab="HTML"
<h1 id="atx-level-1">ATX level 1</h1>
<h2 id="atx-level-2">ATX level 2</h2>
<h3 id="atx-level-3">ATX level 3</h3>
<h4 id="atx-level-4">ATX level 4</h4>
<h5 id="atx-level-5">ATX level 5</h5>
<h6 id="atx-level-6">ATX level 6</h6>
```

!!! note ""
    
    <span class="h1workaround">ATX level 1</span>
    
    <span class="h2workaround">ATX level 2</span>
    
    <span class="h3workaround">ATX level 3</span>
    
    <span class="h4workaround">ATX level 4</span>
    
    <span class="h5workaround">ATX level 5</span>
    
    <span class="h6workaround">ATX level 6</span>

[ATX]: http://www.aaronsw.com/2002/atx/intro

### [Setext]-style heading {: #Setextheading }
The use of equality signs (`=`) and dashes (`-`) is inspired by [the Setext markup language](https://en.wikipedia.org/wiki/Setext) by Ian Feldman.

``` tab="Markdown"
Setext level 1
==============

Setext level 2
--------------
```

``` tab="HTML"
<h1 id="setext-level-1">Setext level 1</h1>
<h2 id="setext-level-2">Setext level 2</h2>
```

!!! note ""
    
    <span class="h1workaround">Setext level 1</span>
    
    <span class="h2workaround">Setext level 2</span>

[Setext]: https://en.wikipedia.org/wiki/Setext

## image {: #image }

``` tab="Markdown"
Here's our logo (hover to see the title text):

Inline-style: 
![alt text](../Mdwnref.png "Logo Title Text 1")

Reference-style: 
![alt text][logo]

[logo]: ../Mdwnref.png "Logo Title Text 2"
```

``` tab="HTML"
<p>Here's our logo (hover to see the title text):</p>
<p>Inline-style: <img src="../Mdwnref.png" title="Logo Title Text 1" alt="alt text" /></p>
<p>Reference-style: <img src="../Mdwnref.png" title="Logo Title Text 2" alt="alt text" /></p>
```

!!! note ""
    
    <p>Here's our logo (hover to see the title text):</p>
    <p>Inline-style: <img src="../Mdwnref.png" title="Logo Title Text 1" alt="alt text" /></p>
    <p>Reference-style: <img src="../Mdwnref.png" title="Logo Title Text 2" alt="alt text" /></p>

An image is equivalent to the [`<img>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img) (image embed) element in HTML.

## inline HTML {: #html }
You can also use raw HTML in your Markdown, and it'll mostly work pretty well.

```
<figure>
<img src="../Mdwnref.png">
<figcaption>This colorful image could use a caption.<br>
Markdown in HTML does *not* work **very** well.
Use HTML <em>tags</em> <strong>instead</strong>.</figcaption>
</figure>
```

!!! note ""
    
    <figure>
    <img src="../Mdwnref.png">
    <figcaption>This colorful image could use a caption.<br>
    Markdown in HTML does *not* work **very** well.
    Use HTML <em>tags</em> <strong>instead</strong>.</figcaption>
    </figure>

## link {: #link }
A link is equivalent to the [`<a>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a) (anchor) element in HTML.

### automatic link {: #alink }

``` tab="Markdown"
A URL in angle brackets will automatically get turned into a link: <https://freedomdefined.org/Definition>.
```

``` tab="HTML"
A URL in angle brackets will automatically get turned into a link: <a href="https://freedomdefined.org/Definition" class="uri">https://freedomdefined.org/Definition</a>.
```

!!! note ""
    
    A URL in angle brackets will automatically get turned into a link: <a href="https://freedomdefined.org/Definition" class="uri">https://freedomdefined.org/Definition</a>.

### inline-style link {: #ilink }

``` tab="Markdown"
[I'm an inline-style link](https://freedomdefined.org/Definition), and
[I'm an inline-style link with a title](https://freedomdefined.org/Definition "Definition of Free Cultural Works").
```

``` tab="HTML"
<a href="https://freedomdefined.org/Definition">I'm an inline-style link</a>, and <a href="https://freedomdefined.org/Definition" title="Definition of Free Cultural Works">I'm an inline-style link with a title</a>.
```

!!! note ""
    
    <a href="https://freedomdefined.org/Definition">I'm an inline-style link</a>, and <a href="https://freedomdefined.org/Definition" title="Definition of Free Cultural Works">I'm an inline-style link with a title</a>.

### reference-style link {: #rlink }

``` tab="Markdown"
[I'm a reference-style link][with a separate link definition], and
[I'm a reference-style link and definition all in one].

The link definition for a reference-style link is included separately, usually at the bottom of the document.

[with a separate link definition]: https://freedomdefined.org/Definition
[I'm a reference-style link and definition all in one]: https://freedomdefined.org/Definition
```

``` tab="HTML"
<p><a href="https://freedomdefined.org/Definition">I'm a reference-style link</a>, and <a href="https://freedomdefined.org/Definition">I'm a reference-style link and definition all in one</a>.</p>
<p>The link definition for a reference-style link is included separately, usually at the bottom of the document.</p>
```

!!! note ""
    
    <p><a href="https://freedomdefined.org/Definition">I'm a reference-style link</a>, and <a href="https://freedomdefined.org/Definition">I'm a reference-style link and definition all in one</a>.</p>
    <p>The link definition for a reference-style link is included separately, usually at the bottom of the document.</p>

## list {: #list }
### attribute list {: #alist }

An attribute list allows [HTML-style attributes](https://en.wikipedia.org/wiki/HTML_attribute) to be added to Markdown elements with curly brackets (`{}`) and a [CSS-like syntax](https://en.wikipedia.org/wiki/Cascading_Style_Sheets#Syntax). More specifically:

- The [number sign](https://en.wikipedia.org/wiki/Number_sign) character (`#`) indicates an `id` or unique identifier. This can be used to create a hyperlink to a section of an HTML page using a [fragment identifier](https://en.wikipedia.org/wiki/Fragment_identifier).
- The [full stop](https://en.wikipedia.org/wiki/Full_stop) character (`.`) indicates a `class` or identifier that can be applied to multiple elements. With a [fenced code block](#fbcode), this can be used to identify what language the code block is written in, which can be used for [syntax highlighting](https://en.wikipedia.org/wiki/Syntax_highlighting), for example:
```
 ```{.yaml}
 foo:
   - bar
   - baz
 ```
```

!!! note
    
    The raw Markdown is indented by a single space to allow nesting of a code block within a code block.

``` tab="Markdown"
*This emphasized text*{#foo} will have `foo` as its `id`.  
**This strongly emphasized text**{.bar} will have `bar` as its `class`.
```

``` tab="HTML"
<p><em id="foo">This emphasized text</em> will have <code>foo</code> as its <code>id</code>.<br />
<strong class="bar">This strongly emphasized text</strong> will have <code>bar</code> as its <code>class</code>.</p>
```

!!! note ""
    
    <p><em id="foo">This emphasized text</em> will have <code>foo</code> as its <code>id</code>.<br />
    <strong class="bar">This strongly emphasized text</strong> will have <code>bar</code> as its <code>class</code>.</p>

!!! warning
    
    Some Markdown implementations specify a colon `:` immediately following the first curly bracket, but may still work without it.

### description list {: #dlist }

``` tab="Markdown"
A description list is made of terms and descriptions
: This is a description, paired with a term.

Each term and its description can represent an [attribute-value pair](https://en.wikipedia.org/wiki/Attribute–value_pair).

Here is an attribute.
: And here is a value.
: It starts with a colon.
: If a value spans multiple lines,
  readability is improved by adding indentation
  from the second line onward,
but it is not required.

: Values can be separated by blank lines,
and still have the same attribute.
```

``` tab="HTML"
<dl>
<dt>A description list is made of terms and descriptions</dt>
<dd>This is a description, paired with a term.
</dd>
</dl>
<p>Each term and its description can represent an <a href="https://en.wikipedia.org/wiki/Attribute–value_pair">attribute-value pair</a>.</p>
<dl>
<dt>Here is an attribute.</dt>
<dd>And here is a value.
</dd>
<dd>It starts with a colon.
</dd>
<dd>If a value spans multiple lines, readability is improved by adding indentation from the second line onward, but it is not required.
</dd>
<dd><p>Values can be separated by blank lines, and still have the same attribute.</p>
</dd>
</dl>
```

!!! note ""
    
    <dl>
    <dt>A description list is made of terms and descriptions</dt>
    <dd>This is a description, paired with a term.
    </dd>
    </dl>
    <p>Each term and its description can represent an <a href="https://en.wikipedia.org/wiki/Attribute–value_pair">attribute-value pair</a>.</p>
    <dl>
    <dt>Here is an attribute.</dt>
    <dd>And here is a value.
    </dd>
    <dd>It starts with a colon.
    </dd>
    <dd>If a value spans multiple lines, readability is improved by adding indentation from the second line onward, but it is not required.
    </dd>
    <dd><p>Values can be separated by blank lines, and still have the same attribute.</p>
    </dd>
    </dl>

A description list is equivalent to the [`<dl>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dl), [`<dt>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dt), and [`<dd>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dd) (description list with one or more terms and descriptions) elements in HTML.

!!! attention
    
    The HTML elements [`<dl>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dl), [`<dt>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dt), and [`<dd>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dd) that make up a description list are inconsistently named across different sources, possibly because they resemble abbreviations.
    
    - The `<dl>` element currently means **description list**[^Mdwnref8], but was referred to as a *definition list* [in the HTML 4.01 specification](https://www.w3.org/TR/html4/struct/lists.html#edef-DL).
    - The `<dt>` and `<dd>` elements mean **term** and **description**[^Mdwnref8], and make up [term-description groups](https://www.w3.org/TR/html5/grouping-content.html#term-description-groups).
        - [On Wikipedia](https://en.wikipedia.org/w/index.php?title=HTML_element&oldid=879416218#Lists), `<dt>` is referred to as a *name* or (previously) as a *definition term*, and `<dd>` is referred to as a *value* or (previously) as *definition data*.
        - [On MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dd$revision/1393699), `<dd>` is referred to as *The Description Details element*.

### ordered list {: #olist }

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

``` tab="HTML"
<ol type="1">
<li>First ordered list item</li>
<li>Another item
<ul>
<li>Unordered sub-list.</li>
</ul></li>
<li>Actual numbers don't matter, just that it's a number
<ol type="1">
<li>Ordered sub-list</li>
</ol></li>
<li><p>And another item.</p>
<p>You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces.</p>
<p>To have a line break without a paragraph, you will need to use two trailing spaces.<br />
Note that this line is separate, but within the same paragraph.</p></li>
</ol>
```

!!! note ""
    
    <ol type="1">
    <li>First ordered list item</li>
    <li>Another item
    <ul>
    <li>Unordered sub-list.</li>
    </ul></li>
    <li>Actual numbers don't matter, just that it's a number
    <ol type="1">
    <li>Ordered sub-list</li>
    </ol></li>
    <li><p>And another item.</p>
    <p>You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces.</p>
    <p>To have a line break without a paragraph, you will need to use two trailing spaces.<br />
    Note that this line is separate, but within the same paragraph.</p></li>
    </ol>

!!! attention
    
    [Python-Markdown](https://python-markdown.github.io/) expects an indentation of four spaces (or one tab) for nested block level elements, which includes lists and sub-lists.[^Mdwnref6]

An ordered list is equivalent to the [`<ol>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol) and [`<li>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/li) (ordered list with one or more list items) elements in HTML.

### unordered list {: #ulist }

``` tab="Markdown"
* An unordered list can use asterisks
- Or minuses
+ Or pluses
```

``` tab="HTML"
<ul>
<li>An unordered list can use asterisks</li>
<li>Or minuses</li>
<li>Or pluses</li>
</ul>
```

!!! note ""
    
    <ul>
    <li>An unordered list can use asterisks</li>
    <li>Or minuses</li>
    <li>Or pluses</li>
    </ul>

An unordered list is equivalent to the [`<ul>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul) and [`<li>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/li) (unordered list with one or more list items) elements in HTML.

## strikethrough {: #strikethrough }

``` tab="Markdown"
A strikethrough uses two tildes. ~~Scratch this.~~
```

``` tab="HTML"
A strikethrough uses two tildes. <del>Scratch this.</del>
```

!!! note ""
    
    Strikethrough uses two tildes. <del>Scratch this.</del>

A strikethrough is equivalent to the [`<del>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/del) (deleted text) element in HTML.

## table {: #table }

Colons can be used to align columns.

``` tab="Markdown"
| A table       | Is            | Cool  |
|---------------|:-------------:|------:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |
```

``` tab="HTML"
<table>
<thead>
<tr class="header">
<th>A table</th>
<th style="text-align: center;">Is</th>
<th style="text-align: right;">Cool</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>col 3 is</td>
<td style="text-align: center;">right-aligned</td>
<td style="text-align: right;">$1600</td>
</tr>
<tr class="even">
<td>col 2 is</td>
<td style="text-align: center;">centered</td>
<td style="text-align: right;">$12</td>
</tr>
<tr class="odd">
<td>zebra stripes</td>
<td style="text-align: center;">are neat</td>
<td style="text-align: right;">$1</td>
</tr>
</tbody>
</table>
```

!!! note ""
    
    <table>
    <thead>
    <tr class="header">
    <th>A table</th>
    <th style="text-align: center;">Is</th>
    <th style="text-align: right;">Cool</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>col 3 is</td>
    <td style="text-align: center;">right-aligned</td>
    <td style="text-align: right;">$1600</td>
    </tr>
    <tr class="even">
    <td>col 2 is</td>
    <td style="text-align: center;">centered</td>
    <td style="text-align: right;">$12</td>
    </tr>
    <tr class="odd">
    <td>zebra stripes</td>
    <td style="text-align: center;">are neat</td>
    <td style="text-align: right;">$1</td>
    </tr>
    </tbody>
    </table>

The table will render correctly even if the raw Markdown does not line up prettily. The rightmost pipe (`|`) and any extra spaces can be omitted. Only one dash is required to separate each header cell. You can also use inline Markdown.

``` tab="Markdown"
| Markdown | Less | Pretty
|-|-|-
| *Still* | `renders` | **nicely**
| 1 | 2 | 3
```

``` tab="HTML"
<table>
<thead>
<tr class="header">
<th>Markdown</th>
<th>Less</th>
<th>Pretty</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Still</em></td>
<td><code>renders</code></td>
<td><strong>nicely</strong></td>
</tr>
<tr class="even">
<td>1</td>
<td>2</td>
<td>3</td>
</tr>
</tbody>
</table>
```

!!! note ""
    
    <table>
    <thead>
    <tr class="header">
    <th>Markdown</th>
    <th>Less</th>
    <th>Pretty</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><em>Still</em></td>
    <td><code>renders</code></td>
    <td><strong>nicely</strong></td>
    </tr>
    <tr class="even">
    <td>1</td>
    <td>2</td>
    <td>3</td>
    </tr>
    </tbody>
    </table>

A table is equivalent to the [`<table>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table) (table) element in HTML, and possibly one or more of the following elements:

- [`<caption>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/caption)
- [`<colgroup>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/colgroup)
- [`<tbody>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tbody)
- [`<tfoot>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tfoot)
- [`<thead>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/thead)
- [`<tr>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tr)

## comparison of Markdown implementations

<!-- This table depends on CSS tweaks to display correctly. -->

|                                                                                     | [Beaker Browser Markdown] | [GitHub Flavored Markdown]                                             | [John Gruber's Markdown] | [Pandoc's Markdown]                             | [PyMdown]                                      | [Python-Markdown]                      | [Stack Overflow Markdown]                                 |
|:------------------------------------------------------------------------------------|:--------------------------|:-----------------------------------------------------------------------|:-------------------------|:------------------------------------------------|:-----------------------------------------------|:---------------------------------------|:----------------------------------------------------------|
|{: .fth } [admonition]                                                               | no{: .no}                 | no{: .no}                                                              | no{: .no}                | no{: .no}                                       | no{: .no}                                      | yes (with extension){: .yes}[^pynadmo] | no{: .no}                                                 |
|{: .fth } [blockquote]                                                               | yes{: .yes}               | yes{: .yes}[^gfmblkq]                                                  | yes{: .yes}[^jgmblkq]    | yes{: .yes}[^pdmblkq]                           | yes{: .yes}                                    | yes{: .yes}                            | yes{: .yes}[^somblq1] [^somblq2]                          |
|{: .fth } [break]  [(hard line, with a backslash)][hard line break with a backslash] | yes{: .yes}               | yes{: .yes}[^gfmbhlk]                                                  | no{: .no}                | yes (with an extension){: .yes}[^pdmbhlk]       | no{: .no}                                      | no{: .no}                              | no{: .no}                                                 |
|{: .fth } [break]  [(hard line, with two spaces)][hard line break with two spaces]   | yes{: .yes}               | yes{: .yes}[^gfmbhlk]                                                  | yes{: .yes} [^jgmbhls]   | yes{: .yes}[^pdmbhlk]                           | yes{: .yes}[^pymbhls]                          | yes{: .yes}                            | yes{: .yes}[^sombhls]                                     |
|{: .fth } [break]  [(thematic)][thematic break]                                      | yes{: .yes}               | yes{: .yes}[^gfmtbrk]                                                  | yes{: .yes}[^jgmtbrk]    | yes{: .yes}[^pdmtbrk]                           | yes{: .yes}                                    | yes{: .yes}                            | yes{: .yes}[^somtbrk]                                     |
|{: .fth } [code]  [(fenced block)][fenced block of code]                             | yes{: .yes}               | yes{: .yes}[^gfmfcdb]                                                  | no{: .no}                | yes (with extension){: .yes}[^pdmfcdb]          | yes (with extension){: .yes}[^pymexra]         | yes (with extension){: .yes}[^pyncodb] | no{: .no}                                                 |
|{: .fth } [code]  [(indented block)][indented block of code]                         | yes{: .yes}               | yes{: .yes}[^gfmicdb]                                                  | yes{: .yes}[^jgmcodb]    | yes{: .yes}[^pdmicdb]                           | yes (with extension){: .yes}[^pymexra]         | yes{: .yes}                            | yes{: .yes}[^somicdb]                                     |
|{: .fth } [code]  [(inline)][inline code]                                            | yes{: .yes}               | yes{: .yes}[^gfmcodi]                                                  | yes{: .yes}[^jgmcodi]    | yes{: .yes}[^pdmcodi]                           | yes{: .yes}                                    | yes{: .yes}                            | yes{: .yes}                                               |
|{: .fth } [emphasis]                                                                 | yes{: .yes}               | yes{: .yes}[^gfmemph]                                                  | yes{: .yes}[^jgmemph]    | yes{: .yes}[^pdmemph]                           | yes{: .yes}                                    | yes{: .yes}                            | yes{: .yes}[^somemph]                                     |
|{: .fth } [footnote]  [(inline-style)][inline-style footnote]                        | no{: .no}                 | no{: .no}                                                              | no{: .no}                | yes (with extension){: .yes}[^pdmftnt]          | partial (with extension){: .partial}[^pymfnis] | no{: .no}[^pynfnis]                    | no{: .no}                                                 |
|{: .fth } [footnote]  [(reference-style)][reference-style footnote]                  | no{: .no}                 | no{: .no}                                                              | no{: .no}                | yes (with extension){: .yes}[^pdmftnt]          | yes (with extension){: .yes}[^pymexra]         | yes (with extension){: .yes}[^pynfnrs] | no{: .no}                                                 |
|{: .fth } [heading]  [(ATX-style)][ATX-style heading]                                | yes{: .yes}               | yes{: .yes}[^gfmatxh]                                                  | yes{: .yes}[^jgmhdng]    | yes{: .yes}[^pdmatxh]                           | yes{: .yes}                                    | yes{: .yes}                            | no{: .no}                                                 |
|{: .fth } [heading]  [(Setext-style)][Setext-style heading]                          | yes{: .yes}               | yes{: .yes}[^gfmstxh]                                                  | yes{: .yes}[^jgmhdng]    | yes{: .yes}[^pdmstxh]                           | yes{: .yes}                                    | yes{: .yes}                            | yes{: .yes}[^somstxh]                                     |
|{: .fth } [image]                                                                    | yes{: .yes}               | yes{: .yes}[^gfmimag]                                                  | yes{: .yes}[^jgmimag]    | yes{: .yes}[^pdmimag]                           | yes{: .yes}                                    | yes{: .yes}                            | yes{: .yes}[^somimag]                                     |
|{: .fth } [inline HTML]                                                              | yes{: .yes}               | partial (some tags are filtered out){: .partial} [^gfmhtm1] [^gfmhtm2] | yes{: .yes}[^jgmhtml]    | yes (with extension){: .yes}[^pdmhtml]          | yes{: .yes}                                    | yes{: .yes}                            | partial (whitelist only){: .partial}[^somhtm1] [^somhtm2] |
|{: .fth } [link]  [(automatic)][automatic link]                                      | yes{: .yes}               | yes{: .yes}[^gfmlka1] [^gfmlka2]                                       | yes{: .yes}[^jgmlkao]    | yes{: .yes}[^pdmlkao]                           | yes{: .yes}                                    | yes{: .yes}                            | yes{: .yes}[^somlkao]                                     |
|{: .fth } [link]  [(inline-style)][inline-style link]                                | yes{: .yes}               | yes{: .yes}[^gfmlkis]                                                  | yes{: .yes}[^jgmlink]    | yes{: .yes}[^pdmlkis]                           | yes{: .yes}                                    | yes{: .yes}                            | yes{: .yes}[^somlink]                                     |
|{: .fth } [link]  [(reference-style)][reference-style link]                          | yes{: .yes}               | yes{: .yes}[^gfmlkrs]                                                  | yes{: .yes}[^jgmlink]    | yes{: .yes}[^pdmlkrs]                           | yes{: .yes}                                    | yes{: .yes}                            | yes{: .yes}[^somlink]                                     |
|{: .fth } [list]  [(attribute list)][attribute list]                                 | no{: .no}                 | no{: .no}                                                              | no{: .no}                | partial (with extensions){: .partial}[^pdmlatr] | no{: .no}                                      | yes (with extension){: .yes}[^pynlatr] | no{: .no}                                                 |
|{: .fth } [list]  [(description list)][description list]                             | no{: .no}                 | no{: .no}                                                              | no{: .no}                | yes (with extension){: .yes}[^pdmldsc]          | yes (with extension){: .yes}[^pymexra]         | yes (with extension){: .yes}[^pynldsc] | no{: .no}                                                 |
|{: .fth } [list]  [(ordered list)][ordered list]                                     | yes{: .yes}               | yes{: .yes}[^gfmlist]                                                  | yes{: .yes}[^jgmlist]    | yes{: .yes}[^pdmlord]                           | yes{: .yes}                                    | yes{: .yes}                            | yes{: .yes}[^somlist]                                     |
|{: .fth } [list]  [(unordered list)][unordered list]                                 | yes{: .yes}               | yes{: .yes}[^gfmlist]                                                  | yes{: .yes}[^jgmlist]    | yes{: .yes}[^pdmlurd]                           | yes{: .yes}                                    | yes{: .yes}                            | yes{: .yes}[^somlist]                                     |
|{: .fth } [strikethrough]                                                            | yes{: .yes}               | yes (with extension){: .yes}[^gfmstrk]                                 | no{: .no}                | yes (with extension){: .yes}[^pdmstrk]          | yes (with extension){: .yes}[^pymtlde]         | no{: .no}                              | no{: .no}                                                 |
|{: .fth } [table]                                                                    | yes{: .yes}               | yes (with extension){: .yes}[^gfmtabl]                                 | no{: .no}                | yes (with extension){: .yes}[^pdmtabl]          | yes (with extension){: .yes}[^pymexra]         | yes (with extension){: .yes}[^pyntabl] | no (by design){: .no} [^somhtm2]                          |

[admonition]: #admonition
[attribute list]: #alist
[automatic link]: #alink
[blockquote]: #blockquote
[break]: #break
[code]: #code
[description list]: #dlist
[emphasis]: #emphasis
[fenced block of code]: #fbcode
[footnote]: #footnote
[hard line break with a backslash]: #hlbreakbslash
[hard line break with two spaces]: #hlbreaktwospace
[heading]: #heading
[image]: #image
[indented block of code]: #ibcode
[inline-style footnote]: #ifootnote
[inline-style link]: #ilink
[inline code]: #icode
[inline HTML]: #html
[link]: #link
[list]: #list
[ordered list]: #olist
[reference-style footnote]: #rfootnote
[reference-style link]: #rlink
[strikethrough]: #strikethrough
[table]: #table
[thematic break]: #tbreak
[unordered list]: #ulist
[ATX-style heading]: #ATXheading
[Beaker Browser Markdown]: https://beakerbrowser.com/docs/guides/create-a-markdown-site
[Setext-style heading]: #Setextheading
[GitHub Flavored Markdown]: https://github.github.com/gfm/
[John Gruber's Markdown]: https://daringfireball.net/projects/markdown/syntax
[Pandoc's Markdown]: https://pandoc.org/MANUAL.html#pandocs-markdown
[PyMdown]: https://facelessuser.github.io/PyMdown/
[Python-Markdown]: https://python-markdown.github.io/
[Stack Overflow Markdown]: https://stackoverflow.com/editing-help
[^gfmbhlk]: <https://github.github.com/gfm/#hard-line-break>
[^gfmblkq]: <https://github.github.com/gfm/#block-quotes>
[^gfmcodi]: <https://github.github.com/gfm/#code-spans>
[^gfmemph]: <https://github.github.com/gfm/#emphasis-and-strong-emphasis>
[^gfmfcdb]: <https://github.github.com/gfm/#fenced-code-blocks>
[^gfmatxh]: <https://github.github.com/gfm/#atx-headings>
[^gfmstxh]: <https://github.github.com/gfm/#setext-headings>
[^gfmhtm1]: <https://github.github.com/gfm/#raw-html>
[^gfmhtm2]: <https://github.github.com/gfm/#disallowed-raw-html-extension->
[^gfmicdb]: <https://github.github.com/gfm/#indented-code-blocks>
[^gfmimag]: <https://github.github.com/gfm/#images>
[^gfmlist]: <https://github.github.com/gfm/#lists>
[^gfmlka1]: <https://github.github.com/gfm/#autolink>
[^gfmlka2]: <https://github.github.com/gfm/#autolinks-extension->
[^gfmlkis]: <https://github.github.com/gfm/#links>
[^gfmlkrs]: <https://github.github.com/gfm/#link-reference-definitions>
[^gfmstrk]: <https://github.github.com/gfm/#strikethrough-extension->
[^gfmtabl]: <https://github.github.com/gfm/#tables-extension->
[^gfmtbrk]: <https://github.github.com/gfm/#thematic-break>
[^jgmbhls]: <https://daringfireball.net/projects/markdown/syntax#p>
[^jgmblkq]: <https://daringfireball.net/projects/markdown/syntax#blockquote>
[^jgmcodb]: <https://daringfireball.net/projects/markdown/syntax#precode>
[^jgmcodi]: <https://daringfireball.net/projects/markdown/syntax#code>
[^jgmemph]: <https://daringfireball.net/projects/markdown/syntax#em>
[^jgmhdng]: <https://daringfireball.net/projects/markdown/syntax#header>
[^jgmhtml]: <https://daringfireball.net/projects/markdown/syntax#html>
[^jgmimag]: <https://daringfireball.net/projects/markdown/syntax#img>
[^jgmlink]: <https://daringfireball.net/projects/markdown/syntax#link>
[^jgmlist]: <https://daringfireball.net/projects/markdown/syntax#list>
[^jgmlkao]: <https://daringfireball.net/projects/markdown/syntax#autolink>
[^jgmtbrk]: <https://daringfireball.net/projects/markdown/syntax#hr>
[^pdmbhlk]: <https://pandoc.org/MANUAL.html#paragraphs>
[^pdmblkq]: <https://pandoc.org/MANUAL.html#block-quotations>
[^pdmcodi]: <https://pandoc.org/MANUAL.html#verbatim>
[^pdmemph]: <https://pandoc.org/MANUAL.html#emphasis>
[^pdmfcdb]: <https://pandoc.org/MANUAL.html#fenced-code-blocks>
[^pdmftnt]: <https://pandoc.org/MANUAL.html#footnotes>
[^pdmatxh]: <https://pandoc.org/MANUAL.html#atx-style-headers>
[^pdmstxh]: <https://pandoc.org/MANUAL.html#setext-style-headers>
[^pdmhtml]: <https://pandoc.org/MANUAL.html#raw-html>
[^pdmicdb]: <https://pandoc.org/MANUAL.html#indented-code-blocks>
[^pdmimag]: <https://pandoc.org/MANUAL.html#images>
[^pdmldsc]: <https://pandoc.org/MANUAL.html#definition-lists>
[^pdmlkao]: <https://pandoc.org/MANUAL.html#automatic-links>
[^pdmlkis]: <https://pandoc.org/MANUAL.html#inline-links>
[^pdmlkrs]: <https://pandoc.org/MANUAL.html#reference-links>
[^pdmlatr]: Attribute lists are supported only with [bracketed spans](https://pandoc.org/MANUAL.html#extension-bracketed_spans), [fenced divs](https://pandoc.org/MANUAL.html#extension-fenced_divs), [fenced code blocks](https://pandoc.org/MANUAL.html#extension-fenced_code_attributes), [headings](https://pandoc.org/MANUAL.html#header-identifiers), [images](https://pandoc.org/MANUAL.html#extension-link_attributes), [links](https://pandoc.org/MANUAL.html#extension-link_attributes) using extensions.
[^pdmlord]: <https://pandoc.org/MANUAL.html#ordered-lists>
[^pdmlurd]: <https://pandoc.org/MANUAL.html#bullet-lists>
[^pdmstrk]: <https://pandoc.org/MANUAL.html#strikeout>
[^pdmtabl]: <https://pandoc.org/MANUAL.html#tables>
[^pdmtbrk]: <https://pandoc.org/MANUAL.html#horizontal-rules>
[^pymbhls]: <https://facelessuser.github.io/PyMdown/user-guide/markdown-syntax/#p>
[^pymexra]: <https://facelessuser.github.io/pymdown-extensions/extensions/extra/>
[^pymfnis]: Inline-style footnotes can be approximated using the [Caret extension](https://facelessuser.github.io/pymdown-extensions/extensions/caret/) to create numbered superscripts and an ordered list. Links between the superscript and footnote will not be available.
[^pymtlde]: <https://facelessuser.github.io/pymdown-extensions/extensions/tilde/>
[^pynadmo]: <https://python-markdown.github.io/extensions/admonition/>
[^pyncodb]: <https://python-markdown.github.io/extensions/fenced_code_blocks/>
[^pynfnis]: <https://github.com/Python-Markdown/markdown/issues/658>
[^pynfnrs]: <https://python-markdown.github.io/extensions/footnotes/>
[^pynlatr]: <https://python-markdown.github.io/extensions/attr_list/>
[^pynldsc]: <https://python-markdown.github.io/extensions/definition_lists/>
[^pyntabl]: <https://python-markdown.github.io/extensions/tables/>
[^sombhls]: <https://stackoverflow.com/editing-help#link-linebreaks>
[^somblq1]: <https://stackoverflow.com/editing-help#link-simple-blockquotes>
[^somblq2]: <https://stackoverflow.com/editing-help#link-advanced-blockquotes>
[^somemph]: <https://stackoverflow.com/editing-help#link-italics-bold>
[^somstxh]: <https://stackoverflow.com/editing-help#link-headers>
[^somhtm1]: <https://stackoverflow.com/editing-help#link-html>
[^somhtm2]: <https://meta.stackexchange.com/questions/1777/what-html-tags-are-allowed-on-stack-exchange-sites/135909#135909>
[^somicdb]: <https://stackoverflow.com/editing-help#link-code>
[^somimag]: <https://stackoverflow.com/editing-help#link-images>
[^somlink]: <https://stackoverflow.com/editing-help#link-links>
[^somlist]: <https://stackoverflow.com/editing-help#link-simple-lists>
[^somlkao]: <https://stackoverflow.com/editing-help#link-bare-urls>
[^somtbrk]: <https://stackoverflow.com/editing-help#link-horizontal-rules>


## licensing
**Some rights reserved: [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/).** Includes significant content from [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) on GitHub with changes made, including the following:

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
- The information on the CSS-like syntax of an [attribute list](#alist) was introduced to me by [Cascading Style Sheets§Selector](https://en.wikipedia.org/wiki/Cascading_Style_Sheets#Selector) on Wikipedia.
- The bulk of the instructions were introduced to me through [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet), part of the [Markdown Here](https://github.com/adam-p/markdown-here) [wiki](https://github.com/adam-p/markdown-here/wiki) on GitHub.

[Markdown]: https://en.wikipedia.org/wiki/Markdown
[^jgmblkq]: <https://daringfireball.net/projects/markdown/syntax#blockquote>
[^Mdwnref1]: <https://github.com/squidfunk/mkdocs-material/issues/179#issuecomment-282027581>
[^Mdwnref2]: <https://stackoverflow.com/questions/7579826/which-semantic-html-tag-for-displaying-side-notes-and-admonitions/7579894#7579894>
[^Mdwnref3]: <https://stackoverflow.com/questions/7579826/which-semantic-html-tag-for-displaying-side-notes-and-admonitions/8297157#8297157>
[^Mdwnref4]: <https://en.wikipedia.org/wiki/Note_(typography)#HTML>
[^Mdwnref5]: <https://python-markdown.github.io/extensions/footnotes/#syntax>
[^Mdwnref6]: <https://python-markdown.github.io/#differences>
[^Mdwnref7]: <https://daringfireball.net/projects/markdown/syntax#precode>
[^Mdwnref8]: <https://www.w3.org/TR/html5/grouping-content.html#the-dl-element>
