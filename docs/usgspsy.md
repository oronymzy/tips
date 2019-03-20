# using [speech synthesis]

## synthesizing speech as an [audio signal]

It is also possible to [synthesize speech from a text file](cnvffmt.md#plaintexttossFLAC).

### synthesizing [English] speech using [audio output](http://www.cstr.ed.ac.uk/projects/festival/manual/festival_23.html) and the [Festival Speech Synthesis System]

!!! note
    
    - {==Foo bar? Baz.==} represents text to be synthesized as speech.

Use `echo "Foo bar? Baz." | festival --tts`.

The [Festival Speech Synthesis System] provides [multiple possible voices](http://www.cstr.ed.ac.uk/projects/festival/manual/festival_24.html#SEC98).

### synthesizing [United States English] speech using [the default audio device](https://github.com/espeak-ng/espeak-ng/blob/master/src/espeak-ng.1.ronn#options) and [eSpeak NG]

!!! note
    
    - {==Foo bar? Baz.==} represents text to be synthesized as speech.

Use `espeak-ng -v "gmw/en-US" "Foo bar? Baz."`.

Use `espeak-ng --voices` to list available voices or `espeak-ng --voices=en` to list available English voices.

!!! bug
    
    Voice files prefixed with `mb/` ([MBROLA](https://en.wikipedia.org/wiki/MBROLA)) cannot be used.

#### explanation

!!! note
    
    This is an incomplete explanation.

- The `-v "gmw/en-US"` [option](https://github.com/espeak-ng/espeak-ng/blob/master/src/espeak-ng.1.ronn#options) uses the `gmw/en-US` voice file, with a VoiceName of `english-us`.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[audio signal]: https://en.wikipedia.org/wiki/Audio_signal
[English]: https://en.wikipedia.org/wiki/English_language
[eSpeak NG]: https://github.com/espeak-ng/espeak-ng
[Festival Speech Synthesis System]: http://www.cstr.ed.ac.uk/projects/festival/
[United States English]: https://en.wikipedia.org/wiki/American_English
[speech synthesis]: https://en.wikipedia.org/wiki/Speech_synthesis
