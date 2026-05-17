# DNS, DHCP and Gateway Basics

This note explains three network terms that often appear in troubleshooting.

## IP Address

An IP address identifies a device in a network.

Example:

```text
192.168.1.24
```

German:

```text
Eine IP-Adresse ist die Adresse eines Geräts im Netzwerk.
```

## Subnet Mask

The subnet mask helps decide which devices are in the same local network.

Example:

```text
255.255.255.0
```

Simple meaning:

```text
192.168.1.x is local when the subnet mask is 255.255.255.0.
```

## Default Gateway

The default gateway is usually the router.

It is used when a device wants to reach something outside the local network.

German:

```text
Das Gateway ist meistens der Router. Darüber erreicht ein Gerät andere Netzwerke.
```

## DNS

DNS translates domain names into IP addresses.

Example:

```text
google.com -> 142.250.x.x
```

If DNS fails, the internet may feel broken even when the connection itself works.

German:

```text
DNS übersetzt Domainnamen in IP-Adressen.
```

## DHCP

DHCP automatically gives devices network settings.

Usually DHCP provides:

- IP address
- subnet mask
- gateway
- DNS server

German:

```text
DHCP verteilt automatisch IP-Adressen und Netzwerkeinstellungen.
```

## Quick Troubleshooting Pattern

```text
1. Do I have an IP address?
2. Do I have a gateway?
3. Can I ping the gateway?
4. Can I ping an external IP?
5. Can DNS resolve a domain?
```

This order prevents random guessing.
