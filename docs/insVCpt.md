# installing [VeraCrypt]
To install from [the VeraCrypt website release](https://www.veracrypt.fr/en/Downloads.html), use `wget -P /tmp https://launchpad.net/veracrypt/trunk/1.23/+download/veracrypt-1.23-setup.tar.bz2` to download the Linux archive file, then use `tar xvf /tmp/veracrypt-1.23-setup.tar.bz2 -C /tmp` to extract its contents to `/tmp`. Navigate to `/tmp` with `cd /tmp`, then use `./veracrypt-1.23-setup-gui-x64` to install VeraCrypt.

To install from [Ubuntu PPA](https://en.wikipedia.org/wiki/Ubuntu_(operating_system)#Package_Archives), use `sudo add-apt-repository ppa:unit193/encryption -y && sudo apt update && sudo apt install veracrypt -y`.

??? info "Personal experience"
    
    The Ubuntu PPA initially worked in Kubuntu 17.10, but then stopped working.

## licensing
**No rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The bulk of the installation script for the Ubuntu PPA was introduced to me by [an answer on Ask Ubuntu by s3m3n](https://askubuntu.com/questions/929195/what-is-the-recommended-way-to-use-veracrypt-in-ubuntu/937325#937325).
- The bulk of the installation script for the VeraCrypt website release was introduced to me by [an answer on Ask Ubuntu by Pawel Debski](https://askubuntu.com/questions/929195/what-is-the-recommended-way-to-use-veracrypt-in-ubuntu/941210#941210).
- The method of extracting an archive into a specified directory was introduced to me by [an answer on Ask Ubuntu by Wesley Rice](https://askubuntu.com/questions/45349/how-to-extract-files-to-another-directory-using-tar-command/45354#45354).

[VeraCrypt]: https://www.veracrypt.fr/en/Home.html
