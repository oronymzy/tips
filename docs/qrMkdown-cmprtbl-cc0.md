<table>
  <tr>
    <th></th>
    <th>[John Gruber’s<br>Markdown]</th>
    <th>[Pandoc's Markdown]</th>
    <th>[Python-Markdown]</th>
  </tr>
  <tr>
    <th>footnotes</th>
    <td class="no">no</td>
    <td class="yes">yes (with extension)[^pdmftnt]</td>
    <td class="yes">yes (with extension)[^pymftnt]</td>
  </tr>
  <tr>
    <th>[headings]</th>
    <td class="yes">yes[^jgmhdng]</td>
    <td class="yes">yes[^pdmhdng]</td>
    <td class="yes">yes</td>
  </tr>
  <tr>
    <th>[links] (inline-style)</th>
    <td class="yes">yes[^jgmlink]</td>
    <td class="yes">yes[^pdmlkis]</td>
    <td class="yes">yes</td>
  </tr>
  <tr>
    <th>[links] (reference-style)</th>
    <td class="yes">yes[^jgmlink]</td>
    <td class="yes">yes[^pdmlkrs]</td>
    <td class="yes">yes</td>
  </tr>
  <tr>
    <th>[lists] ([description lists])</th>
    <td class="no">no</td>
    <td class="yes">yes (with extension)[^pdmldsc]</td>
    <td class="yes">yes (with extension)[^pymldsc]</td>
  </tr>
  <tr>
    <th>[lists] ([ordered lists])</th>
    <td class="yes">yes[^jgmlist]</td>
    <td class="yes">yes[^pdmlord]</td>
    <td class="yes">yes</td>
  </tr>
  <tr>
    <th>[lists] ([unordered lists])</th>
    <td class="yes">yes[^jgmlist]</td>
    <td class="yes">yes[^pdmlurd]</td>
    <td class="yes">yes</td>
  </tr>
  <tr>
    <th>[tables]</th>
    <td class="no">no</td>
    <td class="yes">yes (with<br>*pipe tables*<br>extension)[^pdmtabl]</td>
    <td class="yes">yes (with extension)[^pymtabl]</td>
  </tr>
</table>

[description lists]: #dlists
[headings]: #headings
[links]: #links
[lists]: #lists
[ordered lists]: #olists
[tables]: #tables
[unordered lists]: #ulists
[John Gruber’s<br>Markdown]: https://daringfireball.net/projects/markdown/syntax
[Pandoc's Markdown]: https://pandoc.org/MANUAL.html#pandocs-markdown
[Python-Markdown]: https://python-markdown.github.io/
[^jgmhdng]: https://daringfireball.net/projects/markdown/syntax#header
[^jgmlink]: https://daringfireball.net/projects/markdown/syntax#link
[^jgmlist]: https://daringfireball.net/projects/markdown/syntax#list
[^pymftnt]: https://python-markdown.github.io/extensions/footnotes/
[^pymldsc]: https://python-markdown.github.io/extensions/definition_lists/
[^pymtabl]: https://python-markdown.github.io/extensions/tables/
[^pdmftnt]: https://pandoc.org/MANUAL.html#footnotes
[^pdmhdng]: https://pandoc.org/MANUAL.html#headers
[^pdmldsc]: https://pandoc.org/MANUAL.html#definition-lists
[^pdmlkis]: https://pandoc.org/MANUAL.html#inline-links
[^pdmlkrs]: https://pandoc.org/MANUAL.html#reference-links
[^pdmlord]: https://pandoc.org/MANUAL.html#ordered-lists
[^pdmlurd]: https://pandoc.org/MANUAL.html#bullet-lists
[^pdmtabl]: https://pandoc.org/MANUAL.html#tables
