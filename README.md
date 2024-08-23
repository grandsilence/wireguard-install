# WireGuard installer (with Amnezia WG config generator)

![Lint](https://github.com/grandsilence/wireguard-install/workflows/Lint/badge.svg)
[![Say Thanks!](https://img.shields.io/badge/Say%20Thanks-!-1EAEDB.svg)](https://saythanks.io/to/angristan)

> Fork of [angristan/wireguard-install](https://github.com/angristan/wireguard-install) that supports Amnezia WireGuard config generations.
> The configuration generator in this fork adds the following parameters required for AmneziaWG to work:

```conf
[Interface]
# ...
Jc = 5
Jmin = 50
Jmax = 1000
H1 = 1
H2 = 2
H3 = 3
H4 = 4
# ...

[Peer]
# ...
PersistentKeepalive = 15
# ...
```

**This project is a bash script that aims to setup a [WireGuard](https://www.wireguard.com/) VPN on a Linux server, as easily as possible!**

WireGuard is a point-to-point VPN that can be used in different ways. Here, we mean a VPN as in: the client will forward all its traffic through an encrypted tunnel to the server.
The server will apply NAT to the client's traffic so it will appear as if the client is browsing the web with the server's IP.

The script supports both IPv4 and IPv6. Please check the [issues](https://github.com/grandsilence/wireguard-install/issues) for ongoing development, bugs and planned features! You might also want to check the [discussions](https://github.com/grandsilence/wireguard-install/discussions) for help.

## Requirements

Supported distributions:

- AlmaLinux >= 8
- Arch Linux
- CentOS Stream >= 8
- Debian >= 10
- Fedora >= 32
- Oracle Linux
- Rocky Linux >= 8
- Ubuntu >= 18.04

## Usage

Download and execute the script. Answer the questions asked by the script and it will take care of the rest.

```bash
curl -O https://raw.githubusercontent.com/grandsilence/wireguard-install/master/wireguard-install.sh
chmod +x wireguard-install.sh
./wireguard-install.sh
```

It will install WireGuard (kernel module and tools) on the server, configure it, create a systemd service and a client configuration file.

Run the script again to add or remove clients!

## Providers

I recommend these cheap cloud providers for your VPN server:

- [Vultr](https://www.vultr.com/?ref=8948982-8H): Worldwide locations, IPv6 support, starting at \$5/month
- [Hetzner](https://hetzner.cloud/?ref=ywtlvZsjgeDq): Germany, Finland and USA. IPv6, 20 TB of traffic, starting at 4.5€/month
- [Digital Ocean](https://m.do.co/c/ed0ba143fe53): Worldwide locations, IPv6 support, starting at \$4/month

## Contributing

## Discuss changes

Please open an issue before submitting a PR if you want to discuss a change, especially if it's a big one.

### Code formatting

We use [shellcheck](https://github.com/koalaman/shellcheck) and [shfmt](https://github.com/mvdan/sh) to enforce bash styling guidelines and good practices. They are executed for each commit / PR with GitHub Actions, so you can check the configuration [here](https://github.com/grandsilence/wireguard-install/blob/master/.github/workflows/lint.yml).

## Say thanks

You can [say thanks](https://saythanks.io/to/angristan) if you want!

## Credits & Licence

This project is under the [MIT Licence](https://raw.githubusercontent.com/grandsilence/wireguard-install/master/LICENSE)

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=grandsilence/wireguard-install&type=Date)](https://star-history.com/#grandsilence/wireguard-install&Date)
