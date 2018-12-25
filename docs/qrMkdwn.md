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

??? note
    
    - The HTML versions of the Markdown examples were produced with [pandoc](https://pandoc.org/), except for [admonitions](#admonitions), which was produced with MkDocs, and a result in *blocks of code*, which was left as raw Markdown in order to produce syntax highlighting. For results with only one paragraph, HTML paragraph tags have been removed.
    - The HTML results of the Markdown examples are presented inside [admonitions without an icon or title](https://squidfunk.github.io/mkdocs-material/extensions/admonition/#removing-the-title), and with [admonitions](#admonitions) this is accomplished with an extra nested *div* element. To avoid adding extraneous entries to the table of contents[^qrMkdown1], several [headings](#headings) admonitions contain specially-styled HTML instead of heading elements.

## admonitions {: #admonitions }

``` tab="Markdown"
!!! attention
    
    Admonitions interrupt the flow of a document to communicate something contextually significant. They can be grouped into categories, and are often accompanied by specific icons and colors.
```

``` tab="HTML"
<div class="admonition attention">
<p class="admonition-title">Attention</p>
<p>Admonitions interrupt the flow of a document to communicate something contextually significant. They can be grouped into categories, and are often accompanied by specific icons and colors.</p>
</div>
```

<div class="admonition note">
<div class="admonition attention">
<p class="admonition-title">Attention</p>
<p>Admonitions interrupt the flow of a document to communicate something contextually significant. They can be grouped into categories, and are often accompanied by specific icons and colors.</p>
</div>
</div>

Admonitions do not have a direct HTML equivalent, but [the *aside* element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/aside) may suffice.[^qrMkdown2] [^qrMkdown3]

??? danger "Compatibility hack"
    
    A line containing just four spaces can be added to the beginning of an admonition to make all the lines within the admonition render as a [code block](#bcode) in Markdown implementations that do not support admonitions.

## blockquotes {: #blockquotes }

``` tab="Markdown"
> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote.
```

``` tab="HTML"
<blockquote>
<p>Blockquotes are very handy in email to emulate reply text. This line is part of the same quote.</p>
</blockquote>
<p>Quote break.</p>
<blockquote>
<p>This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can <em>put</em> <strong>Markdown</strong> into a blockquote.</p>
</blockquote>
```

!!! note ""
    
    <blockquote>
    <p>Blockquotes are very handy in email to emulate reply text. This line is part of the same quote.</p>
    </blockquote>
    <p>Quote break.</p>
    <blockquote>
    <p>This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can <em>put</em> <strong>Markdown</strong> into a blockquote.</p>
    </blockquote>

## breaks {: #breaks }
### hard line breaks {: #hlbreak }

Hard line breaks correspond to [the *br* (line break) element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/br) in HTML.

#### hard line breaks with two spaces {: #hlbreaktwospace }

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

#### hard line breaks with a backslash {: #hlbreakbslash }

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

### page breaks {: #pbreak }

Page breaks [can be indicated in Markdown using inline HTML or LaTeX formatting](ipbkMkd.md).

### thematic breaks {: #tbreak }

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

Thematic breaks correspond to [the *hr* (horizontal rule) element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/hr) in HTML.

## code {: #code }

Code blocks are part of the Markdown spec, but syntax highlighting isn't. However, many renderers -- like Github's and *Markdown Here* -- support syntax highlighting. Which languages are supported and how those language names should be written will vary from renderer to renderer.

### inline code {: #icode }

``` tab="Markdown"
Inline `code` has `back-ticks around` it.
```

``` tab="HTML"
Inline <code>code</code> has <code>back-ticks around</code> it.
```

!!! note ""
    
    Inline <code>code</code> has <code>back-ticks around</code> it.

### blocks of code {: #bcode }
 Blocks of code are fenced by lines with three back-ticks (<code>```</code>).

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

Alternatively, code blocks can be fenced by three tildes (`~~~`) or be indented by four spaces.

``` tab="Markdown"
~~~
The quick
brown fox
~~~

    jumps over
    the lazy dog.
```

``` tab="HTML"
<pre><code>The quick
brown fox</code></pre>
<pre><code>jumps over
the lazy dog.</code></pre>
```

!!! note ""
    
    <pre><code>The quick
    brown fox</code></pre>
    <pre><code>jumps over
    the lazy dog.</code></pre>

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

## footnotes {: #footnotes }

!!! attention
    
    Unlike most other Markdown elements, a footnote does not directly correspond with any existing HTML element.[^qrMkdown4] This means that:
    
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
This style of footnote resembles a reference-style link, but works differently. Instead of combining into a hyperlink, the reference becomes a numbered superscript and the link definition becomes a numbered footnote at the end of the page.

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
    
    [Python-Markdown](https://python-markdown.github.io/) expects an indentation of four spaces (or one tab) for footnotes with multiple blocks.[^qrMkdown5]

## headings {: #headings }

``` tab="Markdown"
# H1
## H2
### H3
#### H4
##### H5
###### H6
```

``` tab="HTML"
<h1 id="h1">H1</h1>
<h2 id="h2">H2</h2>
<h3 id="h3">H3</h3>
<h4 id="h4">H4</h4>
<h5 id="h5">H5</h5>
<h6 id="h6">H6</h6>
```

!!! note ""
    
    <span class="h1workaround">H1</span>
    
    <span class="h2workaround">H2</span>
    
    <span class="h3workaround">H3</span>
    
    <span class="h4workaround">H4</span>
    
    <span class="h5workaround">H5</span>
    
    <span class="h6workaround">H6</span>

Alternatively, for H1 and H2, an underline-ish style:

``` tab="Markdown"
Alt-H1
======

Alt-H2
------
```

``` tab="HTML"
<h1 id="alt-h1">Alt-H1</h1>
<h2 id="alt-h2">Alt-H2</h2>
```

!!! note ""
    
    <span class="h1workaround">Alt-H1</span>
    
    <span class="h2workaround">Alt-H2</span>

## images {: #images }

``` tab="Markdown"
Here's our logo (hover to see the title text):

Inline-style: 
![alt text](qrMkdwn.png "Logo Title Text 1")

Reference-style: 
![alt text][logo]

[logo]: qrMkdwn.png "Logo Title Text 2"
```

``` tab="HTML"
<p>Here's our logo (hover to see the title text):</p>
<p>Inline-style: <img src="qrMkdwn.png" title="Logo Title Text 1" alt="alt text" /></p>
<p>Reference-style: <img src="qrMkdwn.png" title="Logo Title Text 2" alt="alt text" /></p>
```

!!! note ""
    
    <p>Here's our logo (hover to see the title text):</p>
    <p>Inline-style: <img src="qrMkdwn.png" title="Logo Title Text 1" alt="alt text" /></p>
    <p>Reference-style: <img src="qrMkdwn.png" title="Logo Title Text 2" alt="alt text" /></p>

## inline HTML {: #html }
You can also use raw HTML in your Markdown, and it'll mostly work pretty well.

```
<figure>
<img src="qrMkdwn.png">
<figcaption>This colorful image could use a caption.<br>
Markdown in HTML does *not* work **very** well.
Use HTML <em>tags</em> <strong>instead</strong>.</figcaption>
</figure>
```

!!! note ""
    
    <figure>
    <img src="qrMkdwn.png">
    <figcaption>This colorful image could use a caption.<br>
    Markdown in HTML does *not* work **very** well.
    Use HTML <em>tags</em> <strong>instead</strong>.</figcaption>
    </figure>

## links {: #links }
### automatic link {: #alink }

``` tab="Markdown"
URLs in angle brackets will automatically get turned into links: <https://freedomdefined.org/Definition>.
```

``` tab="HTML"
URLs in angle brackets will automatically get turned into links: <a href="https://freedomdefined.org/Definition" class="uri">https://freedomdefined.org/Definition</a>.
```

!!! note ""
    
    URLs in angle brackets will automatically get turned into links: <a href="https://freedomdefined.org/Definition" class="uri">https://freedomdefined.org/Definition</a>.

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

## lists {: #lists }
### description lists {: #dlists }

``` tab="Markdown"
Description lists are made of terms and details
: We don't need to go into much detail about it.

Each term and its details can represent attribute-value pairs.

Here is an attribute.
: And here is a value.
: It starts with a colon.
```

``` tab="HTML"
<dl>
<dt>Description lists are made of terms and details</dt>
<dd>We don't need to go into much detail about it.
</dd>
</dl>
<p>Each term and its details can represent attribute-value pairs.</p>
<dl>
<dt>Here is an attribute.</dt>
<dd>And here is a value.
</dd>
<dd>It starts with a colon.
</dd>
</dl>
```

!!! note ""
    
    <dl>
    <dt>Description lists are made of terms and details</dt>
    <dd>We don't need to go into much detail about it.
    </dd>
    </dl>
    <p>Each term and its details can represent attribute-value pairs.</p>
    <dl>
    <dt>Here is an attribute.</dt>
    <dd>And here is a value.
    </dd>
    <dd>It starts with a colon.
    </dd>
    </dl>

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
    
    [Python-Markdown](https://python-markdown.github.io/) expects an indentation of four spaces (or one tab) for nested block level elements, which includes lists and sub-lists.[^qrMkdown6]

### unordered lists {: #ulists }

``` tab="Markdown"
* Unordered list can use asterisks
- Or minuses
+ Or pluses
```

``` tab="HTML"
<ul>
<li>Unordered list can use asterisks</li>
<li>Or minuses</li>
<li>Or pluses</li>
</ul>
```

!!! note ""
    
    <ul>
    <li>Unordered list can use asterisks</li>
    <li>Or minuses</li>
    <li>Or pluses</li>
    </ul>

## strikethrough {: #strikethrough }

``` tab="Markdown"
Strikethrough uses two tildes. ~~Scratch this.~~
```

``` tab="HTML"
Strikethrough uses two tildes. <del>Scratch this.</del>
```

!!! note ""
    
    Strikethrough uses two tildes. <del>Scratch this.</del>

## tables {: #tables }
Colons can be used to align columns.

``` tab="Markdown"
| Tables        | Are           | Cool  |
|---------------|:-------------:|------:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |
```

``` tab="HTML"
<table>
<thead>
<tr class="header">
<th>Tables</th>
<th style="text-align: center;">Are</th>
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
    <th>Tables</th>
    <th style="text-align: center;">Are</th>
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

## comparison of Markdown implementations

<!-- This table depends on CSS tweaks to display correctly. -->

|                                                                                       | [GitHub Flavored Markdown]                                              | [John Gruber's Markdown]                     | [Pandoc's Markdown]                        | [PyMdown]                                       | [Python-Markdown]                       |
|:--------------------------------------------------------------------------------------|:------------------------------------------------------------------------|:---------------------------------------------|:-------------------------------------------|:------------------------------------------------|:----------------------------------------|
|{: .fth } [admonitions]                                                                | no{: .no }                                                              | no{: .no }                                   | no{: .no }                                 | no{: .no }                                      | yes (with extension){: .yes }[^pynadmo] |
|{: .fth } [blockquotes]                                                                | yes{: .yes}[^gfmblkq]                                                   | yes{: .yes }[^jgmblkq]                       | yes{: .yes }[^pdmblkq]                     | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [breaks]  [(hard line, with a backslash)][hard line breaks with a backslash] | yes{: .yes}[^gfmbhlk]                                                   | no{: .no }                                   | yes (with an extension){: .yes }[^pdmbhlk] | no{: .no }                                      | no{: .no }                              |
|{: .fth } [breaks]  [(hard line, with two spaces)][hard line breaks with two spaces]   | yes{: .yes}[^gfmbhlk]                                                   | yes{: .yes} [^jgmbhls]                       | yes{: .yes }[^pdmbhlk]                     | yes{: .yes }[^pymbhls]                          | yes{: .yes }                            |
|{: .fth } [breaks]  [(thematic)][thematic break]                                       | yes{: .yes }[^gfmtbrk]                                                  | yes{: .yes }[^jgmtbrk]                       | yes{: .yes }[^pdmtbrk]                     | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [code]  [(inline)][inline code]                                              | yes{: .yes}[^gfmcodi]                                                   | yes{: .yes }[^jgmcodi]                       | yes{: .yes }[^pdmcodi]                     | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [code]  [(blocks)][blocks of code]                                           | yes{: .yes}[^gfmcodb]                                                   | partial (indent only){: .partial }[^jgmcodb] | yes (with extension){: .yes }[^pdmcodb]    | yes (with extension){: .yes }[^pymexra]         | yes (with extension){: .yes }[^pyncodb] |
|{: .fth } [emphasis]                                                                   | yes{: .yes}[^gfmemph]                                                   | yes{: .yes }[^jgmemph]                       | yes{: .yes }[^pdmemph]                     | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [footnotes]  [(inline-style)][inline-style footnote]                         | no{: .no }                                                              | no{: .no }                                   | yes (with extension){: .yes }[^pdmftnt]    | partial (with extension){: .partial }[^pymfnis] | no{: .no }[^pynfnis]                    |
|{: .fth } [footnotes]  [(reference-style)][reference-style footnote]                   | no{: .no }                                                              | no{: .no }                                   | yes (with extension){: .yes }[^pdmftnt]    | yes (with extension){: .yes }[^pymexra]         | yes (with extension){: .yes }[^pynfnrs] |
|{: .fth } [headings]                                                                   | yes{: .yes }[^gfmhdng]                                                  | yes{: .yes }[^jgmhdng]                       | yes{: .yes }[^pdmhdng]                     | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [images]                                                                     | yes{: .yes }[^gfmimag]                                                  | yes{: .yes }[^jgmimag]                       | yes{: .yes }[^pdmimag]                     | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [inline HTML]                                                                | partial (some tags are filtered out){: .partial } [^gfmhtm1] [^gfmhtm2] | yes{: .yes }[^jgmhtml]                       | yes (with extension){: .yes }[^pdmhtml]    | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [links]  [(automatic)][automatic link]                                       | yes{: .yes }[^gfmlka1] [^gfmlka2]                                       | yes{: .yes }[^jgmlkao]                       | yes{: .yes }[^pdmlkao]                     | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [links]  [(inline-style)][inline-style link]                                 | yes{: .yes }[^gfmlkis]                                                  | yes{: .yes }[^jgmlink]                       | yes{: .yes }[^pdmlkis]                     | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [links]  [(reference-style)][reference-style link]                           | yes{: .yes }[^gfmlkrs]                                                  | yes{: .yes }[^jgmlink]                       | yes{: .yes }[^pdmlkrs]                     | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [lists]  [(description lists)][description lists]                            | no{: .no }                                                              | no{: .no }                                   | yes (with extension){: .yes }[^pdmldsc]    | yes (with extension){: .yes }[^pymexra]         | yes (with extension){: .yes }[^pynldsc] |
|{: .fth } [lists]  [(ordered lists)][ordered lists]                                    | yes{: .yes }[^gfmlist]                                                  | yes{: .yes }[^jgmlist]                       | yes{: .yes }[^pdmlord]                     | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [lists]  [(unordered lists)][unordered lists]                                | yes{: .yes }[^gfmlist]                                                  | yes{: .yes }[^jgmlist]                       | yes{: .yes }[^pdmlurd]                     | yes{: .yes }                                    | yes{: .yes }                            |
|{: .fth } [strikethrough]                                                              | yes (with extension){: .yes }[^gfmstrk]                                 | no{: .no }                                   | yes (with extension){: .yes }[^pdmstrk]    | yes (with extension){: .yes }[^pymtlde]         | no{: .no }                              |
|{: .fth } [tables]                                                                     | yes (with extension){: .yes }[^gfmtabl]                                 | no{: .no }                                   | yes (with extension){: .yes }[^pdmtabl]    | yes (with extension){: .yes }[^pymexra]         | yes (with extension){: .yes }[^pyntabl] |

[admonitions]: #admonitions
[automatic link]: #alink
[blockquotes]: #blockquotes
[blocks of code]: #bcode
[breaks]: #breaks
[code]: #code
[description lists]: #dlists
[emphasis]: #emphasis
[footnotes]: #footnotes
[hard line breaks with a backslash]: #hlbreakbslash
[hard line breaks with two spaces]: #hlbreaktwospace
[headings]: #headings
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
[thematic break]: #tbreak
[unordered lists]: #ulists
[GitHub Flavored Markdown]: https://github.github.com/gfm/
[John Gruber's Markdown]: https://daringfireball.net/projects/markdown/syntax
[Pandoc's Markdown]: https://pandoc.org/MANUAL.html#pandocs-markdown
[PyMdown]: https://facelessuser.github.io/PyMdown/
[Python-Markdown]: https://python-markdown.github.io/
[^gfmblkq]: https://github.github.com/gfm/#block-quotes
[^gfmbhlk]: https://github.github.com/gfm/#hard-line-break
[^gfmcodb]: https://github.github.com/gfm/#fenced-code-blocks
[^gfmcodi]: https://github.github.com/gfm/#code-spans
[^gfmemph]: https://github.github.com/gfm/#emphasis-and-strong-emphasis
[^gfmhdng]: https://github.github.com/gfm/#atx-headings
[^gfmhtm1]: https://github.github.com/gfm/#raw-html
[^gfmhtm2]: https://github.github.com/gfm/#disallowed-raw-html-extension-
[^gfmimag]: https://github.github.com/gfm/#images
[^gfmlist]: https://github.github.com/gfm/#lists
[^gfmlka1]: https://github.github.com/gfm/#autolink
[^gfmlka2]: https://github.github.com/gfm/#autolinks-extension-
[^gfmlkis]: https://github.github.com/gfm/#links
[^gfmlkrs]: https://github.github.com/gfm/#link-reference-definitions
[^gfmstrk]: https://github.github.com/gfm/#strikethrough-extension-
[^gfmtabl]: https://github.github.com/gfm/#tables-extension-
[^gfmtbrk]: https://github.github.com/gfm/#thematic-break
[^jgmbhls]: https://daringfireball.net/projects/markdown/syntax#p
[^jgmblkq]: https://daringfireball.net/projects/markdown/syntax#blockquote
[^jgmcodb]: https://daringfireball.net/projects/markdown/syntax#precode
[^jgmcodi]: https://daringfireball.net/projects/markdown/syntax#code
[^jgmemph]: https://daringfireball.net/projects/markdown/syntax#em
[^jgmhdng]: https://daringfireball.net/projects/markdown/syntax#header
[^jgmhtml]: https://daringfireball.net/projects/markdown/syntax#html
[^jgmimag]: https://daringfireball.net/projects/markdown/syntax#img
[^jgmlink]: https://daringfireball.net/projects/markdown/syntax#link
[^jgmlist]: https://daringfireball.net/projects/markdown/syntax#list
[^jgmlkao]: https://daringfireball.net/projects/markdown/syntax#autolink
[^jgmtbrk]: https://daringfireball.net/projects/markdown/syntax#hr
[^pdmbhlk]: https://pandoc.org/MANUAL.html#paragraphs
[^pdmblkq]: https://pandoc.org/MANUAL.html#block-quotations
[^pdmcodb]: https://pandoc.org/MANUAL.html#verbatim-code-blocks
[^pdmcodi]: https://pandoc.org/MANUAL.html#verbatim
[^pdmemph]: https://pandoc.org/MANUAL.html#emphasis
[^pdmftnt]: https://pandoc.org/MANUAL.html#footnotes
[^pdmhdng]: https://pandoc.org/MANUAL.html#headers
[^pdmhtml]: https://pandoc.org/MANUAL.html#raw-html
[^pdmimag]: https://pandoc.org/MANUAL.html#images
[^pdmldsc]: https://pandoc.org/MANUAL.html#definition-lists
[^pdmlkao]: https://pandoc.org/MANUAL.html#automatic-links
[^pdmlkis]: https://pandoc.org/MANUAL.html#inline-links
[^pdmlkrs]: https://pandoc.org/MANUAL.html#reference-links
[^pdmlord]: https://pandoc.org/MANUAL.html#ordered-lists
[^pdmlurd]: https://pandoc.org/MANUAL.html#bullet-lists
[^pdmstrk]: https://pandoc.org/MANUAL.html#strikeout
[^pdmtabl]: https://pandoc.org/MANUAL.html#tables
[^pdmtbrk]: https://pandoc.org/MANUAL.html#horizontal-rules
[^pymbhls]: https://facelessuser.github.io/PyMdown/user-guide/markdown-syntax/#p
[^pymexra]: https://facelessuser.github.io/pymdown-extensions/extensions/extra/
[^pymfnis]: Inline-style footnotes can be approximated using the [Caret extension](https://facelessuser.github.io/pymdown-extensions/extensions/caret/) to create numbered superscripts and an ordered list. Links between the superscript and footnote will not be available.
[^pymtlde]: https://facelessuser.github.io/pymdown-extensions/extensions/tilde/
[^pynadmo]: https://python-markdown.github.io/extensions/admonition/
[^pyncodb]: https://python-markdown.github.io/extensions/fenced_code_blocks/
[^pynfnis]: https://github.com/Python-Markdown/markdown/issues/658
[^pynfnrs]: https://python-markdown.github.io/extensions/footnotes/
[^pynldsc]: https://python-markdown.github.io/extensions/definition_lists/
[^pyntabl]: https://python-markdown.github.io/extensions/tables/

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
The bulk of the instructions were introduced to me through [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet), part of the [Markdown Here](https://github.com/adam-p/markdown-here) [wiki](https://github.com/adam-p/markdown-here/wiki) on GitHub.

[Markdown]: https://en.wikipedia.org/wiki/Markdown
[^jgmblkq]: https://daringfireball.net/projects/markdown/syntax#blockquote
[^qrMkdown1]: https://github.com/squidfunk/mkdocs-material/issues/179#issuecomment-282027581
[^qrMkdown2]: https://stackoverflow.com/questions/7579826/which-semantic-html-tag-for-displaying-side-notes-and-admonitions/7579894#7579894
[^qrMkdown3]: https://stackoverflow.com/questions/7579826/which-semantic-html-tag-for-displaying-side-notes-and-admonitions/8297157#8297157
[^qrMkdown4]: https://en.wikipedia.org/wiki/Note_(typography)#HTML
[^qrMkdown5]: https://python-markdown.github.io/extensions/footnotes/#syntax
[^qrMkdown6]: https://python-markdown.github.io/#differences

