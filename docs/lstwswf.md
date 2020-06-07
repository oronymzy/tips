# list of websites supporting [web feeds]

## DeviantArt web feed support
RSS feeds [are supported through the DeviantArt API](https://www.deviantart.com/developers/rss). More information is available from [the DeviantArt Help Center](https://www.deviantartsupport.com/en/article/how-do-i-use-rss-feeds).

The [query string](https://en.wikipedia.org/wiki/Query_string) consists of two parts. It specifies the type of pages to return:

`type=`
: `deviation`
: `forums`
: `journal`
: `news`

and it incorporates the results of [a search](https://www.deviantartsupport.com/en/article/are-there-any-tricks-to-narrowing-down-a-search-on-deviantart), including any [search operators](https://whatis.techtarget.com/definition/search-operator).

### supported operators for all page types

[disjunction](https://en.wikipedia.org/wiki/Logical_disjunction) (inclusive or) with `OR`
: *foo OR bar*
: matches, *foo*, *bar*, or both *foo* and *bar*

exact match with quotation marks (`" "`)
: *"foo bar"*
: matches *foo bar* exactly

exclusion with a hyphen-minus (`-`)
: *foo -bar*
: matches *foo*, but not *bar*

grouping (to control [operator precedence](https://en.wikipedia.org/wiki/Order_of_operations)) with parentheses (`( )`)
: *foo (bar OR baz)*
: matches either *foo* and *bar* or *foo* and *baz*

### supported search terms for deviations only

category search with the `in:` prefix
: *in:foobar*

description search with the `description:` prefix
: *description:foobar*

deviant search with the `by:` prefix
: *by:foobar*

deviant's favorites search with the `favby:` prefix (cannot be combined with other search terms)
: *favby:foobar*

image resolution search with the `width:` and `height:` prefixes
: *width:foo*
: *height:bar*

keyword search with the `keywords:` prefix
: *keywords:foobar*

sorting search results by date, in descending order, with `sort:time` in combination with a query
: *foobar sort:time*

title search with the `title:` prefix
: *title:foobar*

upload time search with the `max_age:` prefix
: *max_age:foobar*

### deviations
Use `http://backend.deviantart.com/rss.xml?type=deviation&q=by:foobar+sort:time`, where *foobar* is the username.

!!! tip "Example: [David Revoy](http://www.davidrevoy.com/) [on DeviantArt](https://www.deviantart.com/deevad)"
    
     From `https://www.deviantart.com/deevad`, `deevad` is the username, so use `http://backend.deviantart.com/rss.xml?type=deviation&q=by:deevad+sort:time`.

## GitHub web feed support
Atom feeds are available for the releases, tags, and commits of project pages, accessible by postfixing the page's URL with `releases.atom`, `tags.atom`, and `commits/master.atom`, respectively.[^lstwswf1]

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[web feeds]: https://en.wikipedia.org/wiki/Web_feed

[^lstwswf1]: [RSS feeds for GitHub projects - How to use Git and GitHub - GitHub Support Community](https://github.community/t/rss-feeds-for-github-projects/292/2)
