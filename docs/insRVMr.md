# installing [Ruby Version Manager]

??? info "Personal experience"
    
    - Works in Kubuntu 18.04.
    - Tested in Kubuntu 17.10.

Use `sudo apt-add-repository -y ppa:rael-gc/rvm && sudo apt-get update && sudo apt-get install rvm -y` to install from [Ubuntu PPA](https://en.wikipedia.org/wiki/Ubuntu_(operating_system)#Package_Archives). Open Gnome Terminal with `gnome-terminal`, then use ++"Edit > Preferences > Command"++ and enable ++"Run command as a login shell"++. Reboot. Verify installation with `rvm -v`.

If necessary, open Gnome Terminal with `gnome-terminal`, then use `rvm install ruby` to install Ruby, followed by `rvm alias create default foobar && rvm use foobar` to specify the Ruby version used by Ruby Version Manager, where {==foobar==} represents a Ruby version, for example `ruby-2.6.0`.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The bulk of the installation script and instructions were introduced to me by the [the RVM package for Ubuntu README on GitHub](https://github.com/rvm/ubuntu_rvm/blob/master/README.md).
- The necessity of using Gnome Terminal was introduced to me by [the Change your terminal window section of the RVM package for Ubuntu README on GitHub](https://github.com/rvm/ubuntu_rvm#2-change-your-terminal-window).

[Ruby Version Manager]: https://rvm.io/
