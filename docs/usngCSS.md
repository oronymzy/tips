# using [CSS]

Use `h1,h2,h3,h4,h5,h6 {foo:bar}` to apply the *foo:bar* declaration to HTML heading elements at all six levels.

There is no way to block inheritance of styles in CSS. Inheritance is related to cascading, and cascading is intrinsic to CSS.

There is currently no way to select the parent of an element in CSS.

## [pseudo-classes]
### [:has()]
[According to the MDN wiki](https://developer.mozilla.org/en-US/docs/Web/CSS/:has), the **`:has()`** CSS [pseudo-class](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes) represents an element if any of the selectors passed as parameters (relative to the [`:scope`](https://developer.mozilla.org/en-US/docs/Web/CSS/:scope) of the given element), match at least one element.

The `:has()` pseudo-class takes a selector list as an argument. In the current specification `:has` is not marked as part of the [live selector profile](https://drafts.csswg.org/selectors/#live-profile), which means it can not be used within stylesheets; only with functions like [`document.querySelector()`](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector).

```
/* Selects any <a>, as long as it has an <img> element directly inside it  */
/* Note that this is not supported in any browser yet */
/* It also isn't intended to work in stylesheets */
var test = document.querySelector('a:has(> img)');
```

## preprocessors
### [Less]
[According to Wikipedia](https://en.wikipedia.org/wiki/Less_(stylesheet_language)), Less is a dynamic [preprocessor](https://en.wikipedia.org/wiki/Preprocessor) [style sheet language](https://en.wikipedia.org/wiki/Style_sheet_language) that can be compiled into [Cascading Style Sheets](https://en.wikipedia.org/wiki/Cascading_Style_Sheets) (CSS) and run on the client side or server side.[^usngCSS1]

### [Sass]
[According to Wikipedia], Sass is a [preprocessor](https://en.wikipedia.org/wiki/Preprocessor) [scripting language](https://en.wikipedia.org/wiki/Scripting_language) that is [interpreted](https://en.wikipedia.org/wiki/Interpreted_language) or [compiled](https://en.wikipedia.org/wiki/Compiled_language) into [Cascading Style Sheets](https://en.wikipedia.org/wiki/Cascading_Style_Sheets) (CSS). SassScript is the scripting language itself. Sass consists of two [syntaxes](https://en.wikipedia.org/wiki/Syntax_(programming_languages)). The original syntax, called "the indented syntax", uses a syntax similar to [Haml](https://en.wikipedia.org/wiki/Haml).[^usngCSS2] It uses [indentation](https://en.wikipedia.org/wiki/Indent_style) to separate [code blocks](https://en.wikipedia.org/wiki/Block_(programming)) and [newline](https://en.wikipedia.org/wiki/Newline) characters to separate rules. The newer syntax, "SCSS" (Sassy CSS), uses block formatting like that of CSS. It uses braces to denote code blocks and semicolons to separate lines within a block. The indented syntax and SCSS files are traditionally given the [extensions](https://en.wikipedia.org/wiki/Filename_extension) `.sass` and `.scss`, respectively.

#### Bourbon
Bourbon is a library of [Sass](http://sass-lang.com/) mixins and functions that are designed to make you a more efficient style sheet author.

#### Compass
Compass is a deprecated[^usngCSS3] CSS preprocessor that uses Sass.

### [Stylus]
Stylus is a CSS preprocessor that supports both an indented syntax and regular CSS style.

## licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Includes significant content from:
- [Less (stylesheet language)](https://en.wikipedia.org/w/index.php?title=Less_(stylesheet_language)&oldid=865608252)
- [Sass (stylesheet language)](https://en.wikipedia.org/w/index.php?title=Sass_(stylesheet_language)&oldid=872633192)
on Wikipedia, with changes made.

Also includes significant content from [an answer on Stack Overflow by Dan Herbert](https://stackoverflow.com/questions/1014861/is-there-a-css-parent-selector/1014958#1014958).

### compatible but superseded licensing, included for attribution
**Some rights reserved: [CC BY-SA 2.5](https://creativecommons.org/licenses/by-sa/2.5/) or later.** Includes significant content from [:has()](https://developer.mozilla.org/en-US/docs/Web/CSS/:has$revision/1412251) by Mozilla Contributors, with changes made.

**Some rights reserved: MIT License.** Includes significant content from [the Bourbon README on GitHub](https://github.com/thoughtbot/bourbon/blob/master/README.md), with changes made.

??? note "[MIT License](https://choosealicense.com/licenses/mit/) for Bourbon[^usngCSS4]"
    
    The MIT License (MIT)
    
    Copyright © 2011-2018 [thoughtbot, inc.](http://thoughtbot.com)
    
    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the “Software”), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:
    
    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.
    
    THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.

    (The MIT License)
    
    Copyright (c) Automattic <developer.wordpress.com>
    
    Permission is hereby granted, free of charge, to any person obtaining
    a copy of this software and associated documentation files (the
    'Software'), to deal in the Software without restriction, including
    without limitation the rights to use, copy, modify, merge, publish,
    distribute, sublicense, and/or sell copies of the Software, and to
    permit persons to whom the Software is furnished to do so, subject to
    the following conditions:
    
    The above copyright notice and this permission notice shall be
    included in all copies or substantial portions of the Software.
    
    THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
    EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
    MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
    IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
    CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
    TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
    SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

??? note "[MIT License](https://choosealicense.com/licenses/mit/) for Stylus[^usngCSS5]"
    
    (The MIT License)
    
    Copyright (c) Automattic <developer.wordpress.com>
    
    Permission is hereby granted, free of charge, to any person obtaining
    a copy of this software and associated documentation files (the
    'Software'), to deal in the Software without restriction, including
    without limitation the rights to use, copy, modify, merge, publish,
    distribute, sublicense, and/or sell copies of the Software, and to
    permit persons to whom the Software is furnished to do so, subject to
    the following conditions:
    
    The above copyright notice and this permission notice shall be
    included in all copies or substantial portions of the Software.
    
    THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
    EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
    MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
    IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
    CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
    TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
    SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## prior work
- The fact that there is no more efficient way to apply the contents of a declaration block to HTML heading elements on all six levels than to list them all individually was introduced to me by [an answer on Stack Overflow by Dave Markle](https://stackoverflow.com/questions/7539125/can-i-target-all-h-tags-with-a-single-selector/7539138#7539138).
- The fact that there is no way of blocking inheritance of CSS styles was introduced to me by [an answer on Stack Overflow by Wadih M.](https://stackoverflow.com/questions/1046872/how-can-i-disable-inherited-css-styles/1046905#1046905).

[Bourbon]: https://www.bourbon.io/
[CSS]: https://en.wikipedia.org/wiki/Cascading_Style_Sheets
[:has()]: https://developer.mozilla.org/en-US/docs/Web/CSS/:has
[Less]: http://lesscss.org/
[pseudo-classes]: https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes
[Sass]: https://sass-lang.com/
[Stylus]: http://stylus-lang.com/
[^usngCSS1]: [Official Less website](http://lesscss.org/) Official Less website
[^usngCSS2]: Media Mark (3.2.12). ["Sass - Syntactically Awesome Stylesheets"](http://sass-lang.com/). Sass-lang.com. Retrieved 2014-02-23.
[^usngCSS3]: https://github.com/Compass/compass/blob/stable/README.markdown
[^usngCSS4]: https://github.com/thoughtbot/bourbon/blob/master/LICENSE.md
[^usngCSS5]: https://github.com/stylus/stylus/blob/dev/LICENSE
