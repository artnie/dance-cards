see below for english version
# Tanzkarten
# LaTeX Tanzkarten für Historische und davon inspirierte Tänze

## [Für Tanzkarten zum Ball in Wuppertal 2022 immer hier entlang](https://github.com/Phayax/dance-cards/blob/ball-2022/BALL.md)

## Download

[Tanzkarten A6 - Alle Tänze zusammen](https://github.com/Phayax/dance-cards/releases/latest/download/Tanzkarten.pdf)  
[Tanzkarten A6 - Ein Tanz pro PDF](https://github.com/Phayax/dance-cards/releases/latest/download/Einzel-Karten.zip)

# Verwendung
### Druck
Die Karten können zum Beispiel mit Adobe Acrobat auf A4 Papier gedruckt werden (immer 4 auf eine Seite).   
Papier schwerer als 200g/m² liefert schöne Ergebnisse.  

Wenn man die Karten doppelseitig drucken möchte, muss man die richtigen Seiten "zueinander" legen, dies erfordert etwas mehr Aufwand, in Kürze wird es hier aber dafür fertige PDFs geben.

## Vorlage weiterverwenden
Empfohlene Software:
 - [TeXstudio](https://www.texstudio.org/) als Editor
 - [TeX Live](https://www.tug.org/texlive/) um die PDFs zu erstellen. Unter Windows kann man auch [MiKTeX ](https://miktex.org/) verwenden, das aber deutlich langsamer mit den Karten ist.
 - Ubuntu macht die Installation dieser Pakete sehr einfacher:
   ```
   sudo apt install texstudio
   sudo apt install texlive-full   # braucht viel Speicherplatz, aber man hat alles...
   ```
   Windows ist natürlich aber auch möglich.
 - [Python](https://www.python.org/), wenn man die aufgeteilten PDFs erstellen möchte.

Nun kann man [`cards.tex`](https://github.com/Phayax/dance-cards/blob/main/cards.tex) in TeXstudio öffnen und beliebige Änderungen vornehmen. 
## Erstellen
Um das PDF zu erstellen empfiehlt sich latexmk. Dafür sollte [`.latexmkrc`](https://github.com/Phayax/dance-cards/blob/main/.latexmkrc) im selben Verzeichnis wie cards.tex liegen. Dann lassen sich die Tanzkarten mit 

`latexmk cards.tex` 

erstellen (das Ergebnis liegt dann im Ordner `.build/`).  
<hr>
Um die Einzelkarten zu erstellen, muss mit python die Datei [`compile.py`](https://github.com/Phayax/dance-cards/blob/main/compile.py) aufgerufen werden:

```python compile.py```

Danach kann in dem Ordner `build-single-temp/` einfach nur 

`latexmk` 

ausgeführt werden. Alle Tanzkarten werden dann im Ordner `.build/` erzeugt.

<br/>
<br/>

  
# Dancing Cards
## LaTeX Calling Cards for historic dances

## All-in-one or separate Cards
The Cards are all in one big .tex file



## Other projects:
#### [Contracard by Sam Whited](https://ctan.org/pkg/contracard)
A LaTeX Package to make Calling Cards in a more standardized way. It defines a lot of moves as LaTeX commands and i find it more useful to just write free text. It does enable fun things like lookups for dance moves though.

## Credit:
Using vector art from [Vectorian](https://www.vectorian.net/free-vintage-vectors.html).
