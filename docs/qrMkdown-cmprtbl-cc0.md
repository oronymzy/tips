<table>
  <tr>
    <th></th>
    <th>[John Gruber’s<br>Markdown]</th>
    <th>[Pandoc's Markdown]</th>
    <th>[PyMdown]</th>
    <th>[Python-Markdown]</th>
  </tr>
  <tr>
    <th>[blockquotes]</th>
    <td class="yes">yes[^jgmblkq]</td>
    <td class="yes">yes[^pdmblkq]</td>
    <td class="yes">yes</td>
    <td class="yes">yes</td>
  </tr>
  <tr>
    <th>[code] ([inline])</th>
    <td class="yes">yes[^jgmcodi]</td>
    <td class="yes">yes[^pdmcodi]</td>
    <td class="yes">yes</td>
    <td class="yes">yes</td>
  </tr>
  <tr>
    <th>[code] ([blocks])</th>
    <td class="partial">partial (indent only)[^jgmcodb]</td>
    <td class="yes">yes (with extension)[^pdmcodb]</td>
    <td class="yes">yes (with extension)[^pymexra]</td>
    <td class="yes">yes (with extension)[^pyncodb]</td>
  </tr>
  <tr>
    <th>[emphasis]</th>
    <td class="yes">yes[^jgmemph]</td>
    <td class="yes">yes[^pdmemph]</td>
    <td class="yes">yes</td>
    <td class="yes">yes</td>
  </tr>
  <tr>
    <th>[footnotes] ([inline-style][inline-style footnote])</th>
    <td class="no">no</td>
    <td class="yes">yes (with extension)[^pdmftnt]</td>
    <td class="partial">partial (with extension)[^pymfnis]</td>
    <td class="no">no[^pynfnis]</td>
  </tr>
  <tr>
    <th>[footnotes] ([reference-style][reference-style footnote])</th>
    <td class="no">no</td>
    <td class="yes">yes (with extension)[^pdmftnt]</td>
    <td class="yes">yes (with extension)[^pymexra]</td>
    <td class="yes">yes (with extension)[^pynfnrs]</td>
  </tr>
  <tr>
    <th>[headings]</th>
    <td class="yes">yes[^jgmhdng]</td>
    <td class="yes">yes[^pdmhdng]</td>
    <td class="yes">yes</td>
    <td class="yes">yes</td>
  </tr>
  <tr>
    <th>[horizontal rules]</th>
    <td class="yes">yes[^jgmhzrl]</td>
    <td class="yes">yes[^pdmhzrl]</td>
    <td class="yes">yes</td>
    <td class="yes">yes</td>
  </tr>
  <tr>
    <th>[images]</th>
    <td class="yes">yes[^jgmimag]</td>
    <td class="yes">yes[^pdmimag]</td>
    <td class="yes">yes</td>
    <td class="yes">yes</td>
  </tr>
  <tr>
    <th>[inline HTML]</th>
    <td class="yes">yes[^jgmhtml]</td>
    <td class="yes">yes (with extension)[^pdmhtml]</td>
    <td class="yes">yes</td>
    <td class="yes">yes</td>
  </tr>
  <tr>
    <th>[links] ([automatic][automatic link])</th>
    <td class="yes">yes[^jgmlkao]</td>
    <td class="yes">yes[^pdmlkao]</td>
    <td class="yes">yes</td>
    <td class="yes">yes</td>
  </tr>
  <tr>
    <th>[links] ([inline-style][inline-style link])</th>
    <td class="yes">yes[^jgmlink]</td>
    <td class="yes">yes[^pdmlkis]</td>
    <td class="yes">yes</td>
    <td class="yes">yes</td>
  </tr>
  <tr>
    <th>[links] ([reference-style][reference-style link])</th>
    <td class="yes">yes[^jgmlink]</td>
    <td class="yes">yes[^pdmlkrs]</td>
    <td class="yes">yes</td>
    <td class="yes">yes</td>
  </tr>
  <tr>
    <th>[lists] ([description lists])</th>
    <td class="no">no</td>
    <td class="yes">yes (with extension)[^pdmldsc]</td>
    <td class="yes">yes (with extension)[^pymexra]</td>
    <td class="yes">yes (with extension)[^pynldsc]</td>
  </tr>
  <tr>
    <th>[lists] ([ordered lists])</th>
    <td class="yes">yes[^jgmlist]</td>
    <td class="yes">yes[^pdmlord]</td>
    <td class="yes">yes</td>
    <td class="yes">yes</td>
  </tr>
  <tr>
    <th>[lists] ([unordered lists])</th>
    <td class="yes">yes[^jgmlist]</td>
    <td class="yes">yes[^pdmlurd]</td>
    <td class="yes">yes</td>
    <td class="yes">yes</td>
  </tr>
  <tr>
    <th>[strikethrough]</th>
    <td class="no">no</td>
    <td class="yes">yes (with extension)[^pdmstrk]</td>
    <td class="yes">yes (with extension)[^pymtlde]</td>
    <td class="no">no</td>
  </tr>
  <tr>
    <th>[tables]</th>
    <td class="no">no</td>
    <td class="yes">yes (with<br>*pipe tables*<br>extension)[^pdmtabl]</td>
    <td class="yes">yes (with extension)[^pymexra]</td>
    <td class="yes">yes (with extension)[^pyntabl]</td>
  </tr>
</table>

[automatic link]: #alink
[blockquotes]: #blockquotes
[blocks]: #bcode
[code]: #code
[description lists]: #dlists
[emphasis]: #emphasis
[footnotes]: #footnotes
[headings]: #headings
[horizontal rules]: #hrule
[images]: #images
[inline]: #icode
[inline-style footnote]: #ifootnote
[inline-style link]: #ilink
[inline HTML]: #html
[links]: #links
[lists]: #lists
[ordered lists]: #olists
[reference-style footnote]: #rfootnote
[reference-style link]: #rlink
[strikethrough]: #strikethrough
[tables]: #tables
[unordered lists]: #ulists
[John Gruber’s<br>Markdown]: https://daringfireball.net/projects/markdown/syntax
[Pandoc's Markdown]: https://pandoc.org/MANUAL.html#pandocs-markdown
[PyMdown]: https://facelessuser.github.io/PyMdown/
[Python-Markdown]: https://python-markdown.github.io/
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
