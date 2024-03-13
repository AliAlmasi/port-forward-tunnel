# Quick port prerouting script (using iptables)

This script can be used for initializing the port prerouting tunnel.

## What's prerouting?

prerouting is used for altering a packet as soon as it’s received.

## What's this used for exactly?

Genuinely, you can use this to create a relay server for your main VPN server. This method can be used in countries like Iran, where domestic servers have fewer restrictions. Your VPN packets are sent to your relay (domestic) server, then it'll be sent (by using this script) to your main VPN server (in Germany for example).

![How it works?](./how-it-works.png)

## How to use this?

You can simply use this script by running this on your relay server:

```plaintext
sudo bash <(curl https://raw.githubusercontent.com/AliAlmasi/port-prerouting-tunnel/main/install.sh)
```

After running this line, it will ask you for an IP address. Since you're making a relay server, then you should enter your main server's IP. After doing this, you can change your VPN configurations to use your relay server's IP as the destination.

## How to uninstall this?

You can undo this script by running this on your relay server:

```plaintext
sudo bash <(curl https://raw.githubusercontent.com/AliAlmasi/port-prerouting-tunnel/main/uninstall.sh)
```
