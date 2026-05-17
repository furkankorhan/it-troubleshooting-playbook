# Was ist DNS?

DNS bedeutet **Domain Name System**.

Ein Computer arbeitet im Netzwerk mit IP-Adressen. Menschen merken sich aber Namen wie `google.com` leichter als Zahlen. DNS verbindet diese beiden Welten.

Kurz gesagt:

```txt
google.com -> DNS -> IP-Adresse
```

## Einfaches Beispiel

Wenn ich im Browser `google.com` eingebe, fragt mein Gerät einen DNS-Server:

```txt
Welche IP-Adresse gehört zu google.com?
```

Der DNS-Server antwortet mit einer IP-Adresse. Danach kann der Browser die Webseite laden.

## Warum ist DNS wichtig beim Troubleshooting?

Wenn das Internet scheinbar nicht funktioniert, kann das Problem an DNS liegen.

Typische Zeichen:

- Webseiten öffnen sich nicht über Namen wie `google.com`
- eine direkte IP-Adresse funktioniert aber vielleicht noch
- `ping 8.8.8.8` funktioniert, aber `ping google.com` nicht

## Nützliche Befehle

```bash
nslookup google.com
```

```bash
ping google.com
```

```bash
ping 8.8.8.8
```

## Merksatz

Wenn IP funktioniert, aber Namen nicht funktionieren, prüfe DNS.
