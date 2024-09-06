# Parzivals ODD‑Âventiuren

Die Suche nach dem ewig wartbaren Gral

---

## Parzival-Legacy
wie lief es in der Vergangenheit? Tustep, php, manuell bearbeitetes HTML

---

## Pilotanwendung TEIPublisher
erste Idee (TH): klassischer TEIPublisher-Stack
aber Anspruch: Funktionserhalt, UI/UX-Entscheidungen beibehalten
### roadblocks:
Revisionskontrolle
Organisation der Seite
passt nicht zu XML-Struktur
passt nicht zum Aufbau der Edition
fehlende webcomponents-Expertise
allg. uptake sehr limitiert
---
### Einsicht nach einiger Zeit: neues Konzept nötig

TEIPublisher nur für rendering der text views / Transkriptionen
gut: kleingranular möglich durch XQuery-API (rendered snippets)
ODD nur CSS-Klassen
Frontend
Funktionalität und finales Design nur im Frontend
D3 u.ä. (Kartenvisualisierungen) im Frontend
statisches Backend
Strukturdateien und Metadent versionskontrolliert über eigene API (skriptbasiert, GH Actions)


---

## Red Flags

technical
revision control (data files)
non-containment; jede App braucht eigene TEIPb-Instanz (aber mehrere TEIPb auf 1 eXist möglich?)
required expertise (sys admin)
versions chaos (Sebi’s notes)
