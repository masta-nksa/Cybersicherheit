---
lektion: 3
zielgruppe: sus
art: input
titel: "Kurzinput: Virenschutz & Firewall"
kurz: "Signaturen, Hash-Werte, Ports – und wo beide Schutzebenen an Grenzen stossen"
reihenfolge: 1
---

# Kurzinput: Wie schützen Antivirus-Software und Firewall?

**Lektion 3 – Cybersicherheit | Plenum, ca. 8 Minuten**

## Antivirus-Software

Antivirenprogramme durchsuchen Dateien nach bekannten „Signaturen" – typischen Bitmustern von Schadcode. Eine Signatur ist im Prinzip ein eindeutiger digitaler Fingerabdruck einer Datei, berechnet über eine sogenannte Hash-Funktion (z. B. SHA-256).

**Woher weiss das Programm, wonach es suchen soll?** Sicherheitsfirmen betreiben sogenannte „Honeypots" – Systeme, die absichtlich Angriffen ausgesetzt werden, um neue Schadsoftware einzufangen. Diese wird analysiert, in Signaturen umgewandelt und per Update an alle Antivirenprogramme verteilt. **Deshalb gilt:** Ein Antivirenprogramm ist nur so gut wie sein letztes Update – brandneue Schadsoftware kann für kurze Zeit unentdeckt bleiben.

Zwei Scan-Arten kommen meist kombiniert zum Einsatz:
- **Echtzeitschutz:** prüft jede neue Datei sofort (Download, USB-Stick, E-Mail-Anhang)
- **Festplattenscan:** durchsucht periodisch den gesamten Datenträger

Fortgeschrittene Programme nutzen zusätzlich eine „Sandbox" – eine abgeschottete Testumgebung, in der verdächtiger Code ausgeführt und sein Verhalten beurteilt wird, statt nur nach bekannten Signaturen zu suchen.

**Zum Ausprobieren (optional):** [SHA-256-Tool](https://emn178.github.io/online-tools/sha256.html) – geben Sie ein Wort ein und ändern Sie ein einziges Zeichen. Der Hash-Wert verändert sich komplett – genau das macht ihn als „Fingerabdruck" nützlich.

## Firewall

Eine Firewall ist die zweite Verteidigungslinie: Sie verhindert nicht die Infektion selbst, sondern begrenzt deren Auswirkungen, indem sie den Netzwerkverkehr kontrolliert.

Kommunikation läuft über sogenannte „Ports" – man kann sie sich wie nummerierte Türen vorstellen. Die Firewall schliesst standardmässig fast alle Ports und erlaubt nur gezielt definierte Ausnahmen (z. B. Port 443 für sicheres Surfen im Browser). Bei einem unerwarteten Verbindungsversuch fragt die Firewall meist nach, ob dieser erlaubt werden soll.

## Grenzen

Weder Antivirus noch Firewall bieten hundertprozentige Sicherheit – neue Schadsoftware, geschickte Tricks oder falsch konfigurierte Einstellungen können beide Schutzebenen umgehen. **Deshalb bleibt das eigene Verhalten entscheidend** – damit steigen wir jetzt ins Gruppenpuzzle ein.
