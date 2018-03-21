# teutoinfo - LaTeX-Paket zum Erzeugen von Teuto-Infos

`teutoinfo` ist ein LaTeX-Paket zur Erzeugung von Teuto-Infos
(Mitgliederzeitschrift der [PV Teutonia 1842 zu Rastatt](http://www.pv-teutonia.org/)).

## Systemvoraussetzungen

Das Paket benötigt mindestens

- LaTeX2e von 1994
- Die LaTeX-Pakete
    - babel (mit Sprache ngerman)
    - fancybox
    - fancyhdr
    - geometry
    - inputenc (mit Kodierung utf-8)
    - mdframed
    - multicol
    - xkeyval
    - xstring

Auf einem Ubuntu 16.04-System genügt hierfür die Installation von
`texlive-latex-extra`, `texlive-lang-german` und allen Abhängigkeiten. Dazu
müssen etwa 775 MB an Paketen heruntergeladen werden, die LaTeX-Installation ist
dann etwa 1,2 GB groß.

## Installation

Die Paketdatei `teutoinfo.sty` muss im selben Verzeichnis wie die Teuto-Info
liegen, damit LaTeX sie findet. Alternativ kann sie auch in das Verzeichnis
`$TEXMFHOME` gelegt werden (normalerweise ist das `~/texmf/`), und zwar auf den
folgenden Pfad:

```
$TEXMFHOME/tex/latex/teutoinfo/teutoinfo.sty
```

Weitere Informationen gibt es
[hier](https://en.wikibooks.org/wiki/LaTeX/Creating_Packages#Creating_your_own_package).

## Verwendung

Ein minimales funktionierendes Beispiel ist in der Datei `beispiel.tex` zu
finden. Das Paket erwartet zwingend vier Optionen, die als kommaseparierte
Liste von Variable/Wert-Paaren geliefert werden müssen (a=b,c=d,...):

- `issue`: laufende Nummer der Ausgabe im derzeitigen Jahr
- `month`: Name des Monats der Veröffentlichung
- `year`: Jahr der Veröffentlichung

Ein Beispiel für die Paketeinbindung:

```latex
\usepackage[issue=2,month=April,year=2018]{teutoinfo}
```

## Lizenz

Das Paket steht unter der MIT-Lizenz (siehe Datei LICENSE) und kann nach deren
Bestimmungen frei weiterverwendet werden.
