# enabling browser support for the dat protocol
For Firefox on a Linux system, install **Dat-Firefox**, a prototype browser extension which makes `dat://` urls function in Firefox using a slightly modified [dat-gateway](https://github.com/sammacbeth/dat-gateway) as a bridge to the dat network. To install Dat-Firefox, first install [dat-fox-helper](https://github.com/sammacbeth/dat-fox-helper) with `curl -o- https://raw.githubusercontent.com/sammacbeth/dat-fox-helper/master/installer.sh | bash`, then install the extension from the [Mozilla Addon Store](https://addons.mozilla.org/en-US/firefox/addon/dat-p2p-protocol/). The [dat-fox](https://github.com/sammacbeth/dat-fox) extension will automatically verify if the binary can be automatically launched when it starts up. When a dat protocol url is entered, set the *Launch Application* to Dat and select “Remember my choice for dat links”.

??? info "Personal experience"
    - Only works in a limited and buggy way on Slinky running Kubuntu 18.04.
    - Does not work on Shady running Lubuntu 18.04, with Firefox returning an error that “The proxy server is refusing connections”.

## licensing
**Some rights reserved: MIT License.** Includes significant content from “[Dat-Firefox README](https://github.com/sammacbeth/dat-fox/blob/master/README.md)” and “[Dat-fox Helper Readme](https://github.com/sammacbeth/dat-fox-helper/blob/master/Readme.md)” on GitHub with the modifications, including the following:

- Fixed linebreak issues.

??? note "MIT License for Dat-Firefox[^ebsdatp1]"
    MIT License
    
    Copyright (c) 2018 Sam Macbeth
    
    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:
    
    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.
    
    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.

??? note "MIT License for Dat-fox Helper[^ebsdatp2]"
    MIT License
    
    Copyright (c) 2018 Sam Macbeth
    
    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:
    
    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.
    
    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.

[^ebsdatp1]: https://github.com/sammacbeth/dat-fox/blob/master/LICENSE.txt
[^ebsdatp2]: https://github.com/sammacbeth/dat-fox-helper/blob/master/LICENSE.txt
