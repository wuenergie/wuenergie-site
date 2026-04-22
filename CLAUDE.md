# CLAUDE.md — Projekt-Memory für Claude Code

Statische Einpersonen-Website für **WuEnergie / Ing.-Büro Jörg Wünnenberg**
(Staufen im Breisgau, seit 2003). Konversionsorientiert — Ziel: E-Mail-Anfrage
oder 30-Minuten-Erstgespräch via Cal.com.

> Dieses Dokument brieft zukünftige Claude-Sessions. Das Inhaber-Handbuch
> („So änderst du Texte") steht in [README.md](./README.md).

## Positionierung (Kernsatz)

> „Ich verbinde Energieberatung mit echter Anlagentechnik: Ich messe,
> analysiere und optimiere Energieflüsse direkt im Betrieb — damit
> Einsparungen tatsächlich erreicht werden."

**T-förmige Kompetenz** als USP: Beratung **und** Umsetzung aus einer Hand —
Audit, BAFA-Antrag, SPS-Programmierung, Schaltschrank, Inbetriebnahme,
Monitoring. Das unterscheidet vom reinen Berater und vom reinen Automatisierer.

## Zielgruppe

- Primär: Geschäftsführer/Inhaber Mittelstand (20–500 MA), Facility Manager,
  Betreiber energieintensiver Objekte (Hotels, Camping, Produktion, Pflegeheime).
- Sekundär: Kommunen, Stadtwerke, Sparkassen (DIN-EN-16247-Audits).

Entscheidungskontext: geschäftsorientiert, technisch interessiert, **keine
Ingenieure**. Suchen Vertrauen + klaren nächsten Schritt.

## Marken

- **wuenergie.de** — diese Website (beratungs-/vertriebsorientiert)
- **wuennenberg.org** — technische Schwestermarke (WordPress, separat betrieben)
- Langfristig geplante Zusammenführung. Bestandskunden kennen „Wünnenberg".

## Stack (bewusst schlicht)

| Ebene          | Wahl                                                             |
| -------------- | ---------------------------------------------------------------- |
| Generator      | **Jekyll** (nativ von GitHub Pages gebaut, kein Action nötig)    |
| Content        | Markdown im Repo-Root, Daten in `_data/*.yml`                    |
| Styling        | Eine handgepflegte CSS-Datei, CSS-Variablen, `clamp()`           |
| Fonts          | System-Font-Stack (kein Google CDN, keine Custom Webfonts)       |
| Interaktivität | Keine. Pure HTML/CSS.                                            |
| Kontakt        | `mailto:` + externer Cal.com-Link (kein Embed, kein Tracking-JS) |
| Analytics      | Keine                                                            |
| Hosting        | GitHub Pages (Source: `main` Branch, Root)                       |

**Bewusst NICHT im Einsatz:** npm, Node, Bundler-Builds im CI,
React/Vue/Alpine, Astro, Tailwind-Build, Analytics, Cookie-Banner,
Kontaktformular.

## Dateistruktur

```text
_config.yml            Site-Konfig
_data/
  site.yml             Kontaktdaten, Kernsatz, Badges (zentrale Quelle)
  referenzen.yml       Referenzliste (datengetrieben)
_layouts/
  default.html         Hauptseiten-Shell
  landing.html         Vertical-Landingpage-Template
_includes/
  head.html            Meta-Tags, OG, Favicon, CSS
  footer.html          Footer mit Adresse/Kontakt/Links
  cta.html             Wiederverwendbarer Kontakt-Block
assets/css/style.css   Eine CSS-Datei, das war's
index.md               Startseite
camping.md             /camping — Landing für Campingplätze
impressum.md           /impressum
datenschutz.md         /datenschutz
CNAME                  wuenergie.de
favicon.svg            Brand-Icon (Teal „W")
robots.txt
```

## Tonalität & Stil (verbindlich)

- **Professionell-technisch, aber warm.** Inhabergeführtes Ingenieurbüro, **kein SaaS-Startup**.
- Vertrauen > Hype. Konkret > abstrakt. Wirtschaftlichkeit im Fokus.
- Menschliche Ansprache: „Ich messe…" — kein distanziertes Marketing-Deutsch.
- Deutsche Begriffe bevorzugen („Gebäudeautomation", nicht „Building Automation").
- H1/H2 in Serif (System-Serif) — menschlicher Kontrapunkt zur Technik-Thematik.

## Do's und Don'ts

### DO

- Quantifizierte Ergebnisse zitieren, **wenn echte Zahlen vorliegen**.
- Förder-Kontext mitdenken (BAFA EBN/EEW, KfW, §71a GEG, DIN EN 16247, EPBD).
- Inhalte in Markdown/YAML pflegen — Inhaber muss im GitHub-Webeditor editieren können.
- Texte ausschließlich in `_data/site.yml` und Markdown-Dateien, niemals in Layouts/Includes hardcoden.

### DON'T

- Keine fiktiven Kennzahlen (wenn unbekannt: weglassen).
- Keine Count-Up-Animationen auf Zahlen (wirkt unseriös).
- Keine Kundenlogos ohne bestätigte Bildrechte.
- Keine KI-generierten Stockfotos, keine Whiteboard-CO₂-Klischees.
- Keine Google Fonts CDN, Google Analytics, Google Maps, Meta Pixel.
- Keine Cookie-Banner.
- Keine neuen Dependencies (npm, zusätzliche Gems, …).
- Kein Kontaktformular (bewusste Entscheidung: E-Mail + Cal.com).
- Keine Feature-Erweiterungen ohne explizite Freigabe.

## Neue Branchen-Landingpage anlegen

`camping.md` ist das Muster. Datei kopieren, `permalink:`, `title:`,
`description:` und Inhalte anpassen. Schema:

1. Hero (Overline + H1 + Lede + CTAs) im Layout `landing`
2. Typische Schmerzpunkte (`.pain-list`)
3. Vorgehen (`.steps` mit 4 Schritten)
4. Branchen-Referenzen (`.ref-list`)
5. Quick-Check als Einstieg
6. `{% include cta.html %}`

## Arbeitsweise

Der Inhaber arbeitet in **Phasen mit Review-Gates**. Nach jeder abgeschlossenen
Phase stoppen und fragen, ob die nächste beginnen soll. Nicht autonom
weiterlaufen.
