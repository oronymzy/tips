# using [FFmpeg]
Use `for i in *.flac ; do ffmpeg -i "$i" -acodec libmp3lame -q:a 0 $(basename "${i/.flac}").mp3; done` to convert multiple FLAC files to MP3 files, preserving filenames. Use `ffmpeg -i foo.flac -acodec libmp3lame -q:a 0 bar.mp3` to convert a single FLAC file to a single MP3 file, where *foo.flac* is the input file and *bar.mp3* is the output file.

## explanation

!!! note
    This is an incomplete explanation.

- `-q:a 0` encodes the MP3 file at variable bitrate with a range between 220-260 kbit/s, the highest available quality.[^usFFmpg1]

## licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Includes significant content from [an answer on Unix & Linux Stack Exchange by Ketan](https://unix.stackexchange.com/questions/114908/bash-script-to-convert-all-flac-to-mp3-with-ffmpeg/114917#114917), with changes made.

## prior work
- The method of iterating through a [for loop](https://en.wikipedia.org/wiki/For_loop) with FFmpeg and preserving the filename was introduced to me by [an answer on Unix & Linux Stack Exchange by Ketan](https://unix.stackexchange.com/questions/114908/bash-script-to-convert-all-flac-to-mp3-with-ffmpeg/114917#114917).

[FFmpeg]: https://ffmpeg.org/
[^usFFmpg1]: https://trac.ffmpeg.org/wiki/Encode/MP3#VBREncoding
