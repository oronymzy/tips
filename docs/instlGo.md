# installing [Go]
In Linux, use `wget -P /tmp https://dl.google.com/go/go1.11.linux-amd64.tar.gz && sudo tar -C /usr/local -xzf /tmp/go1.11.linux-amd64.tar.gz`, then add these lines to `$HOME/.profile`:

```
# Set GOROOT
export GOROOT=/usr/local/go
export PATH=$GOROOT/bin:$PATH
```

Reboot.

To uninstall, use `rm -rvf /usr/local/go/`, then remove the text previously added to `$HOME/.profile`.

??? info "Personal experience"
    - Works on Slim running CentOS 7.
    - Tested in Kubuntu 17.10.

## explanation

!!! note
    This is an incomplete explanation.

- `wget -P /tmp https://dl.google.com/go/go1.11.linux-amd64.tar.gz` downloads [the Linux tar](https://golang.org/dl/).
- `sudo tar -C /usr/local -xzf /tmp/go1.11.linux-amd64.tar.gz` extracts the tar and creates a Go tree in `/usr/local/go`.

## licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Includes significant content from [an answer on Ask Ubuntu by Tony](https://askubuntu.com/questions/959932/installation-instructions-for-golang-1-9-into-ubuntu-16-04/960327#960327), with modifications.

## prior work
- The lines to be added to `$HOME/.profile` and the necessity of setting GOROOT was introduced to me by [an answer on Ask Ubuntu by Tony](https://askubuntu.com/questions/959932/installation-instructions-for-golang-1-9-into-ubuntu-16-04/960327#960327).
- The method of extracting the tar and creating a Go tree was introduced to me by [a page on the Go website](https://golang.org/doc/install).
- The method of uninstalling Go was introduced to me by [an answer on Stack Overflow by Basile Starynkevitch](https://stackoverflow.com/questions/42186003/how-to-uninstall-golang/42186042#42186042).

[Go]: https://golang.org/
