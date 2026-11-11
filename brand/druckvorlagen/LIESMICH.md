# haka-tax — Druckvorlagen

Stand 11.11.2026. Jede Vorlage liegt als **SVG** (bearbeitbar) und als **PDF**
(druckfertig) vor. Die Schrift ist in Pfade gewandelt: Die Dateien geben überall
identisch aus, es muss keine Schrift installiert sein.

Personalisierte Visitenkarten liegen nur im Markenordner der Kanzlei, nicht in diesem
Repository. Hier liegen Rückseite und editierbare Vorlage.

## Inhalt

| Ordner | Datei | Endformat | Verwendung |
|---|---|---|---|
| `Visitenkarten` | `visitenkarte-vorderseite-<name>` | 85 × 55 mm | Vorderseite je Person |
| | `visitenkarte-rueckseite` | 85 × 55 mm | gemeinsame Rückseite |
| | `visitenkarte-vorderseite-VORLAGE-editierbar.svg` | 85 × 55 mm | für neue Personen, Text noch editierbar |
| `Kuverts` | `kuvert-DL-mit-fenster` | 220 × 110 mm | Standardversand, passt zum Briefbogen |
| | `kuvert-DL-ohne-fenster` | 220 × 110 mm | Empfänger wird aufgedruckt oder aufgeklebt |
| | `kuvert-C5-mit-fenster` | 229 × 162 mm | einmal gefaltete A4-Post |
| | `kuvert-C4-ohne-fenster` | 229 × 324 mm | ungefaltete A4-Post, Berichte, Jahresabschlüsse |
| `Berichtsdeckblatt` | `deckblatt-bericht-mit-stanzfenster` | 210 × 297 mm | Karton über dem Word-Deckblatt |
| | `deckblatt-bericht-geschlossen` | 210 × 297 mm | Karton, Titel wird aufgedruckt |
| `Aufkleber` | `aufkleber-kuvert-gross-A4` | 8 × 99,1 × 67,7 mm | Absender mit vollem Kanzleiblock |
| | `aufkleber-absender-klein-A4` | 21 × 63,5 × 38,1 mm | kompakter Absender für neutrale Kuverts |

## Visitenkarten

Die Dateien messen 89 × 59 mm: 85 × 55 mm Endformat plus 2 mm Anschnitt rundum.
Vorderseite 4/0-farbig auf Weiß, Rückseite HakaDark vollflächig mit dem Icon.
Empfehlung: 350 g/m² Naturpapier matt, ungestrichen.

Auf den Karten steht die zentrale Telefonnummer. Sobald die Durchwahlen feststehen,
werden die Karten neu erzeugt — bitte vorher nicht in Druck geben.

## Kuverts

Das Sichtfenster gehört zum Kuvert, nicht zum Druckbild, und ist deshalb nicht
eingezeichnet. Maßgeblich ist DIN 680: Fenster 90 × 45 mm, 20 mm von links, 15 mm von
unten. Die Vorlagen halten diesen Bereich frei; die Anschrift des Briefbogens sitzt
genau darin.

Beim Bestellen angeben: Format und Fenster (z. B. „DIN lang, Fenster links nach
DIN 680“), Druck 4/0, Papier 90–100 g/m² weiß, Haftklebung oder nassklebend.

Die Dateien liegen im Endformat ohne Beschnitt vor. Das angeschnittene Icon in hellem
Grau läuft bewusst über die Kante: Verlangt die Druckerei Beschnitt, den weißen Grund
um 3 mm nach allen Seiten vergrößern.

## Berichtsdeckblatt

Das Stanzfenster gibt den Titelblock des Word-Deckblatts aus
`02-Vorlagen-Dokumente` frei: Lage 40 / 134 mm, Größe 130 × 82 mm, untere rechte Ecke
auf 16 mm gefast — dieselbe Schräge wie in der Bildmarke. Die Stanzkontur liegt als
magentafarbene Strichlinie in der Datei und ist für die Druckerei als Stanzform
anzulegen; sie druckt nicht mit. Empfehlung: 250 g/m² Karton.

## Aufkleber

| Vorlage | Etikett | passende Artikel |
|---|---|---|
| `aufkleber-kuvert-gross-A4` | 99,1 × 67,7 mm, 2 × 4 | Avery Zweckform L7165, Herma 4458 |
| `aufkleber-absender-klein-A4` | 63,5 × 38,1 mm, 3 × 7 | Avery Zweckform L7160, Herma 4625 |

Beim Drucken aus dem PDF **„Tatsächliche Größe“** einstellen, nicht „An Seite
anpassen“. Vor der ersten Charge einen Probedruck auf Normalpapier machen und gegen
einen Etikettenbogen halten.

## Farben

| Farbe | Hex | CMYK |
|---|---|---|
| HakaGold | `#D9A441` | 14 / 36 / 85 / 0 |
| HakaGrey | `#8B7D85` | 45 / 45 / 34 / 17 |
| HakaBerry | `#9B1E52` | 28 / 100 / 36 / 23 |
| HakaDark | `#5A1230` | 40 / 100 / 41 / 60 |
| Tinte | `#211E19` | — |
| Icon als Flächenmotiv | `#EFECEE` | HakaGrey mit rund 14 % Tonwert |
