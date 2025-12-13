# Overview

{% hint style="info" %}
**Holesail tip:** Feel free to reach out to us at hello@holesail.io if you have any questions or feature requests.&#x20;
{% endhint %}

Holesail is a peer-to-peer network tunneling and reverse proxy system that enables secure sharing of locally running services without requiring static IPs, port forwarding, or complex network configurations.&#x20;

This documentation provides a high-level introduction to the Holesail system, its architecture, and core functionalities.

> It’s Tailscale but without servers, no accounts, and no complicated setup. Just scan the QR, and you’re connected, encrypted, fast, and easy.&#x20;
>
> — From [Guy Swann](https://x.com/TheGuySwann)

> I’ve become a Holesail addict. If I can’t just generate a key and connect remotely to my service now, I’m now just looking for a replacement that does let me do this. I don’t even try anymore. It’s either as easy as Holesail, or I’ll find a replacement 🤣
>
> — From [Pear Report](https://fountain.fm/episode/MyIucEf5hVoN3xsQmhbg)

> Just used @holesail\_io to connect to a service running on Linux localhost on my MacBook. I can use it easily and from anywhere.&#x20;
>
> \
> Even via Terminal, this is the easiest and quickest way I've ever connected two computers and shared a service/app. Generate key, paste key, done.

> Holesail allows us to provide a revolutionary Peer-to-Peer (P2P) tunnelling solution, giving users instant access to their local networks without the need for complex configurations. This innovative approach ensures seamless connectivity and robust security through end-to-end encryption.\
> — From [Discord Linux](https://discord-linux.com)

## Easiest way to connect ever

Holesail CLI generates a QR code, scan the QR code with the Holesail Go app, and that's pretty much it. There are no complicated steps or painful setups—**just set up, scan, and sail.**

## Built with security in Mind

Holesail is not only a tunnelling software but also a security tool. All data that goes through holesail is encrypted and never touches any third-party server **ever**.&#x20;

All connections are completely peer-to-peer, and only the person with whom you share your "connection key" can find you and connect with you.

This gives your servers peak security against any attacker.

## Truly Peer-to-Peer

**Holesail is the only truly peer-to-peer software** of its kin&#x64;**;** there are **no servers** or third party relays. You own all your data and only the person you share access with can find you and connect to you.

Other peers in the network have no idea what you are running, if it is running, or how to connect to it or even if you are using Holesail.

## It's Open Source

Holesail and all of its modules are completely open source. This gives third-party services a method to  integrate Holesail into their system and make their services secure and easy to connect to.

## Key Features

* **Peer-to-peer tunnels**: Establish direct connections between peers without intermediary servers
* **Zero Configuration required**: Holesail does not require any configuration to work, just run a command and you are good to go.
* **Zero knowledge architecture:** No central servers means your data never touches any servers, it is all peer to peer. You connect directly with peers and your data stays with you. We never know who is using Holesail and for what.
* **TCP / UDP**: Tunnel both TCP and UDP traffic flawlessly.
* **No Bandwidth Limit**: Transfer as much data as you want, there is no limitation on the amount of data that goes through Holesail.
* **Open Source:** Holesail is completely open source and the source code is available on our Github repository.
* **No network configuration**: Works without port forwarding, static IPs, or NAT traversal setup
* **Secure connections**: All connections are end to end encrypted.
* **File manager**: Built-in filemanager to share files securely
* **Cross-platform compatibility**: Built with platform independence using Bare modules and Pear runtime support. Holesail works on iOS, Android, Linux, macOS and Windows.
* **Simple command-line interface**: Easy-to-use CLI.

## Popular use cases

1. Access your machines over the internet with Rustdesk + Holesail; no port forwarding or static IP is required.
2. Share locally running servers, websites and AI with anyone.
3. Share files and folders remotely. There are no bandwidth restrictions and no size limits.
4. Play Minecraft and any LAN game remotely with your friends.
5. Secure your SSH servers, block IP access and access securely with Holesail.
6. Access your Ollama server at home wherever you go.

Access selfhosted Vaultwarden, Portainer, Rustdesk, Ollama, Minecraft, Btcpayserver or anything with Holesail.

## Get Started

We've put together some helpful guides for you to get setup with our product quickly and easily.
