# using yq

!!! note
    
    There are two different [YAML](https://yaml.org/) processors named *yq*, [one by Andrey Kislyuk](https://github.com/kislyuk/yq) that functions as a [jq](https://stedolan.github.io/jq/) wrapper, and [one by Mike Farah](https://github.com/mikefarah/yq) that is separate from jq.

## [Andrey Kislyuk's yq] {: #AKyq }
Although YAML supports comments[^usingyq1], JSON does not support comments[^usingyq2], and jq mostly does not know how to handle comments[^usingyq3] [^usingyq4], so any YAML comments will not be preserved when using Andrey Kislyuk's yq.

[Andrey Kislyuk's yq]: https://github.com/kislyuk/yq
[^usingyq1]: https://yaml.org/spec/1.2/spec.html#comment//
[^usingyq2]: https://stackoverflow.com/questions/244777/can-comments-be-used-in-json/244858#244858
[^usingyq3]: https://github.com/stedolan/jq/issues/402
[^usingyq4]: https://github.com/stedolan/jq/wiki/FAQ#processing-not-quite-valid-json
