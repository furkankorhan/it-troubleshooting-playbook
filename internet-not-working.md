# Scenario: Internet funktioniert nicht

This checklist is for a simple support situation: a user says the internet is not working.

The goal is not to fix everything immediately. The goal is to find out where the problem probably is.

## 1. Ask One Clarifying Question

Does the problem happen on one device or on multiple devices?

- One device: likely device, Wi-Fi, cable, IP configuration or DNS setting
- Multiple devices: likely router, provider, Wi-Fi access point or local network issue

## 2. Check Obvious Things First

- Wi-Fi or Ethernet connected?
- Airplane mode disabled?
- Router powered on?
- Correct Wi-Fi network selected?
- Cable fully connected?
- Does another website fail too?

German practice:

```text
Ich prüfe zuerst die einfachen Ursachen: WLAN, Kabel, Router und ob das Problem nur ein Gerät betrifft.
```

## 3. Check IP Configuration

Useful commands:

```bash
ipconfig        # Windows
ifconfig        # macOS/Linux
ip addr         # Linux
```

Look for:

- IP address
- subnet mask
- default gateway
- DNS server

Warning signs:

- no IP address
- `169.254.x.x` address
- missing gateway
- missing DNS server

## 4. Test the Local Gateway

Example:

```bash
ping 192.168.1.1
```

If the gateway does not answer, the problem is probably local:

- wrong Wi-Fi
- weak Wi-Fi signal
- cable issue
- router issue
- wrong IP range
- DHCP problem

## 5. Test Internet by IP

Example:

```bash
ping 8.8.8.8
```

If this works, basic internet connectivity is probably available.

If this does not work, the problem may be routing, router, provider or firewall related.

## 6. Test DNS

Examples:

```bash
nslookup google.com
dig google.com
```

If `ping 8.8.8.8` works but `google.com` does not resolve, DNS is a strong suspect.

German practice:

```text
Die Verbindung per IP funktioniert, aber der Domainname wird nicht aufgelöst. Deshalb prüfe ich DNS.
```

## 7. Check the Route

Examples:

```bash
traceroute google.com   # macOS/Linux
tracert google.com      # Windows
```

This shows where packets stop on the way to the destination.

## Short Decision Flow

```text
Only one device affected?
-> Check Wi-Fi/cable/IP/DNS on that device.

All devices affected?
-> Check router, provider status and local network.

IP ping works but domain does not?
-> Check DNS.

Gateway ping fails?
-> Check local network first.
```
