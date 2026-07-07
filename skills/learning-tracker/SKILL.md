---
name: learning-tracker
description: Automatischer Learning-Prozess des Content-Teams. Analysiert das laufende Gespräch auf NEUE Erkenntnisse (die noch nicht im Repo/Content-System stehen), sortiert sie nach Vales etablierten Kategorien und erzeugt eine fertige, autonom lauffähige learning-<N>.md für Claude Code. Verwenden bei "learnings", "learning update", "was haben wir gelernt", "neue erkenntnisse fürs system", "learning file", "mach ein learning". Nimmt NUR Neues auf (nichts bereits Umgesetztes). Fasst den Kern (frameworks/) nie an; n=1-Inhaltliches bleibt Hypothese.
---

# Learning-Tracker

Du automatisierst, was bei Learning 1 und 2 manuell lief: neue Erkenntnisse erkennen, einsortieren,
und eine fertige, autonom lauffähige learning-<N>.md ausgeben, die Claude Code ohne Rückfragen umsetzt.

## Zwingende erste Handlung
1. Lies references/learning-ledger.md — daraus ergibt sich die letzte verarbeitete Learning-Nummer und
   was bereits umgesetzt wurde. Die neue Datei heißt learning-<letzte+1>.md.
2. Lies references/learnings.md, references/kanal-profile.md und die betroffenen skills/*/SKILL.md, um
   abzugleichen, was schon im Repo steht.

## Was als NEUES Learning zählt (nur das aufnehmen)
Vergleiche das laufende Gespräch gegen Ledger + Repo. Nimm NUR auf, was dort noch NICHT steht. Sortiere
jedes neue Learning in eine dieser Kategorien:
- Prozess-Learning (Arbeitsschritt/Regel, keine inhaltliche Wette) → darf in Skills/Profil.
- Vales Planungsprozess-Präferenz → darf in regisseur/Profil.
- Inhaltliche Hypothese (Wette über Wirkung, n-abhängig) → NUR ins Journal, als HYPOTHESE.
- Status-Update (bestehende Hypothese erreicht n≥3 + Vale-OK) → Hochstufung im Journal.

## Drift-Schutz (hart)
- frameworks/ nie anfassen. learnings.md append-only. n=1 nie als Regel. Nichts löschen.
- Inhaltliche Hypothesen werden erst mit n≥3 UND Vales ausdrücklichem OK zur Regel.

## Deine Ausgabe: eine fertige learning-<N>.md
Baue sie nach EXAKT diesem Muster (wie Learning 1/2), damit sie autonom in Claude Code läuft:
1. Kopf: Kontext, Verhältnis zu vorherigen Learnings (ergänzt, überschreibt nicht), Drift-Schutz.
2. Teil A: Prozess-Learnings (dürfen in den Kern).
3. Teil B: Vales Planungsprozess-Präferenzen (falls neue dazukamen).
4. Teil C: Inhaltliche Hypothesen (nur Journal) + etwaige Status-Updates.
5. Teil D: EIN Claude-Code-Prompt in durchnummerierten Schritten. Pro Schritt: exakte Datei + Abschnitt
   + wörtlicher Einfügetext. Am Anfang: "keine Rückfragen, bei Mehrdeutigkeit konventionsnächste
   Variante". Harte Regeln oben (frameworks/ tabu, append-only, nichts löschen). Enthält am Ende
   git commit + git push.
6. Teil E: Checkliste "Damit es wirklich greift" (Prompt laufen lassen → Push prüfen → Plugin updaten).
7. WICHTIG: Der Prompt muss als LETZTEN Schritt references/learning-ledger.md aktualisieren (neue
   Learning-Nummer + Stichworte der jetzt umgesetzten Learnings anhängen), damit beim nächsten Mal klar
   ist, was schon verarbeitet wurde.

## Ablauf, wenn Vale "learnings" sagt
1. Ledger + Repo lesen. 2. Gespräch auf Neues analysieren, kategorisieren. 3. Wenn nichts Neues: das
ehrlich sagen, keine leere Datei bauen. 4. Sonst: die learning-<N>.md erzeugen und als Datei ausgeben
(Chat: zum Download; Claude Code: ins Repo-Root schreiben). 5. Vale kurz zusammenfassen, was neu ist und
was der Prompt tun wird.

## Was du NICHT tust
- Keine frameworks/ ändern. Nicht selbst ins learnings.md schreiben (das macht der performance-analyst
  bzw. der erzeugte Prompt). Keine alten, schon umgesetzten Learnings erneut aufnehmen.
