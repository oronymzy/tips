# installing [Git]
## CentOS
Use `sudo yum install centos-release-scl && sudo yum install rh-git29 && scl enable rh-git29 bash` to install Git 2.9.

## Ubuntu
Use `sudo add-apt-repository ppa:git-core/ppa -y && sudo apt-get update && sudo apt-get install git -y` to install from [Ubuntu PPA](https://en.wikipedia.org/wiki/Ubuntu_(operating_system)#Package_Archives).

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The `ppa:git-core/ppa` PPA and the bulk of the installation script was introduced to me by [an answer on Ask Ubuntu by muru](https://askubuntu.com/questions/568591/how-do-i-install-the-latest-version-of-git-with-apt/568596#568596).
- The bulk of the CentOS installation script was introduced to me by [a page on Software Collections](https://www.softwarecollections.org/en/scls/rhscl/rh-git29/).

[Git]: https://git-scm.com/
