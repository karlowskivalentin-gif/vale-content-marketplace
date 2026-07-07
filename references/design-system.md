# Design-System: Deussen CI + Vale-Signatur

> **Verbindliches Design-System** für alle Deussen-Deliverables (Skripte, Shotlists,
> Edit-Pipelines, PDFs, Word-Dokumente) aus dem content-team-Plugin.
> Quelle: offizielles Deussen-Brandbook (`#Brandbook.pdf`, Deussen Immobilien) + Co-Branding-Regeln
> von Vale. Diese Datei **ersetzt** ältere Layout-Angaben in den Skills (insbesondere den früheren
> Gold-Standard #B08D57 — Gold ist KEINE Deussen-Markenfarbe mehr).

---

## 1. Grundprinzip & Co-Branding

**„Deussen dominiert, Vale signiert."**

- Deussen-Deliverables sehen zu 100 % nach Deussen aus: Deussen-Farben, Deussen-Logo,
  Deussen-Typografie.
- Vale erscheint ausschließlich als **dezente Signatur in der Fußzeile** (kleines Vale-Logo
  bzw. „erstellt von vale video"-Zeile) — niemals gleichrangig mit dem Deussen-Branding,
  niemals im Header.

## 2. Farben (Deussen)

### Primärpalette
| Farbe | HEX | RGB | Verwendung |
|---|---|---|---|
| **Midnight Royal Blue** | `#25408F` | 37, 64, 143 | Leitfarbe: Headlines, VO-Boxen, Akzentlinien, Labels |
| **Jet Black** | `#151515` | 21, 21, 21 | Fließtext, Wortmarke |
| **Light Neutral Gray** | `#CCCCCC` | 204, 204, 204 | Trennlinien, Hintergrund-Flächen, Meta-Text |

### Akzentpalette (sparsam, nie als Leitfarbe)
| Farbe | HEX | RGB |
|---|---|---|
| Sky Ice Blue | `#8DD7FC` | 141, 215, 252 |
| Neon Mint Green | `#4DFF8D` | 77, 255, 141 |
| Golden Sun Yellow | `#FFD522` | 255, 213, 34 |

**Regel:** Leitfarbe der Deliverables ist **Midnight Royal Blue `#25408F` — NICHT Gold**.
Das früher in den Skills verwendete Gold `#B08D57` stammt nicht aus dem Brandbook und wird
nicht mehr verwendet.

## 3. Logo (Deussen)

Das Deussen-Logo (Bildmarke „di" in Midnight Royal Blue + Wortmarke „DEUSSEN IMMOBILIEN" in
Jet Black) steht in jedem Deliverable **eingebettet im Header** — kein Text-Platzhalter.

**Repo-Pfade (verbindlich):**
- Primär: `references/assets/logos/deussen/deussen-logo.svg`
- Fallback: `references/assets/logos/deussen/deussen-logo.png` (1200 px, aus dem SVG gerendert)

> Bei der Dokument-Erstellung werden diese Dateien zum Einbetten verwendet; die ebenfalls
> vorhandene `.ai`-Datei wird nicht genutzt (nur SVG/PNG).

**Usage-Regeln (aus dem Brandbook):**
- Schutzraum: rundum ca. **20 %** der Logo-Gesamthöhe freihalten.
- **Kein** Drop-Shadow, **nicht** verzerren/strecken, **keine** Kontur (Stroke),
  **keine** markenfremden Farben.
- Auf dunklem Grund die Reverse-/helle Variante bevorzugen (falls nicht vorhanden:
  ausreichend hellen Hintergrund hinter das Logo legen).

## 4. Typografie

- **Primärschrift: Poppins** — für alles (Headlines, Labels, Fließtext, VO-Boxen).
  Verfügbare Schnitte im Vale-OS: Poppins Regular, Medium, Bold
  (`Vale-OS\02_Projekte\Deussen-Immobilien\deussen_branddesign\`).
- **Sekundärschrift: Lexend** — nur wenn Poppins nicht verfügbar ist (z. B. Systemgrenzen);
  generischer Fallback: sans-serif.
- **Hierarchie (Brandbook):** H1–H3 SemiBold, H4 Medium, Fließtext Regular/Light.
- Headlines in Jet Black `#151515` oder Midnight Royal Blue `#25408F`, niemals in Akzentfarben.

## 5. Deliverable-Layout (Skript / Shotlist / Edit-Pipeline)

- **Header:** eingebettetes Deussen-Logo + dezentes „DEUSSEN IMMOBILIEN"-Label, darunter
  Dokumenttitel (Poppins SemiBold) und feine Akzentlinie in `#25408F`.
- **Beat-Struktur:** pro Beat eine Kopfzeile (`BEAT N · Phase · Timecode`), darunter der
  Sprechtext in einer **blau akzentuierten Box** (`#25408F` als Rahmen/Balken bzw. sehr helles
  Blau als Flächen-Tint) — fett, gut lesbar, teleprompter-tauglich. **Nicht Gold.**
- **Scanbarkeit:** in Sekunden erfassbar; großzügiger Weißraum, klare Trennlinien in `#CCCCCC`.
- **Ausgabe:** Word UND PDF, sofern Vale nichts anderes sagt.
- **Fußzeile:** Vale-Signatur (siehe Abschnitt 7) + Seitenzahl + Stand-Datum.

## 6. Datei-Einbettung

- Zum Einbetten in Dokumente ausschließlich die **SVG-** (bevorzugt) oder **PNG-Dateien**
  aus `references/assets/logos/` verwenden; `.ai` wird nie eingebettet.
- Logos nie neu einfärben, nie beschneiden, Seitenverhältnis immer beibehalten.

## 7. Vale-Branding (Signatur)

Vale-Markenwerte: Ink-Schwarz `#14110d`, Vale-Orange `#e2622c`, Schrift Inter (ExtraBold für
die Wortmarke). In Deussen-Deliverables erscheint Vale **nur als Signatur in der Fußzeile** —
klein, dezent, einfarbig wirkend (Co-Branding-Regel: „Deussen dominiert, Vale signiert").

**Repo-Pfade (verbindlich):** `references/assets/logos/vale/<name>.png`
(zu jeder Variante liegt zusätzlich eine `.svg` gleichen Namens)

| Datei | Variante | Einsatz |
|---|---|---|
| `references/assets/logos/vale/logohorizontal.png` | Logo + „VALE VIDEO" horizontal | Standard-Signatur auf hellem Grund |
| `references/assets/logos/vale/logohorizontalreverse.png` | horizontale Variante, hell/reverse | Fußzeile auf dunklem Grund |
| `references/assets/logos/vale/logomark.png` | nur Bildmarke | sehr kleine Signatur (z. B. neben Seitenzahl) |
| `references/assets/logos/vale/logomarkoutline.png` | Bildmarke als Outline | maximal dezente Signatur |
| `references/assets/logos/vale/logomarkreverse.png` | Bildmarke hell/reverse | kleine Signatur auf dunklem Grund |
| `references/assets/logos/vale/logowordmark.png` | nur Wortmarke | Text-Signatur ohne Bildmarke |

> Bei der Dokument-Erstellung werden diese Dateien zum Einbetten verwendet; `.ai` wird nicht
> genutzt (nur SVG/PNG).

**Standard für Deussen-Fußzeilen:** `logomarkoutline.png` oder `logohorizontal.png`, Höhe
maximal ca. 60 % der Fußzeilen-Texthöhe-Zeile, kombiniert mit „erstellt von vale video" in
`#CCCCCC`/kleinem Grauton.
