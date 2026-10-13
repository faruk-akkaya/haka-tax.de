# haka-tax — Druckvorlagen

Vorlagen für Kuverts, Berichtsdeckblätter und Aufkleber, aufgebaut aus dem
freigegebenen Markenzeichen und den Maßregeln aus `../markenrichtlinien.md`.

Jede Vorlage liegt als **SVG** (bearbeitbar) und als **PDF** (druckfertig) vor.

## Inhalt

| Datei | Endformat | Verwendung |
|---|---|---|
| `kuvert-DL-mit-fenster` | 220 × 110 mm | DIN-lang-Kuvert mit Sichtfenster, Standardversand |
| `kuvert-DL-ohne-fenster` | 220 × 110 mm | DIN lang ohne Fenster, Empfänger wird aufgedruckt |
| `kuvert-C5-mit-fenster` | 229 × 162 mm | C5 für ungefaltete A5- bzw. einmal gefaltete A4-Post |
| `kuvert-C4-ohne-fenster` | 229 × 324 mm | C4 für ungefaltete A4-Post, Berichte, Jahresabschlüsse |
| `deckblatt-bericht-mit-fenster` | 210 × 297 mm | Berichtsdeckblatt mit Stanzfenster, Titel der Innenseite scheint durch |
| `deckblatt-bericht` | 210 × 297 mm | Berichtsdeckblatt geschlossen, Titel wird aufgedruckt |
| `aufkleber-kuvert-gross-A4` | 8 × 99,1 × 67,7 mm | Absenderaufkleber mit vollem Kanzleiblock für neutrale Kuverts |
| `aufkleber-absender-klein-A4` | 21 × 63,5 × 38,1 mm | kompakter Absenderaufkleber |

## Technische Angaben

**Endformat ohne Beschnitt.** Kein Element läuft bis an die Kante, die Dateien
liegen daher in der exakten Endgröße vor. Das ist Absicht: Kuverts lassen sich
wegen der Klebelaschen und des ungenauen Anlagestands in der Maschine selten
randabfallend bedrucken. Verlangt eine Druckerei trotzdem Beschnitt, genügt es,
den weißen Hintergrund um 3 mm nach allen Seiten zu vergrößern — es liegt kein
Motiv in der Beschnittzone.

**Schrift ist in Pfade gewandelt.** Weder SVG noch PDF brauchen eine
installierte Schrift; die Dateien geben überall identisch aus. Für Textänderungen
siehe „Vorlagen ändern" unten.

**Maßgenauigkeit.** Die SVG-Dateien sind exakt. Die PDFs können durch die
Umrechnung in Punkt um bis zu 0,2 mm abweichen (z. B. C4 mit 323,8 statt
324,0 mm) — das liegt weit innerhalb der Fertigungstoleranz von Kuverts und
Schneidemaschinen.

**Farben.** Vierfarbig (CMYK) drucken, Werte aus dem Markenhandbuch:

| Farbe | Hex | CMYK |
|---|---|---|
| HakaGold | `#D9A441` | 14 / 36 / 85 / 0 |
| HakaGrey | `#8B7D85` | 45 / 45 / 34 / 17 |
| HakaBerry | `#9B1E52` | 28 / 100 / 36 / 23 |
| HakaDark | `#5A1230` | 40 / 100 / 41 / 60 |
| Text | `#211E19` | — |
| Wasserzeichen | `#EFECEE` | HakaGrey mit rund 14 % Tonwert |

Das Wasserzeichen ist die einfarbige Fassung der Bildmarke. Es wird nicht
gedreht und nicht beschnitten — die Marke steht vollständig im Satzspiegel.

## Kuverts

Das Sichtfenster gehört zum Kuvert, nicht zum Druckbild: in den Druckdateien ist
es deshalb **nicht** eingezeichnet. Maßgeblich ist DIN 680 — Fenster 90 × 45 mm,
20 mm von links, 15 mm von unten. Die Vorlagen halten diesen Bereich frei.

Beim Bestellen bei einer Kuvertdruckerei anzugeben:

- Format und Fenster (z. B. „DIN lang, Fenster rechts/links nach DIN 680")
- Druck 4/0 (einseitig vierfarbig)
- Papier 90–100 g/m², weiß, ohne Recyclinggrau — der helle Grund trägt das
  Wasserzeichen
- Haftklebung oder nassklebend, nach Bedarf

## Berichtsdeckblatt

Zwei Fassungen:

- **mit Stanzfenster** — die untere rechte Ecke des Fensters ist auf 45° gefast,
  dieselbe Schräge wie in der Bildmarke. Das Fenster gibt den Titel der ersten
  Innenseite frei. Die Stanzkontur liegt als magentafarbene Linie (`#E6007E`,
  0,25 mm, gestrichelt) in der Datei und ist für die Druckerei als **Stanzform
  auf eigener Ebene / Sonderfarbe „Stanzkontur"** anzulegen. Sie druckt nicht mit.
  Lage: 53 / 74 mm, 104 × 96 mm, Fase 20 mm.
- **geschlossen** — Titelfeld wird mitgedruckt oder vom Bürodrucker gefüllt.
  Die Platzhalter in eckigen Klammern ersetzen.

Empfehlung: 200–250 g/m² für das Deckblatt, damit die Stanzung sauber steht.

## Aufkleber

Die Bogen passen auf handelsübliche Etikettenbogen:

| Vorlage | Etikett | passende Artikel |
|---|---|---|
| `aufkleber-kuvert-gross-A4` | 99,1 × 67,7 mm, 2 × 4 | Avery Zweckform 3652 / L7165, Herma 4458 |
| `aufkleber-absender-klein-A4` | 63,5 × 38,1 mm, 3 × 7 | Avery Zweckform 3425 / L7160, Herma 4625 |

Beim Drucken aus dem PDF unbedingt **„Tatsächliche Größe" / Skalierung 100 %**
einstellen — „An Seite anpassen" verschiebt das Raster gegenüber der Stanzung.
Vor der ersten Charge einen Probedruck auf Normalpapier machen und gegen einen
Etikettenbogen halten.

## Vorlagen ändern

Weil die Schrift in Pfaden liegt, lässt sich Text nicht mehr direkt editieren.
Für Änderungen (Adresse, Durchwahl, Platzhalter) die Vorlagen neu erzeugen statt
die SVG-Pfade zu bearbeiten — die Erzeugung ist in der Projekthistorie
dokumentiert und setzt auf denselben Master-Pfaden und Maßregeln auf wie die
Dateien in `../`.

Kurzfristige Einzelfälle: im SVG den betreffenden `<path>` löschen und ein
`<text>`-Element mit `font-family="Inter"` an derselben Stelle einsetzen — dann
muss auf dem ausgebenden Rechner aber Inter installiert sein.

## Vor der Beauftragung

Formale Markenrecherche (DPMA/EUIPO) auf die Bildmarke, falls noch nicht
geschehen — siehe `../markenrichtlinien.md`.
