# using [youtube-dl]

!!! note
    
    {==foo.bar==} represents the URL of the YouTube video to be downloaded.

Use `youtube-dl --all-subs --write-all-thumbnails --write-description --write-info-json -o "%(uploader)s's %(title)s-%(id)s.%(ext)s" foo.bar` to download a video.

## explanation

- The `--all-subs` [subtitle option](https://github.com/rg3/youtube-dl/blob/master/README.md#subtitle-options) downloads all available video subtitles.
- The `--write-all-thumbnails` [thumbnail image](https://github.com/rg3/youtube-dl/blob/master/README.md#thumbnail-images) option writes all thumbnail image formats to disk.
- The `--write-description` [filesystem option](https://github.com/rg3/youtube-dl/blob/master/README.md#filesystem-options) writes the video description to a file with a `.description` extension.
- The `--write-info-json` [filesystem option](https://github.com/rg3/youtube-dl/blob/master/README.md#filesystem-options) writes video metadata to a file with a `.info.json` extension.
- `"%(uploader)s's %(title)s-%(id)s.%(ext)s"` specifies a custom [output template](https://github.com/rg3/youtube-dl/blob/master/README.md#output-template) for the name of the output file.
    - `uploader` specifies the video uploader's full name.
    - `title` specifies the video title.
    - `id` specifies the video identifier.
    - `ext` specifies the video filename extension.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[youtube-dl]: https://rg3.github.io/youtube-dl/
