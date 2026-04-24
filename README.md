# wuenergie.de

Statische Website für **WuEnergie / Ing.-Büro Jörg Wünnenberg** (Staufen im Breisgau).

Gebaut mit **Jekyll**, gehostet auf **GitHub Pages**. Keine npm-Abhängigkeiten, kein lokaler Build nötig — GitHub baut die Seite automatisch aus dem `main`-Branch.

## Texte ändern

Alle Inhalte liegen als Markdown und YAML im Repo:

| Datei                  | Inhalt                                                       |
| ---------------------- | ------------------------------------------------------------ |
| `_data/site.yml`       | Kontaktdaten, Kernsatz, Buchungs-Link, Qualifikations-Badges |
| `_data/referenzen.yml` | Liste aller Referenzen                                       |
| `index.md`             | Startseite (`/`)                                             |
| `camping.md`           | Landingpage Campingplätze (`/camping/`)                      |
| `impressum.md`         | Impressum (`/impressum/`)                                    |
| `datenschutz.md`       | Datenschutz (`/datenschutz/`)                                |

### Ändern direkt auf github.com

1. Datei im Repo öffnen
2. Oben rechts auf das Stift-Symbol klicken
3. Text ändern
4. Unten auf „Commit changes" klicken

Nach 1–2 Minuten ist die Änderung live auf wuenergie.de.

## Neue Branchen-Landingpage anlegen

1. Datei `camping.md` kopieren, z.B. als `hotels.md`
2. Im Front-Matter `permalink: /hotels/` und `title:` anpassen
3. Inhalte schreiben, committen — fertig. Erreichbar unter `/hotels/`.

## Lokal ansehen (optional)

Nur nötig, wenn Änderungen vor dem Push geprüft werden sollen. Voraussetzung: **Ruby** (auf macOS meist vorinstalliert).

```sh
bundle install              # einmalig — installiert Jekyll & Plugins
bundle exec jekyll serve    # startet http://localhost:4000 mit Live-Reload
```

In VSCode gibt's dafür auch einen Task: `Terminal → Run Task… → Jekyll: Serve`.

Einfacher für einmalige Änderungen: direkt auf GitHub committen — Tippfehler fallen dort ohnehin sofort auf, weil die Seite in 1–2 Minuten live geht.

## Domain

`wuenergie.de` zeigt per `CNAME`-Datei (Repo-Root) auf GitHub Pages. DNS beim Registrar muss auf GitHub-Pages-IPs verweisen:

```text
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

Oder als CNAME auf `<user>.github.io`.

## Technische Schwestermarke

[wuennenberg.org](https://wuennenberg.org) ist die separate, technisch-ingenieurliche Marke (WordPress, eigenständig). Im Footer wird dorthin verlinkt.

---

## Für Entwickler: Repo-Aufbau

Wenn du eine Datei siehst und dich fragst, was sie tut:

| Pfad                     | Zweck                                                                            |
| ------------------------ | -------------------------------------------------------------------------------- |
| `_config.yml`            | Jekyll-Hauptkonfiguration (Titel, URL, Plugins, Sprache, Zeitzone)               |
| `_layouts/*.html`        | Seiten-Templates (`default`, `landing`) mit Header/Footer                        |
| `_includes/*.html`       | Wiederverwendbare Bausteine: `head.html`, `footer.html`, `cta.html`              |
| `_data/*.yml`            | Datengetriebene Inhalte (zentrale Quelle für Kontakt, Referenzen)                |
| `assets/css/style.css`   | Einzige CSS-Datei — handgepflegt, CSS-Variablen, `clamp()`                       |
| `favicon.svg`            | Brand-Icon (Teal „W")                                                            |
| `robots.txt`             | Crawler-Regeln + Verweis auf die automatisch generierte `sitemap.xml`            |
| `CNAME`                  | Custom Domain für GitHub Pages                                                   |
| `Gemfile`                | Ruby-Abhängigkeiten für die optionale lokale Vorschau                            |
| `.editorconfig`          | Formatierungs-Defaults (UTF-8, LF, 2 Spaces) — editorübergreifend                |
| `.markdownlint.jsonc`    | Markdown-Linter-Regeln (wird von VSCode-Extension gelesen)                       |
| `.cspell.json`           | Rechtschreibprüfung DE+EN mit projektspezifischem Wörterbuch                     |
| `.vscode/`               | VSCode-Workspace-Einstellungen + empfohlene Extensions                           |
| `CLAUDE.md`              | Projekt-Briefing für Claude-Code-Sessions (Tonalität, Stack, Tabus)              |

### Empfohlene VSCode-Extensions

Beim ersten Öffnen bietet VSCode die Installation an (`.vscode/extensions.json`):

- **Markdownlint** — Warnungen bei Markdown-Problemen
- **Code Spell Checker** + **German** — Rechtschreibung DE+EN
- **YAML (Red Hat)** — Validierung von `_data/*.yml` und `_config.yml`
- **Shopify Liquid** — Syntax-Highlighting für Jekyll-Templates
- **EditorConfig** — respektiert `.editorconfig`

Alle Linter laufen rein lokal in VSCode — keine Node-/npm-Installation nötig.

### Bewusste Nicht-Entscheidungen

Siehe [`CLAUDE.md`](./CLAUDE.md) für das vollständige Briefing. Kurzfassung:

- **Keine** npm-/Node-Toolchain, **kein** Bundler-Build im CI
- **Keine** Google Fonts, Google Analytics, Cookie-Banner, Kontaktformulare
- **Keine** Kundenlogos ohne Bildrechte, **keine** fiktiven Kennzahlen
