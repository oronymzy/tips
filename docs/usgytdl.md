# using [youtube-dl]

!!! note
    
    {==foo.bar==} represents the URL of the YouTube video to be downloaded.

Use `youtube-dl --all-subs --write-all-thumbnails --write-description --write-info-json -o "%(uploader)s's %(title)s-%(id)s.%(ext)s" foo.bar` to download a video using a template-based filename, along with its description text, additional info, all available subtitles, and all available thumbnails. Alternatively, use `youtube-dl --all-subs --write-all-thumbnails --write-description --write-info-json -f "[height<=480]" -o "%(uploader)s's %(title)s (%(resolution)s resolution)-%(id)s.%(ext)s" foo.bar` to download the video in the same way, but only in a format with a video height of 480 pixels or lower, and with the video resolution included in the filename.

## explanation

- The `-f "[height<=480]"` [format selection option](https://github.com/rg3/youtube-dl/blob/master/README.md#format-selection) downloads a video only in a format with a video height of 480 pixels or lower.
- The `-o "%(uploader)s's %(title)s (%(resolution)s resolution)-%(id)s.%(ext)s"` [output template option](https://github.com/rg3/youtube-dl/blob/master/README.md#output-template) specifies a custom template for the name of the output file.
    - `uploader` specifies the video uploader's full name.
    - `title` specifies the video title.
    - `resolution` specifies the video resolution.
    - `id` specifies the video identifier.
    - `ext` specifies the video filename extension.
- The `--all-subs` [subtitle option](https://github.com/rg3/youtube-dl/blob/master/README.md#subtitle-options) downloads all available video subtitles.
- The `--write-all-thumbnails` [thumbnail image](https://github.com/rg3/youtube-dl/blob/master/README.md#thumbnail-images) option writes all thumbnail image formats to disk.
- The `--write-description` [filesystem option](https://github.com/rg3/youtube-dl/blob/master/README.md#filesystem-options) writes the video description to a file with a `.description` extension.
- The `--write-info-json` [filesystem option](https://github.com/rg3/youtube-dl/blob/master/README.md#filesystem-options) writes video metadata to a file with a `.info.json` extension.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[youtube-dl]: https://rg3.github.io/youtube-dl/
