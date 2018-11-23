# using [Browsersync]
To start a server for a single static HTML file, use `browser-sync start --server "/foo/bar/baz" --index foobar.html`, where *foobar.html* is the static HTML file to be served, and */foo/bar/baz* is the path to the file.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The fact that Browsersync looks for an `index.html` file in the specified directory, and that the `index` option can be used to override this was introduced to me by [a comment on GitHub by shakyShane](https://github.com/BrowserSync/browser-sync/issues/699#issuecomment-117277076).
- The fact that the path to the file is specififed betwen the `server` and `index` options was introduced to me by [a comment on GitHub by shakyShane](https://github.com/BrowserSync/browser-sync/issues/1579#issuecomment-416046545).

[Browsersync]: https://browsersync.io/
