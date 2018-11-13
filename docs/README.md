# Oronymzy's tips

Hope you find them useful.

!!! info
    This site came about from my habit of [information grazing](https://en.wikipedia.org/wiki/Information_grazing), and serves as a way of documenting information I tend to quickly forget.

!!! note
    [MkDocs](https://www.mkdocs.org/) pages are designed to be generated from [Python-Markdown](https://python-markdown.github.io/)-formatted text files[^Orotips1], but I tend to use [Pandoc Markdown](http://pandoc.org/MANUAL.html#pandocs-markdown), and I'm also using [PyMdown Extensions](https://facelessuser.github.io/pymdown-extensions/), so it's a bit of a mess.

## disclosure of bias
My operating system of choice is [Kubuntu](https://kubuntu.org/) for desktop and laptop computers and [Android](https://en.wikipedia.org/wiki/Android_(operating_system)) for mobile devices. These operating systems are both (arguably) [Linux distributions](https://en.wikipedia.org/wiki/Linux_distribution), and are therefore [Unix-like](https://en.wikipedia.org/wiki/Unix-like). Consequently, much material relies on the [Unix shell](https://en.wikipedia.org/wiki/Unix_shell), though some material will use a graphical user interface. Proprietary operating systems like Windows and Mac will appear only occasionally. There is also an almost exclusive use of permissively-licensed software, even to the point of sacrificing functionality. The rationale for this is sustainability, as proprietary tools often become obsolete or inaccessible with no recourse for the user.

## license
All content is licensed [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) **unless otherwise noted**, and will always be more permissive than all rights reserved. The *licensing* heading denotes the license for each page. Additionally, the website generated from the content falls under the following licenses:

??? note "[BSD 2-Clause “Simplified” License](https://choosealicense.com/licenses/bsd-2-clause/) for [MkDocs](https://www.mkdocs.org/) [^Orotips2] [^Orotips3]"
    
    Copyright © 2014, Tom Christie. All rights reserved.
    
    Redistribution and use in source and binary forms, with or
    without modification, are permitted provided that the following
    conditions are met:
    
    Redistributions of source code must retain the above copyright
    notice, this list of conditions and the following disclaimer.
    Redistributions in binary form must reproduce the above copyright
    notice, this list of conditions and the following disclaimer in
    the documentation and/or other materials provided with the
    distribution.
    
    THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND
    CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES,
    INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
    MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
    DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR
    CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
    SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
    LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF
    USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED
    AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT
    LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN
    ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE
    POSSIBILITY OF SUCH DAMAGE.

??? note "[MIT License](https://choosealicense.com/licenses/mit/) for [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) [^Orotips4]"
    
    Copyright (c) 2016-2018 Martin Donath <martin.donath@squidfunk.com>
    
    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to
    deal in the Software without restriction, including without limitation the
    rights to use, copy, modify, merge, publish, distribute, sublicense, and/or
    sell copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:
    
    The above copyright notice and this permission notice shall be included in
    all copies or substantial portions of the Software.
    
    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NON-INFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
    FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS
    IN THE SOFTWARE.

## prior work
The following additions to `mkdocs.yml`:

```
markdown_extensions:
  - admonition
  - def_list
  - footnotes
  - markdown.extensions.attr_list
  - pymdownx.details
  - pymdownx.keys
  - pymdownx.tilde
extra:
  social:
    - type: 'github'
      link: 'https://github.com/oronymzy'
repo_name: 'oronymzy/oronymzy.tips'
repo_url: 'https://github.com/oronymzy/oronymzy.tips'
edit_uri: ''
```

were introduced to me by [Adding a source repository], [Adding social links], [Admonition], [Attribute Lists], [Definition Lists], [Footnotes], [Keys], [Tilde], and [PyMdown Extensions].

## regarding prior work
I will always make an effort to recognize prior work, regardless of licensing, and I hope others will do the same as we all [share knowledge](https://en.wikipedia.org/wiki/Knowledge_sharing) together.

[Adding a source repository]: https://squidfunk.github.io/mkdocs-material/getting-started/#adding-a-source-repository
[Adding social links]: https://squidfunk.github.io/mkdocs-material/getting-started/#adding-social-links
[Admonition]: https://squidfunk.github.io/mkdocs-material/extensions/admonition/#installation
[Attribute Lists]: https://python-markdown.github.io/extensions/attr_list/
[Definition Lists]: https://python-markdown.github.io/extensions/definition_lists/
[Footnotes]: https://squidfunk.github.io/mkdocs-material/extensions/footnotes/#installation
[Keys]: https://facelessuser.github.io/pymdown-extensions/extensions/keys/
[PyMdown Extensions]: https://squidfunk.github.io/mkdocs-material/extensions/pymdown/#installation
[Tilde]: https://facelessuser.github.io/pymdown-extensions/extensions/tilde/
[^Orotips1]: https://www.mkdocs.org/user-guide/writing-your-docs/#writing-with-markdown
[^Orotips2]: https://www.mkdocs.org/about/license/
[^Orotips3]: https://github.com/mkdocs/mkdocs/blob/master/LICENSE
[^Orotips4]: https://github.com/squidfunk/mkdocs-material/blob/master/LICENSE
