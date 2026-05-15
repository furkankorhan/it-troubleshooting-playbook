# IT Troubleshooting Playbook

A practical troubleshooting playbook for common IT support situations.

The goal is simple: when something does not work, do not guess first. Check the basics, collect evidence, then decide the next step.

## Focus

This repository starts with network troubleshooting because it is one of the most common support situations:

- internet connection problems
- wrong or missing IP configuration
- DNS problems
- DHCP problems
- gateway/router problems
- basic terminal checks

## First Scenario: Internet funktioniert nicht

### 1. Check the physical and obvious things

- Is Wi-Fi or Ethernet connected?
- Is airplane mode disabled?
- Is the router/modem powered on?
- Does the problem affect one device or many devices?

### 2. Check IP configuration

Useful commands:

```bash
ipconfig        # Windows
ifconfig        # macOS/Linux
ip addr         # Linux
```

Look for:

- local IP address
- subnet mask
- default gateway
- DNS server

### 3. Test local network

```bash
ping 192.168.1.1
```

If the gateway does not answer, the problem is probably local: Wi-Fi, cable, router, wrong IP range or DHCP.

### 4. Test internet by IP

```bash
ping 8.8.8.8
```

If this works, the internet connection may be fine and DNS may be the problem.

### 5. Test DNS

```bash
nslookup google.com
dig google.com
```

If IP ping works but domain lookup fails, check DNS settings.

### 6. Check the route

```bash
traceroute google.com   # macOS/Linux
tracert google.com      # Windows
```

This helps show where the connection stops.

## Short German Explanations

| Begriff | Kurze Erklärung |
|---|---|
| IP-Adresse | Eine Adresse, mit der ein Gerät im Netzwerk erreichbar ist. |
| DNS | Übersetzt Domainnamen wie `google.com` in IP-Adressen. |
| DHCP | Verteilt automatisch IP-Adressen und Netzwerkeinstellungen. |
| Gateway | Der Router, über den ein Gerät andere Netzwerke erreicht. |
| Ping | Testet, ob ein Ziel erreichbar ist und wie lange die Antwort dauert. |

## What This Repository Shows

- I can structure a technical problem step by step.
- I know the basic difference between IP, DNS, DHCP and gateway.
- I can use terminal commands to collect information.
- I document technical topics in a simple and readable way.
- I am building this repository as practical proof for IT system and support fundamentals.

## Next Improvements

- Add screenshots or example command outputs
- Add a printable checklist
- Add a German-only version for interview practice
- Add more scenarios: slow PC, full storage, printer problem, software installation issue
