# installing Google Chrome
## CentOS
Use `sudo yum install https://dl.google.com/linux/direct/google-chrome-stable_current_x86_64.rpm`.

## Kubuntu
Use `wget -P /tmp https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb && sudo dpkg -i --force-depends /tmp/google-chrome-stable_current_amd64.deb`. If any dependencies did not install, also use `sudo apt-get install -f`.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The bulk of the Kubuntu installation script was introduced to me by [an answer on Ask Ubuntu by Tioz](https://askubuntu.com/questions/760085/how-do-you-install-google-chrome-on-ubuntu-16-04/760452#760452).
- The method of installing an RPM package from a URL using yum was introduced to me by [a question on Stack Exchange by userX](https://unix.stackexchange.com/questions/457130/install-google-chrome-in-centos).
