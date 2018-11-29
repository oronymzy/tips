# getting a web page screenshot
In **Firefox**, once the page is loaded, use ++shift++ ++f2++ to open the developer toolbar and use `screenshot --fullpage` to save a PNG-formatted screenshot as a local file. In Kubuntu, the file will be saved to the *Downloads* directory. In **Google Chrome** under **Chrome OS, Linux, or Windows**, once the page is loaded, use ++ctrl++ ++shift++ ++i++ and then ++ctrl++ ++shift++ ++p++ to open the developer menu, enter `screenshot`, select *Capture full size screenshot*, and navigate to where the screenshot should be saved.

Once the screenshot is saved, [embed the download image's URL into the image as Exif metadata](emExfmi.md).

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The method of getting a screenshot with Firefox was introduced to me by [an answer on Stack Overflow by enreas](https://stackoverflow.com/questions/13158083/take-a-full-page-screenshot-with-firefox-on-the-command-line/14830242#14830242).
- The method of getting a screenshot with Google Chrome was introduced to me by [a page on Zapier](https://zapier.com/blog/full-page-screenshots-in-chrome/).
