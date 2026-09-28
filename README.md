# Netzwerknotizen

Hier sammle ich Grundlagen und Checklisten zur Fehlersuche im Netzwerk. Die Notizen gehören zu meiner Vorbereitung auf eine IT-Ausbildung, besonders im Bereich Systemintegration.

## Inhalt

- [Internet funktioniert nicht](internet-not-working.md) – Verbindung, IP-Konfiguration, Gateway und DNS prüfen
- [DNS, DHCP und Gateway](dns-dhcp-gateway.md) – kurze Erklärungen der Begriffe
- [Terminal-Befehle](terminal-command-notes.md) – Befehle für Netzwerk-, Datei- und Git-Aufgaben
- [Was ist DNS?](was-ist-dns.md) – eine kurze Erklärung auf Deutsch

Ein Teil der Notizen ist auf Englisch. Die deutschen Abschnitte helfen mir, die Fachbegriffe auch auf Deutsch zu verwenden.

## Verwendung

Die Markdown-Dateien lassen sich direkt auf GitHub lesen. Die Beispiele sind Lernmaterial und keine Protokolle aus einem Firmennetzwerk. Adressen wie `192.168.1.1` müssen zum eigenen Netzwerk passen.

Ein fehlgeschlagener Ping beweist noch keinen Verbindungsfehler: Manche Geräte und Firewalls beantworten solche Anfragen nicht. Auch einzelne Zeitüberschreitungen bei `traceroute` reichen nicht aus, um eine Störung zuzuordnen. Ergebnisse sollten immer zusammen mit weiteren Prüfungen betrachtet werden.

Die Sammlung ist noch klein. Als Nächstes möchte ich nachvollziehbare Beispiele mit eigenen Beobachtungen ergänzen.
