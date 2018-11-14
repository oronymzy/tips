# quick reference for [Markdown]

This is intended as a quick reference and showcase. For more complete info, see [John Gruber's original spec](http://daringfireball.net/projects/markdown/).

## headings {: #headings }

```no-highlight
# H1
## H2
### H3
#### H4
##### H5
###### H6
```

Alternatively, for H1 and H2, an underline-ish style:

```no-highlight
Alt-H1
======

Alt-H2
------
```

# H1
## H2
### H3
#### H4
##### H5
###### H6

Alternatively, for H1 and H2, an underline-ish style:

Alt-H1
======

Alt-H2
------

## emphasis {: #emphasis }

```no-highlight
Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

Combined emphasis with **asterisks and _underscores_**.

Strikethrough uses two tildes. ~~Scratch this.~~
```

Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

Combined emphasis with **asterisks and _underscores_**.

Strikethrough uses two tildes. ~~Scratch this.~~

## lists {: #lists }

!!! note
    
    Leading and trailing spaces are shown with dots (`⋅`).

```no-highlight
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

* Unordered list can use asterisks
- Or minuses
+ Or pluses
```

1. First ordered list item
2. Another item
    * Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
    1. Ordered sub-list
4. And another item.

    You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces.
    
    To have a line break without a paragraph, you will need to use two trailing spaces.
    Note that this line is separate, but within the same paragraph.

* Unordered list can use asterisks
- Or minuses
+ Or pluses

!!! attention
    
    [Python-Markdown](https://python-markdown.github.io/) expects an indentation of four spaces (or one tab) for nested block level elements, which includes lists and sub-lists.[^qrMkdown1]

## links {: #links }

!!! attention
    
    Because reference-style links do not work within admonitions, several *Result* admonitions contain raw Markdown formatted differently than in the example, with reference-style links replaced with inline-style links.

There are two ways to create links:

```
[inline-style](https://www.google.com)
```
??? tip "Result"
    
    [inline-style](https://www.google.com)
and
```
[reference-style]
```
??? tip "Result"
    
    [reference-style](https://www.google.com)
  
alternately, reference-style links can be created like this:

```
[alternate reference-style link][link definition]
```
In either case, the link definition for a reference-style link is included separately, usually at the bottom of the document:
```
[link definition]: https://www.google.com
[reference-style]: https://www.google.com
```
A more detailed example:
```no-highlight
[I'm an inline-style link](https://www.google.com)

[I'm an inline-style link with title](https://www.google.com "Google's Homepage")

[I'm a reference-style link][Arbitrary case-insensitive reference text]

[I'm a relative reference to a repository file](../blob/master/LICENSE)

[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself].

URLs in angle brackets will automatically get turned into links: <http://www.example.com>

Some text to show that the reference links can follow later.

[1]: http://slashdot.org
[arbitrary case-insensitive reference text]: https://www.mozilla.org
[link text itself]: http://www.reddit.com
```

??? tip "Result"
    
    [I'm an inline-style link](https://www.google.com)
    
    [I'm an inline-style link with title](https://www.google.com "Google's Homepage")
    
    [I'm a reference-style link](https://www.mozilla.org)
    
    [I'm a relative reference to a repository file](../blob/master/LICENSE)
    
    [You can use numbers for reference-style link definitions](http://slashdot.org)
    
    Or leave it empty and use the [link text itself](http://www.reddit.com).
    
    URLs in angle brackets will automatically get turned into links: <http://www.example.com>
    
    Some text to show that the reference links can follow later.

## images {: #images }

```no-highlight
Here's our logo (hover to see the title text):

Inline-style: 
![alt text](qrMkdwn.png "Logo Title Text 1")

Reference-style: 
![alt text][logo]

[logo]: qrMkdwn.png "Logo Title Text 2"
```

Here's our logo (hover to see the title text):

Inline-style: 
![alt text](qrMkdwn.png "Logo Title Text 1")

Reference-style: 
![alt text][logo]

[logo]: qrMkdwn.png "Logo Title Text 2"

## code and syntax highlighting {: #code }

Code blocks are part of the Markdown spec, but syntax highlighting isn't. However, many renderers -- like Github's and *Markdown Here* -- support syntax highlighting. Which languages are supported and how those language names should be written will vary from renderer to renderer.

```no-highlight
Inline `code` has `back-ticks around` it.
```

Inline `code` has `back-ticks around` it.

Blocks of code are either fenced by lines with three back-ticks <code>```</code>, or are indented with four spaces.

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

Colons can be used to align columns.

| Tables        | Are           | Cool  |
|---------------|:-------------:|------:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

```
The table will render correctly even if the raw Markdown does not line up prettily. The rightmost pipe (`|`) and any extra spaces can be omitted, and only one dash is required to separate each header cell. You can also use inline Markdown.

| Markdown | Less | Pretty
|-|-|-
| *Still* | `renders` | **nicely**
| 1 | 2 | 3
```

The table will render correctly even if the raw Markdown does not line up prettily. The rightmost pipe (`|`) and any extra spaces can be omitted, and only one dash is required to separate each header cell. You can also use inline Markdown.

| Markdown | Less | Pretty
|-|-|-
| *Still* | `renders` | **nicely**
| 1 | 2 | 3

## blockquotes {: #blockquotes }

```no-highlight
> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote.
```

> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote.

## inline HTML {: #html }

You can also use raw HTML in your Markdown, and it'll mostly work pretty well. 

```no-highlight
<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>

  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl>
```

<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>

  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl>

## horizontal rule {: #hr }

```
Three or more...

---

Hyphens

***

Asterisks

___

Underscores
```

Three or more...

---

Hyphens

***

Asterisks

___

Underscores

## line breaks {: #lines }

!!! note
    
    Leading and trailing spaces are shown with dots (`⋅`).

Try experimenting to learn how line breaks work -- hit ++enter++ once (i.e., insert one newline), then hit it twice (i.e., insert two newlines), and see what happens.

Here are some things to try out:

```
Here's a line for us to start with.

This line is separated from the one above by two newlines, so it will be a *separate paragraph*.

This line is also a separate paragraph, but...⋅⋅
This line is separated by a single newline and two spaces, so it's a separate line in the *same paragraph*.
```

Here's a line for us to start with.

This line is separated from the one above by two newlines, so it will be a *separate paragraph*.

This line is also a separate paragraph, but...  
This line is separated by a single newline and two spaces, so it's a separate line in the *same paragraph*.

!!! note
    
    Most Markdown implementations require lines on the same paragraph to be separated by **two spaces** just before the newline, but ending a line with a backslash (`\`) is also supported by [Pandoc's Markdown] (with an extension)[^qrMkdown2].

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
[Pandoc's Markdown]: https://pandoc.org/MANUAL.html#pandocs-markdown
[^qrMkdown1]: https://python-markdown.github.io/#differences
[^qrMkdown2]: https://pandoc.org/MANUAL.html#paragraphs
