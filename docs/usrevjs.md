# using [reveal.js]

!!! note
    
    reveal.js can function as a self-contained program running from local files in the browser, but only [in a limited way](https://github.com/hakimel/reveal.js/#basic-setup). Complete functionality like [loading slides from a separate Markdown file](https://github.com/hakimel/reveal.js/#external-markdown) and [adding audio playback](https://github.com/rajgoel/reveal.js-plugins/tree/master/audio-slideshow) requires running it from a local or remote server.

reveal.js can be downloaded with [Git](instGit.md) using `git clone https://github.com/hakimel/reveal.js.git && cd reveal.js`. `git clone https://github.com/hakimel/reveal.js.git` clones the reveal.js repository and `cd reveal.js` navigates to the reveal.js folder. It can also be downloaded directly from GitHub using the ++"Clone or download"++ button.

Slides can be written using Markdown formatting either within *index.html* or as a separate file.

## self-contained usage
### [Markdown within *index.html*]
For slides within *index.html*, wrap the Markdown-formatted text in `textarea` elements with the `data-template` attribute, and in turn wrap those in `section` HTML elements with the `data-markdown` attribute. The `plugin/markdown/marked.js` and `plugin/markdown/markdown.js` scripts will also need to be added to *index.html*. An example:

```
<section data-markdown>
  <textarea data-template>
    ## Page title

    A paragraph with some text and a [link](http://hakim.se).
  </textarea>
</section>
```

## server-based usage
In Kubuntu, running reveal.js from a local web server requires [npm](inNjspv.md). From within the reveal.js directory, use `npm install` **after each modification** to install dependencies, and `npm start` to serve the presentation and monitor the source files for changes.

!!! attention
    
    If an error message similar to `grunt: not found` is encountered, try running reveal.js from the home directory.

### [separate Markdown file]
For slides written in a separate file with Markdown-formatted text, add the following to *index.html*:

```
<section data-markdown="example.md"
         data-separator="^<!-- reveal.js horizontal slide -->"
         data-separator-vertical="^\n\n"
         data-separator-notes="^Note:"
         data-charset="iso-8859-15">
</section>
```

!!! note
    Windows uses `\r\n` instead of `\n` as its linefeed character. For a regex that supports all operating systems, use `\r?\n` instead of `\n`.

#### explanation
- The `data-markdown` attribute specifies the path to the separate file with Markdown-formatted text.
- The `data-separator` attribute defines how horizontal slides are delimited in the separate file using a regular expression. It defaults to `^\r?\n---\r?\n$`, a newline-bounded horizontal rule.
- The `data-separator-vertical` attribute defines how vertical slides are delimited in the separate file using a regular expression.
- The `data-separator-notes` attribute is a regular expression for specifying the beginning of the current slide's speaker notes. It defaults to `notes?:`, so it will match both *note:* and *notes:*.
- The `data-charset` attribute is optional and specifies which charset to use when loading the external file.

### [slideout menu]
To add a slideout menu (accessible with a [hamburger button](https://en.wikipedia.org/wiki/Hamburger_button)), download [the latest release of reveal.js-menu plugin](https://github.com/denehyg/reveal.js-menu/releases/latest), extract it to `plugin/menu`, and add the following to `index.html` within `dependencies: [`, within `Reveal.initialize({`, within a `script` HTML element:

```
{ src: 'plugin/menu/menu.js' }
```

It may also be necessary to add a comma at the end if other dependencies are present.

## licensing
**Some rights reserved: MIT License.** Includes significant content from [the reveal.js README on GitHub](https://github.com/hakimel/reveal.js/), with changes made.

??? note "[MIT License](https://choosealicense.com/licenses/mit/) for reveal.js[^usrevjs1]"
    
    Copyright (C) 2018 Hakim El Hattab, http://hakim.se, and reveal.js contributors
    
    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:
    
    The above copyright notice and this permission notice shall be included in
    all copies or substantial portions of the Software.
    
    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
    THE SOFTWARE.

## prior work
The method of installing [the reveal.js-menu plugin](https://github.com/denehyg/reveal.js-menu/) was introduced to me by [the Manual section of the reveal.js-menu plugin README on GitHub](https://github.com/denehyg/reveal.js-menu/#manual).

[Markdown within *index.html*]: https://github.com/hakimel/reveal.js/#markdown
[reveal.js]: https://revealjs.com/
[separate Markdown file]: https://github.com/hakimel/reveal.js/#external-markdown
[slideout menu]: https://github.com/denehyg/reveal.js-menu
[^usrevjs1]: https://github.com/hakimel/reveal.js/blob/master/LICENSE
