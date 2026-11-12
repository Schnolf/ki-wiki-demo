# CLAUDE.md — Regeldatei für mein KI-Wiki

<!-- Diese Datei liest Claude Code bei jedem Start automatisch. Sie ist die
     „Hausordnung“ der Bibliothek: Was liegt wo, wie wird eingearbeitet,
     wie wird geantwortet. Fang klein an und ergänze eine Regel immer dann,
     wenn etwas schiefgegangen ist. -->

Das ist mein persönliches Wiki. Du (Claude) pflegst es, ich entscheide, was hineinkommt.

## Ordner

<!-- Die drei Ebenen nach Karpathys LLM-Wiki: Rohquellen, Wiki, Regeln. -->

- `_inbox/` — neue Quellen, noch nicht eingearbeitet. Hier lege ich Dinge ab.
- `quellen/` — Rohquellen nach dem Einarbeiten. **Nie verändern**, sie sind der Beleg.
- `wiki/` — von dir gepflegte Seiten:
  - `wiki/buecher/` — eine Seite pro Buch, Artikel oder Vortrag
  - `wiki/begriffe/` — Konzepte, die in mehreren Quellen vorkommen
  - `wiki/ideen/` — meine eigenen Ideen und Entwürfe
- `index.md` — Übersicht aller Wiki-Seiten mit je einer Zeile. Lies sie zuerst.
- `log.md` — Protokoll: was wann eingearbeitet oder geändert wurde.

## Seitenformat

<!-- Frontmatter macht Seiten durchsuchbar. `aliases` ist das wichtigste Feld:
     Grep findet nur, was wörtlich dasteht. -->

Jede Wiki-Seite beginnt so:

```yaml
---
title: Sprechender Titel
tags: [thema, unterthema]
aliases: [Synonyme, Abkürzungen, englischer Begriff, Personennamen]
quellen: [dateiname-der-rohquelle]
erstellt: JJJJ-MM-TT
summary: 1–2 eigene Sätze, worum es geht und warum es relevant ist.
---
```

- Dateinamen in `kebab-case`, ohne Umlaute (`ä→ae`, `ö→oe`, `ü→ue`, `ß→ss`).
- Querverweise als `[[dateiname|Anzeigetext]]` (Obsidian-Wikilinks).
- Doppelpunkt in YAML-Werten nur in Anführungszeichen.

## Ablauf 1 — Quelle einarbeiten („Arbeite die Inbox ein“)

1. Quelle lesen und mir in 2–3 Sätzen sagen, worum es geht.
2. Prüfen, ob es dazu schon eine Seite gibt. Wenn ja: ergänzen statt doppelt anlegen.
3. Seite in `wiki/` anlegen bzw. ergänzen, betroffene Begriffs- und Ideenseiten verlinken.
4. Rohquelle von `_inbox/` nach `quellen/` verschieben.
5. `index.md` und `log.md` aktualisieren.
6. Mir zeigen, was du geändert hast. **Bei Unsicherheit fragen, nicht raten.**

<!-- „Kuration statt Masse“: Nicht alles gehört ins Wiki. Diese Regel ist der
     Unterschied zwischen einem Wiki und einer zweiten Ablage. -->
Nicht alles gehört ins Wiki. Leere Notizen, reine To-dos und Dubletten meldest du mir, statt sie einzuarbeiten.

## Ablauf 2 — Frage beantworten

1. Zuerst `index.md`, dann gezielt suchen (auch nach Synonymen und `aliases`).
2. Antwort **mit Quellenlinks** auf die Wiki-Seiten geben.
3. Trennen: Was steht in der Quelle? Was ist meine spätere Idee? Was ist deine Schlussfolgerung?
4. Wenn nichts dazu im Wiki steht: das ehrlich sagen. Nicht aus dem Allgemeinwissen auffüllen, ohne es zu kennzeichnen.
5. Ist die Antwort wertvoll, biete an, sie als neue Seite zu speichern.

## Ablauf 3 — Wiki pflegen („Mach einen Check“)

Prüfe auf: Seiten ohne Eintrag in `index.md`, tote Wikilinks, fehlende `summary`,
widersprüchliche Aussagen zwischen Seiten. Melde, was du findest; ändere erst nach Rückfrage.

## Was du nicht tust

- Rohquellen in `quellen/` verändern.
- Seiten löschen, ohne zu fragen.
- Längere Zitate aus urheberrechtlich geschützten Büchern übernehmen — eigene Zusammenfassungen genügen.
