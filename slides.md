# Parzivals ODD‑Âventiuren

Die Suche nach dem ewig wartbaren Gral

---

## Parzival-Legacy

![legacy-Parzival-Screenshot](/img/image.png)

<style>
    .slide img {
        max-height: 500px;        
    }
</style>

## <!-- etwas über die Wichtigkeit des Projekts sagen, wie lange es schon läuft. Dass da über Jahre verschiedene Leute daran gearbeitet haben -->

### Legacy Workflow

Tustep
`$<*T 103.07>_[name ref="rego:o0254" type="Ort"]Waleis[/name] und [name ref="rego:o0012" type="Ort"]Anschouwe[/name],`

--> TXT
`21;r;a;103;6;;d(er) kvneginne vber driv lant`

--> SQL-DB --> php --> HTML
`<td><span class="versheader">103.<a name="103.6">6</a></span> <span class="vers-content">d<span class="7">(er)</span> kvneginne vber driv lant</span></td>`

---

## Pilotanwendung TEIPublisher

## erste Idee: klassischer TEIPublisher-Stack

Anspruch: Funktionserhalt, UI/UX-Entscheidungen beibehalten

---

![verssynopse](/img/synopsis.png)

---

![wireframe-verssynopse](/img/wf-synopsis.jpg)

---

[![new-synopse](/img/new-synopse.png)](https://dhbern.github.io/presentation_parzival/textzeugen/d-mk/719/25)

---

### roadblocks:

_add some meme here_

---

Revisionskontrolle

---

Organisation der Seite
passt nicht zu XML-Struktur
passt nicht zum Aufbau der Edition

---

fehlende webcomponents-Expertise
allg. uptake sehr limitiert

---

### neues Konzept

TEIPublisher nur für rendering der text views / Transkriptionen
gut: kleingranular möglich durch XQuery-API (rendered snippets)

---

ODD nur CSS-Klassen
Funktionalität und finales Design nur im Frontend
D3 u.ä. (Kartenvisualisierungen) im Frontend

---

statisches Backend
Strukturdateien und Metadent versionskontrolliert über eigene API (skriptbasiert, GH Actions)

---

## Red Flags

technical
revision control (data files)
non-containment; jede App braucht eigene TEIPb-Instanz (aber mehrere TEIPb auf 1 eXist möglich?)
required expertise (sys admin)
versions chaos:

- verschiedene integrale Bestandteile die niemals unabhängig von TEIP genutzt werden sind einzeln versioniert und funktionieren aber nur mit einer einzigen Version jeweils.
  - Exist-db
  - Tei Publisher
  - Web components
  - API
  - exide
  - roaster
  - dashboard
  - existdb-login
  - EXPath Bin Module
  - Launcher
  - undundund...
