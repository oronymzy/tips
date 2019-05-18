# installing yq

!!! note
    
    There are two different [YAML](https://yaml.org/) processors named *yq*, [one by Andrey Kislyuk](https://github.com/kislyuk/yq) that functions as a [jq](https://stedolan.github.io/jq/) wrapper, and [one by Mike Farah](https://github.com/mikefarah/yq) that is separate from jq.

## [Andrey Kislyuk's yq] {: #AKyq }
Use `sudo -H pip install yq` to install using [pip](https://pip.pypa.io/en/stable/).

## [Mike Farah's yq] {: #MFyq }

!!! note
    
    Mike Farah's yq can be launched with `yq.v2`.

[Install Go](instlGo.md), use `go get gopkg.in/mikefarah/yq.v2 && cd $HOME/go/src/gopkg.in/mikefarah/yq.v2 && go build` to download and install Mike Farah's yq, then append `PATH=$PATH:$HOME/go/src/gopkg.in/mikefarah/yq.v2/` to *.bashrc*.

!!! tip "Alternative installation methods"
    
    - Use `sudo add-apt-repository ppa:rmescandon/yq -y && sudo apt update && sudo apt install yq -y` to install from [Ubuntu PPA](https://en.wikipedia.org/wiki/Ubuntu_(operating_system)#Package_Archives).
    - Use `snap install yq` to install using [Snappy](https://en.wikipedia.org/wiki/Snappy_(package_manager)).

??? info "Personal experience"
    
    - Snappy installation tested in Kubuntu 17.10.
    - PPA installation does not work in Kubuntu 17.10.

## prior work
- The method of installing Andrey Kislyuk's yq using pip was introduced to me by [the Installation section of Andrey Kislyuk's yq's GitHub](https://github.com/kislyuk/yq#installation)
- The method of installing Mike Farah's yq using Go, PPA, or Snappy was introduced to me by [the Install section of Mike Farah's yq's GitHub](https://github.com/mikefarah/yq#install)

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

[Andrey Kislyuk's yq]: https://github.com/kislyuk/yq
[Mike Farah's yq]: https://github.com/mikefarah/yq
