# content-team — Vales virales Content-System

Ein Plugin aus **6 zusammenspielenden Skills**, destilliert aus deinen drei Framework-Videos
(Hooks, Dopamine Ladder, Algorithmus). Zusammen ergeben sie ein Team, das weiß, was ein
viral gehendes und konvertierendes Video ausmacht — und es als fertiges Produktionsdokument liefert.

## Das Team

| Skill | Rolle | Wofür |
|-------|-------|-------|
| **regisseur** | Orchestrator | Einstieg für neue Videos. Führt die ganze Pipeline, liefert nur geprüfte Dokumente. |
| **content-strategist** | Gatekeeper | Prüft Ideen gegen Kanal & Avatar, sagt auch mal "verwirf das". |
| **hook-architekt** | Hooks | 2–3 Hook-Varianten, Key-Visual-first, 4-Komponenten-Alignment. |
| **story-architekt** | Skript | Volles Produktionsdokument entlang der Dopamine Ladder. |
| **script-doctor** | Kritiker | Auditiert deine Drafts UND reverse-engineert fremde/virale Videos. |
| **performance-analyst** | Lern-Loop | Lernt aus deinen Zahlen dazu — ohne den Kern kaputtzuoptimieren. |

## So benutzt du es

**Neues Video (voller Ablauf):**
> "Neues Video für Deussen über die Villa in Urdenbach."

→ Der **regisseur** übernimmt: fragt dich den festen Einstiegs-Fragebogen ab (Kanal, Thema, Format,
Key Visual, Ziel, Short/Long), läuft dann Strategie → Hook → Skript → Audit durch und gibt dir das
fertige Produktionsdokument.

**Einzelne Bausteine (direkt):**
> "Schreib mir 3 Hooks für dieses Reel." → **hook-architekt**
> "Passt diese Idee auf meinen Personal-Brand-Kanal?" → **content-strategist**
> "Warum hat dieses fremde Video 15M Views?" → **script-doctor** (Reverse-Engineering)
> "Hier sind die Zahlen von gestern." → **performance-analyst**

## Wie es dazulernt (ohne Drift)

- Der **Kern** (die Frameworks) ist unantastbar. Kein Skill schreibt ihn um.
- Ergebnisse gehen ins **Lern-Journal** (`references/learnings.md`), append-only.
- Eine Beobachtung wird erst zur **Regel**, wenn sie sich über **≥3 Videos** zeigt UND du sie
  abnickst. Bis dahin bleibt sie eine Hypothese.
- **Formate** leben in der `format-bibliothek.md`: Evergreen-Set ist stabil; neue Trend-Formate
  bekommen ein Verfallsdatum und müssen sich beweisen.

## Was du noch tun solltest

1. **`references/kanal-profile.md` prüfen.** Ich habe deine 3 Kanäle vorbefüllt (Deussen als
   Entertainment-first mit Dual-Zielgruppe, KYM, Personal Brand). Korrigier, was nicht stimmt.
2. **Grenzen kennen:** Die Skills können keine Videos ansehen. Für Analysen fütterst du Transkript
   (ziehst du selbst) + Kurzbeschreibungen von Key Visual, Text-Overlays, Audio, Schnitt. Der
   script-doctor fragt dich diesen festen Input immer gleich ab.

## Installation (Claude.ai / Cowork / Desktop — über GitHub)

Dieses Repo IST ein Marketplace. Nach dem Hochladen auf GitHub (öffentlich):

**Im Chat / in Cowork:**
1. Customize-Menü → Tab **Plugins**.
2. Bereich **Personal plugins** → **"+"** → **"Add marketplace"**.
3. Dein GitHub-Repo angeben (z.B. `karlowskivalentin-gif/vale-content-marketplace`).
4. `content-team` erscheint im Katalog → installieren.

**In Claude Code (Terminal), falls gewünscht:**
```
/plugin marketplace add karlowskivalentin-gif/<repo-name>
/plugin install content-team@vale-content-marketplace
```

Die Skills heißen nach der Installation `content-team:regisseur`, `content-team:hook-architekt` usw.
Hooks/Sub-Agents laufen nur in Cowork; im reinen Chat sind die Skills trotzdem voll nutzbar.

## Struktur

```
content-team/                     ← Repo-Root = Marketplace
├── .claude-plugin/
│   ├── plugin.json               (Plugin-Manifest)
│   └── marketplace.json          (Marketplace-Katalog)
├── README.md
├── skills/
│   ├── regisseur/SKILL.md
│   ├── content-strategist/SKILL.md
│   ├── hook-architekt/SKILL.md
│   ├── story-architekt/SKILL.md
│   ├── script-doctor/SKILL.md
│   └── performance-analyst/SKILL.md
└── references/
    ├── kanal-profile.md          (editierbar — deine 3 Kanäle)
    ├── format-bibliothek.md      (Evergreen + Trend-Formate)
    ├── learnings.md              (append-only Lern-Journal)
    └── frameworks/
        ├── 01-hooks.md
        ├── 02-dopamine-ladder.md
        └── 03-algorithmus-strategie.md
```
