# determining the IP address
In Kubuntu, use any of the following:

- `hostname -I`
- `ifconfig -a`
- `ip addr show`
- `ip route get 8.8.8.8 | awk '{print $NF; exit}'`

## licensing
**Some rights reserved: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).** Specifically, the following content falls under this license:

- [An answer on Ask Ubuntu by rsp](https://askubuntu.com/questions/430853/how-do-i-find-my-internal-ip-address/604691#604691):
> `ip route get 8.8.8.8 | awk '{print $NF; exit}'`

If the above content is omitted, the rest is licensed **no rights reserved: [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).**

## prior work
- The `hostname -I` method was introduced to me by [an answer on Ask Ubuntu by Sarath Somana](https://askubuntu.com/questions/430853/how-do-i-find-my-internal-ip-address/665495#665495).
- The `ifconfig -a` and `ip addr show` methods were introduced to me by [an answer on Ask Ubuntu by kamil](https://askubuntu.com/questions/430853/how-do-i-find-my-internal-ip-address/430855#430855).
- The `ip route get 8.8.8.8 | awk '{print $NF; exit}'` method was introduced to me by [an answer on Ask Ubuntu by rsp](https://askubuntu.com/questions/430853/how-do-i-find-my-internal-ip-address/604691#604691).
