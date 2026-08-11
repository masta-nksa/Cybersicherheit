# Cybersicherheit – Unterrichtseinheit (5 Lektionen)

Materialien zur Unterrichtseinheit «Cybersicherheit» (Informatik, 2. Kanti).
Die Website wird von GitHub Pages direkt aus diesem Repository mit Jekyll gebaut –
**die Markdown-Dateien sind die Quelle, generiertes HTML wird nie eingecheckt.**

## Aufbau

```
├── _config.yml            Konfiguration (Titel, baseurl, Badge-Beschriftungen)
├── index.md               Startseite
├── lektion-1.md … -5.md   je eine Lektionsseite (nur Metadaten + kurzer Einleitungstext)
├── lektionen/             alle Arbeitsblätter, Musterlösungen und Ablaufpläne
├── Cybersicherheit_Konzept_5_Lektionen.md   didaktisches Gesamtkonzept
├── _layouts/              HTML-Gerüst (default / startseite / lektion / material)
└── assets/css/unterricht.css   Gestaltung inkl. Dark Mode und Druckansicht
```

## Inhalte bearbeiten

Text ändern: einfach die `.md`-Datei bearbeiten (lokal oder direkt auf github.com über
den Stift-Button) und committen. Ein paar Minuten später ist die Seite aktualisiert.

Jede Inhaltsdatei beginnt mit einem kleinen YAML-Block, aus dem sich Navigation und
Einordnung ergeben – der Rest der Datei ist normales Markdown:

```yaml
---
lektion: 3              # zu welcher Lektion gehört die Datei (1–5)
zielgruppe: sus         # sus | lehrperson  → bestimmt den Bereich auf der Lektionsseite
art: arbeitsblatt       # Badge; mögliche Werte siehe art_labels in _config.yml
titel: "Gruppenpuzzle: Schutzmassnahmen"   # Titel in Navigation und Browser-Tab
kurz: "Sechs Pakete zu den 11 Schutzmassnahmen"   # Kurzbeschrieb auf der Lektionsseite
reihenfolge: 2          # Sortierung innerhalb des Bereichs
---
```

**Neues Material hinzufügen:** Datei in `lektionen/` anlegen, obigen Block anpassen,
committen – sie erscheint automatisch an der richtigen Stelle. Es muss kein HTML und
keine Navigation angefasst werden.

## Lokale Vorschau (optional)

Nicht nötig, um die Seite zu aktualisieren – GitHub baut serverseitig. Wer trotzdem
lokal schauen will, braucht Ruby:

```
gem install bundler
bundle install
bundle exec jekyll serve
```

Anschliessend läuft die Vorschau auf <http://localhost:4000>. Wichtig: `baseurl` in
`_config.yml` muss dem Repository-Namen entsprechen, sonst greifen die Links auf der
veröffentlichten Seite ins Leere.
