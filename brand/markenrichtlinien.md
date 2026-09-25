# haka tax – Markenzeichen und Farbsystem

Finale, vom Grafikdesigner freigegebene Fassung. Sie ersetzt alle vorherigen
Logo-Entwürfe (unter anderem das frühere 2×2-Signet aus gerundeten Blöcken)
vollständig. Die Masterdateien liegen neben diesem Dokument in `brand/`.

---

## 1. Das Icon

Vier Pfeile, die zur Mitte zeigen — eine feste Vektorform, kein Farbverlauf.
Lesart: vier Partner, die auf einen gemeinsamen Punkt ausgerichtet sind.

Ein Viertel, lokal 0..100 (Ecke außen = (0,0), Ecke innen/Mitte = (100,100));
die anderen drei Viertel sind exakt diese Form, gespiegelt:

```svg
<path d="M0 0 L25 0 L75 50 L75 0 L100 0 L100 100 L0 100 L0 75 L50 75 L0 25 Z"/>
```

Vollständiges Icon (viewBox `0 0 220 220`):

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 220 220">
  <path d="M0 0 L25 0 L75 50 L75 0 L100 0 L100 100 L0 100 L0 75 L50 75 L0 25 Z" fill="#D9A441"/>
  <path d="M0 0 L25 0 L75 50 L75 0 L100 0 L100 100 L0 100 L0 75 L50 75 L0 25 Z" fill="#8B7D85" transform="translate(220 0) scale(-1 1)"/>
  <path d="M0 0 L25 0 L75 50 L75 0 L100 0 L100 100 L0 100 L0 75 L50 75 L0 25 Z" fill="#9B1E52" transform="translate(0 220) scale(1 -1)"/>
  <path d="M0 0 L25 0 L75 50 L75 0 L100 0 L100 100 L0 100 L0 75 L50 75 L0 25 Z" fill="#5A1230" transform="translate(220 220) scale(-1 -1)"/>
</svg>
```

Feste Regeln:

- Reihenfolge/Position der vier Farben nie vertauschen: oben links Gold, oben
  rechts Grau, unten links Beere, unten rechts Dunkel.
- Die Fuge in der Mitte bleibt proportional erhalten — nie auf 0 setzen (die
  Form würde kollabieren), nie größer skalieren als hier vorgegeben.
- Form nicht verzerren, **nicht drehen**, keine Schatten/Verläufe/Konturen.
- **Mindestgröße:** 16 px als Favicon, 8 mm im Druck.
- **Dunkler Grund** (Footer, Dark Mode, dunkle Folien): die aufgehellte Fassung
  `icon-farbig-dunkel.svg` verwenden, nie die helle Fassung auf Dunkel legen.
- **Graustufen:** `icon-graustufen.svg` / `icon-graustufen-dunkel.svg`.
  **Schwarz/Weiß** (Stempel, Fax, Einfarbdruck): `icon-schwarz.svg` auf hellem,
  `icon-weiss.svg` auf dunklem Grund.

## 2. Farbsystem

| Name / Token | Hex | CMYK | Rolle im Icon |
|---|---|---|---|
| HakaGold `--gold` | `#D9A441` | 14/36/85/0 | oben links |
| HakaGrey `--graualt` | `#8B7D85` | 45/45/34/17 | oben rechts |
| HakaBerry `--himbeere` | `#9B1E52` | 28/100/36/23 | unten links |
| HakaDark `--wein` | `#5A1230` | 40/100/41/60 | unten rechts |

Auf dunklem Grund bleibt HakaGold bei 100 %, die anderen drei werden 50 %
Richtung Weiß aufgehellt:

| Name | Hex (dunkler Grund) |
|---|---|
| HakaGold | `#D9A441` (unverändert) |
| HakaGrey | `#C5BEC2` |
| HakaBerry | `#CD8EA8` |
| HakaDark | `#AC8897` |

Rollen in der Anwendung: **HakaBerry ist die Hauptfarbe** (Primär-Buttons,
Links, Überschriften-Akzent), HakaGold bleibt Akzent-/Highlight-Farbe,
HakaDark ist Zweitfarbe (Hover/Aktiv, dunkle Flächen, Footer), HakaGrey trägt
ruhige Sekundärflächen, Linien und Meta-Text.

Weitere Tokens der Website: `--tinte` `#211E19` hell / `#F0ECE1` dunkel
(Fließtext), `--papier` `#FFFFFF` / `#1B1714` (Seitengrund), `--papier-2`
`#F2EFE7` / `#272219` (Sektionen, Karten, Formularfelder).

Abgrenzung: Die Hauptfarbe ist bewusst **kein** Telekom-Magenta (`#E20074`) und
**kein** Blauviolett wie bei Grant Thornton (`#4F2D7F`). Kein reines Magenta,
kein Neon, kein Blauviolett irgendwo im Auftritt einführen.

Kontrast: HakaBerry `#9B1E52` auf Weiß erfüllt WCAG AA für Text (7,8:1); Gold
`#D9A441` auf Weiß **nicht** – Gold daher nie als Textfarbe auf hellem Grund,
nur als Fläche, Linie oder Icon. Auf dunklem Grund gilt umgekehrt: Text in
Creme, Akzente in den aufgehellten Werten (HakaBerry dunkel: 6,8:1).
HakaGrey `#8B7D85` erreicht als kleiner Text auf Weiß nur 3,9:1 — für Meta-Text
nutzt die Website deshalb die abgedunkelte Variante `--text-muted` `#71656C`,
während `#8B7D85` unverändert für Linien, Flächen und das Icon gilt.

## 3. Wortmarke und Kombination

**Genau zwei zulässige Erscheinungsformen — keine dritte Variante:**

1. **Nur das Icon**, ohne Text und ohne Trennstrich. Für Favicon, App-Icon,
   Profilbild und als alleinstehende Bildmarke, wenn der Markenname bereits
   anderswo steht.
2. **Icon + Trennstrich + „haka-tax"**, in dieser festen Reihenfolge:
   `Icon | haka-tax`. Überall, wo Icon und Firmenname gemeinsam auftreten —
   Header, Footer, Briefkopf, Signatur, Deckblätter.

Es gibt **keine** Variante „Icon + Text ohne Trennstrich" und **keinen** Zusatz
wie „Steuerberatung" innerhalb des Zeichens.

**Kritische Maßregel:** Die Höhe des Icons entspricht **exakt** der Höhe des
kleinen „h" in „haka-tax" (Oberlänge bis Grundlinie). Icon-Unterkante =
Grundlinie des Textes.

Weitere Maße, proportional zur Icon-Höhe H:

- Abstand Icon → Trennstrich: 0,216 × H
- Trennstrich: Breite 0,034 × H, Höhe = H
- Abstand Trennstrich → Text: 0,216 × H
- Schrift: **Inter, Regular (400)** — kein Fett, keine Kursive, Laufweite
  −0,01 em. In Inter entspricht die h-Höhe 0,7234 em, der Schriftgrad ergibt
  sich also als H ÷ 0,7234.
- Textfarbe: `#211E19` auf hellem, `#F0ECE1` auf dunklem Grund.

Fertige Lockups: `lockup-hell.svg` und `lockup-dunkel.svg`.

## 4. Umsetzung auf der Website (Repository haka-tax.de)

Umgesetzter Stand:

- `favicon.svg` = `brand/favicon.svg` (Icon auf weißer gerundeter Kachel); der
  identische Inhalt liegt als inline `data:image/svg+xml` in allen 16 Seiten
  (8 DE + 8 EN). `apple-touch-icon.png`, `icon-192.png` und `icon-512.png`
  stammen aus den PNG-Exporten des Designers.
- Header und Footer tragen die Kombi-Form `Icon | haka-tax` (Regel 3.2). Die
  Wortmarke bleibt Live-Text in Inter Regular; Maße und Abstände leiten sich in
  `styles.css` proportional aus `--lockup-h` ab (siehe Abschnitt „Marken-Lockup").
- Das Header-Icon füllt seine vier Viertel aus den Marken-Tokens und wechselt
  damit im Dunkelmodus automatisch auf die aufgehellte Fassung. Das Footer-Icon
  liegt in beiden Themes fest auf der Weinfläche und nutzt feste dunkle Werte.
- `og-image.png` (1200 × 630) zeigt die Kombi-Form auf `#F2EFE7`.

## 5. Geschäftsausstattung

- **Briefbogen (DIN A4):** Icon oben links, 12 mm hoch, 20 mm vom linken und
  oberen Rand; Wortmarke nach Regel 3 rechts daneben. Absender-/Fußzeile in
  `--tinte`, Trennlinie in HakaGrey, Folgeseiten nur Icon 8 mm.
- **Visitenkarte (85 × 55 mm):** Vorderseite weiß, Lockup links oben; Rückseite
  HakaDark `#5A1230` vollflächig mit dem Icon in der dunklen Fassung, mittig, 22 mm.
- **E-Mail-Signatur:** Icon 48 px, daneben Name/Funktion in `--tinte`,
  Kontaktzeile in HakaGrey, Link in HakaBerry.
- **Präsentation:** Titelfolie Grund `#F2EFE7` mit Lockup; Inhaltsfolien Icon
  10 mm rechts unten; Diagramme in Beere/Dunkel/Gold/Grau.
- **Social-Profile:** Profilbild = Icon auf weißer Kachel (512 px).
- **Stempel/Prägung:** einfarbige Fassung, Icon ≥ 8 mm.

## 6. Dateien in diesem Ordner

```
icon-farbig.svg              Master, heller Grund, transparent
icon-farbig-dunkel.svg       aufgehellte Fassung für dunklen Grund
icon-graustufen.svg          Graustufen, heller Grund
icon-graustufen-dunkel.svg   Graustufen, dunkler Grund
icon-schwarz.svg             Schwarz, für hellen Grund
icon-weiss.svg               Weiß, für dunklen Grund
favicon.svg                  Icon auf weißer gerundeter Kachel
lockup-hell.svg              Icon | haka-tax, helle Fassung
lockup-dunkel.svg            Icon | haka-tax, dunkle Fassung
```

Vor der endgültigen Veröffentlichung: formale Markenrecherche (DPMA/EUIPO) auf
die Bildmarke.
