# HTML Notizen

## Week #1 Mittwoch 19.10.22

## html

- keine Programmiersprache

  - weile keine Logik damit erstellt werden kann
  - Markup Language

- Attribute

  - lokal (src für img tag)
  - global (id oder class - auf jeden Tag anwendbar)

- self closing tag

  - < img src="/pfad" / >
          - /> zum Schließen

- immer h1 als erste Überschrift
  - für SEO
  - dann immer Abstufungen h2 -> h3 -> h4 (auch für SEO)

## Donnerstag 20.10.22

- cizzy um Endgeräte zu simulieren (visuell)

## css

- cascading -> bestimmte Reihenfolge

- universal Selektor  ---- *
- type Selektor ----  h1
- class selektor ---- .information

- em: relative zur Schriftgröße des Eltern (parent) Elements
- rem: relative zur Schriftgröße im Root Elements (root {})

- border-radius: 50%; quadratische Bilder werden rund, oder Boxen

- Transparenz: #AABBCC00 bis #AABBCCFF

- box-sizing: border-box;
	- mit * Selektor immer setzen
	- content-box (default Wert)
- *Bild einfügen* 

- < span > ein Element für Schrift
- block vs inline-block
- display: block -> verwandelt inline Element (z.B. span, em, img, ...) in Block Element.

- **Fonts immer runterladen und einfügen auch rechtlisten Gründen
	- kein Verweis auf z.B. Google Fonts

- **inline stylesheet schlägt externes stylesheet
- **die höhere Spezifität gewinnt**
- **was im .css weiter unten steht hat eine höhere Spezifität**
	- classen-name keine Einfluss auf Spezifität

- first paint
	- style im < head > im .html
	- für performance optimierung

- role="list" bei Listen (ul / ol)
	- für Accessability (Screenreader)
	- damit der SR checkt dass es ne Liste ist. wenn z.B. die Punkte entfernt werden (list-style: none)
	
- class immer mit css
- id eher .js
	- kann zu verwirrung führen
	- allgemeine Convention 
	- und auch als Link verwenden zum navigieren erlaubt, weil hat nichts mit css zu tun

- h1 gibt es immer nur 1x auf einer Seite

- margin: auto
	- zum Zentrieren des Elements im Viewport

- base.css für mehrere .css files und .html
	- eigene Session

- < div class="box box1 box2" >
	- mann kann mehrere Klassen vergeben in einem Tag

- Convention BEM (Block Element Modifier)
	- box__bottom--pink

- img -> selector
- color: -> property
- red -> value
- alles zusammen declaration

- margin: 0px 0px 0px 0px;
	- startet bei top
	- geht dann im Uhrzeigersinn weiter

- outline: -> secondary border
	- dotted -> punktiert
	- dashed -> gestrichelt

- ul:first-child -> so kann man das erste Child ansprechen

- placeholder="default text" -> z.B. im INPUT tag

- ./ 
- ../
- / 
	- Unterschiede checken