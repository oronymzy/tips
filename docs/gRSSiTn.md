# getting an RSS feed for an iTunes podcast
!!! attention
    This is not a permanent solution to the problem of web pages for iTunes podcasts not providing a way of getting RSS feeds. **It could stop working at any time.**

Get the *id* number from the page's URL, for example `941907967` from `https://itunes.apple.com/us/podcast/reply-all/id941907967`, the page for [Reply All](https://www.gimletmedia.com/reply-all). Visit the URL `https://itunes.apple.com/lookup?id=foobar&entity=podcast`, where *foobar* is the id number, for example `https://itunes.apple.com/lookup?id=941907967&entity=podcast`. This will return a [JSON](https://json.org/)-formatted plain text document named `1.txt`, which can be saved as a file with a `json` extension. The RSS feed URL will be the value for the `feedUrl` attribute, for example `http://feeds.gimletmedia.com/hearreplyall`.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
The solution was introduced to me by [an answer on Super User by Gino](https://superuser.com/questions/78415/get-rss-feed-from-itunes-podcast-links/782413#782413).
