# Latex Minimalbeispiele
Einige Minimalbeispiele in LaTeX als Beispiele oder Test von Problemen oder packages.

## apacite
Beispiel für die Verwendung des *apacite package*. Ermöglicht das Zitieren und
Referenzieren nach den Regeln der *American Psychological Association* (APA
style).
Links: [APA style](http://www.apastyle.org/), [apacite](https://ctan.org/pkg/apacite)

## beamer-handout
Eine Möglichkeit, mittels 'makefile' aus dem selben LaTeX-Dokument mit der Beamer-Class eine Präsentation sowie ein Handout zu generieren.
Im Präsentationsmodus werden werden bei stufenweisem Aufdecken von Items u.ä. jeweils verschiedene Slides erzeugt,
die im Handout zu einem Slide zusammengefasst werden.

Anwendung:
Folgender Befehl erzeugt eine Beamer-Präsentation `praes.pdf`. Im Beispiel eine einzige Folie, die eine itemweise aufgedeckte Liste zeigt.
```bash
make
```
Mit folgender Option wird ein Handout erzeugt (`handout.pdf`).
```bash
make handout
```
Die unterschiedliche Namensgebung wird mit der pdflatex-Option `-jobname` erreicht,
damit sich bei der Erzeugung der beiden Compiledurchläufe die Ergebnisse sich nicht gegenseitig überschreiben.

## beamer-handout

## box-pfeil

## fallvignette
Eine einfache, selbstdefinierte LaTeX-Umgebung, wie sie z.B. für die
Darstellung eines abgesetzten Textes (Boxtext) gebraucht werden kann. Hier im
Beispiel für eine medizinische Fallvignette.

## flussdiagramm

## framed
Beispiele zum [framed package](https://www.ctan.org/pkg/framed).
Mit diesem Package können umrandete, mit Schatten oder mit einer senkrechten Linie versehene Textabschnitte erzeugt werden.

## font-test

## framed

## gezackte-box

## hamiltondiagramm
Beispiel für ein Säulen-Diagramm mit `tikz`.

## includegraphics
Minimalbeispiel und Test des Befehles `\includegraphics{}`.

## nice_listing

## overpic
## tabellenkalkulation
Test des *spreadtab package*.

## Tastenfont
Darstellung von Tastatur-Zeichen unter Anwendung des *tikz package*.

## test-beamer-artikel

## test-caption

## trennung-deutsch

## tufte_handout_test
