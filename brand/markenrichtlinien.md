# Markenumstellung haka tax – neues Signet und neue Farben

Dieser Text ist die vollständige Vorgabe für alle Anpassungen (Website, Markenrichtlinien,
Briefpapier, Vorlagen, digitale Profile). Er ist so geschrieben, dass er ohne weitere
Rückfragen an einen Webentwickler, eine Grafikerin oder ein KI-Werkzeug übergeben werden kann.
Die zugehörigen Logodateien liegen im Ordner `haka-tax-logo/` (SVG-Master in `svg/`,
Rasterexporte in `png/`).

---

## 1. Das Signet

Vier gerundete Blöcke im 2×2-Raster. Jeder Block ist an seiner **äußeren** Ecke gerundet;
die vier **inneren** Ecken sind gefast, sodass die Fuge in der Mitte eine kleine Raute bildet.
Lesart: vier Partner, die auf einen gemeinsamen Punkt ausgerichtet sind.

Vektorquelle (Raster 120 × 120, Blöcke 34 × 34, Fuge 4, Außenradius 8, Fase 10):

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 120 120">
  <path d="M32 24 L58 24 L58 48 L48 58 L24 58 L24 32 A8 8 0 0 1 32 24 Z" fill="#D9A441"/>
  <path d="M62 24 L88 24 A8 8 0 0 1 96 32 L96 58 L72 58 L62 48 Z"         fill="#8B7D85"/>
  <path d="M24 62 L48 62 L58 72 L58 96 L32 96 A8 8 0 0 1 24 88 Z"         fill="#9B1E52"/>
  <path d="M72 62 L96 62 L96 88 A8 8 0 0 1 88 96 L62 96 L62 72 Z"         fill="#5A1230"/>
</svg>
```

Farbzuordnung (fest, nie vertauschen):

| Block          | Rolle       | Heller Grund | Dunkler Grund |
|----------------|-------------|--------------|---------------|
| oben links     | Gold        | `#D9A441`    | `#E3B35A`     |
| oben rechts    | Warmgrau    | `#8B7D85`    | `#A79AA3`     |
| unten links    | Himbeere    | `#9B1E52`    | `#C43A72`     |
| unten rechts   | Wein        | `#5A1230`    | `#8E2A55`     |

Regeln:
- Der Rand des 120er-Rasters (24 Einheiten um die Blöcke) ist der **Schutzraum**. Innerhalb
  dieses Raums steht nichts anderes. Bei Skalierung: Schutzraum = ein Drittel der Blockbreite.
- Die Form wird nicht gedreht, gespiegelt, verzerrt, mit Verlauf, Schatten oder Kontur versehen.
- Die Fuge und die Rautenmitte bleiben immer frei (Hintergrundfarbe).
- **Mindestgröße:** 16 px als Favicon, 8 mm im Druck.
- **Dunkler Grund** (Footer, Dark Mode, dunkle Präsentationsfolien): die aufgehellte Fassung
  verwenden (`haka-tax-signet-dunkler-grund.svg`), nie die helle Fassung auf Dunkel legen.
- **Einfarbig** (Stempel, Prägung, Fax, Schwarz-Weiß-Druck): alle vier Blöcke in Schwarz
  (`#211E19`) bzw. auf Dunkel in Creme (`#F0ECE1`). Datei `haka-tax-signet-einfarbig*.svg`.

## 2. Farbsystem

| Token           | Hell (Grund weiß/creme) | Dunkel (Grund `#1B1714`) | Verwendung |
|-----------------|-------------------------|--------------------------|-----------|
| `--gold`        | `#D9A441` | `#E3B35A` | Akzent: Hervorhebungen, aktive Zustände, Icons, Badges |
| `--graualt`     | `#8B7D85` | `#A79AA3` | ruhige Sekundärflächen, Linien, Meta-Text |
| `--himbeere`    | `#9B1E52` | `#C43A72` | **Hauptfarbe**: Primär-Buttons, Links, Überschriften-Akzent |
| `--wein`        | `#5A1230` | `#8E2A55` | Zweitfarbe: Hover/Aktiv von Himbeere, dunkle Flächen, Footer |
| `--tinte`       | `#211E19` | `#F0ECE1` | Fließtext / Text auf Dunkel |
| `--papier`      | `#FFFFFF` | `#1B1714` | Seitenhintergrund |
| `--papier-2`    | `#F2EFE7` | `#272219` | Sektionen, Karten, Formularfelder |

Hinweise zur Abgrenzung: Die Hauptfarbe ist bewusst **kein** Telekom-Magenta (`#E20074`) und
**kein** Blauviolett wie bei Grant Thornton (`#4F2D7F`). Kein reines Magenta, kein Neon, kein
Blauviolett irgendwo im Auftritt einführen. Gold ist Akzent, nie Fläche für Fließtext.

Kontrast: Himbeere `#9B1E52` auf Weiß erfüllt WCAG AA für Text; Gold `#D9A441` auf Weiß
**nicht** – Gold daher nie als Textfarbe auf hellem Grund, nur als Fläche, Linie oder Icon.
Auf dunklem Grund gilt umgekehrt: Text in Creme, Akzente in den aufgehellten Werten.

## 3. Wortmarke und Kombination

- Die Wortmarke lautet ausschließlich **„haka tax“** (Kleinschreibung, Leerzeichen; alternativ
  „haka-tax“ oder „haka.tax“, wenn technisch nötig). Kein Zusatz „Steuerberatung“ im Logo.
- Schrift: die Headline-Schrift der Website (derzeit Inter), Schnitt SemiBold (600), leicht
  negativ gesperrt (−0,01 em). Farbe: `--tinte`. Datei `haka-tax-wortmarke.svg` enthält den
  Text als Textobjekt; für Druck von der Grafikerin in Pfade wandeln.
- Anordnung: **Signet immer links, Wortmarke rechts**, beide auf gemeinsamer Mittelachse.
  Abstand Signet → Wortmarke: 0,3 × Signethöhe. Versalhöhe der Wortmarke ≈ 0,55 × Signethöhe.
- Nie: Signet zwischen den Wörtern, Signet rechts, Wortmarke über/unter dem Signet (Ausnahme:
  zentrierte Anwendung auf Deckblättern, dort Signet oben, Wortmarke darunter, mittig).

## 4. Website (Repository haka-tax.de)

Nur Logo, Favicon und Farbsystem ändern. Layout, Typografie, Inhalte und Struktur bleiben.

1. `favicon.svg` durch `svg/haka-tax-favicon.svg` ersetzen (weiße gerundete Kachel, Radius 26,
   mit dem Signet). Die inline `data:image/svg+xml`-Favicons auf allen 16 Seiten (8 DE + 8 EN)
   durch denselben Inhalt ersetzen. Zusätzlich `png/favicon/favicon-180.png` als
   `apple-touch-icon` und `favicon-192.png`/`favicon-512.png` fürs Web-App-Manifest einbinden.
2. Header- und Footer-Logo auf allen 16 Seiten: die vier `<path>`-Elemente aus Abschnitt 1
   übernehmen. Im Header (heller Grund) die hellen Werte, im Footer (dunkler Grund) die
   dunklen Werte. Die Wortmarke bleibt Live-Text „haka tax“ in der bestehenden Schrift; falls
   dort noch „haka-tax“ steht, so lassen (Schreibweise ist frei).
3. `styles.css`: die bisherigen Marken-Tokens (`--raspberry`, `--violet`, `--honey`, `--mauve`)
   entfernen und durch die Tokens aus Abschnitt 2 ersetzen. Jede Stelle mitziehen, die die
   alten Tokens referenziert: Buttons (`.cta-btn`, `.accent`, `.ghost`), Hero-Verlauf,
   Links, Hover/Active/Focus, Badges/Tags, Footer, `.lang-notice`, Formular-Fokusringe.
   Zuordnung: Violett → Wein, Himbeerrot → Himbeere (neuer Wert), Honig → Gold, Mauve → Warmgrau.
   Dark-Mode-Block entsprechend mit den dunklen Werten.
4. `og-image.png` mit dem neuen Signet neu erzeugen (1200 × 630, Signet links, Wortmarke rechts,
   Grund `#F2EFE7`).
5. Prüfen: Kontrast AA für Text in beiden Themes, Screenshots von Header, Footer, Hero, einem
   Button-Zustand und Favicon in Hell und Dunkel, je eine DE- und eine EN-Seite.

## 5. Markenrichtlinien (Dokument, 8–10 Seiten)

Aufbau: 1 Signet und Herleitung · 2 Schutzraum, Mindestgrößen, Varianten (Farbe, dunkler
Grund, einfarbig) · 3 Fehlanwendungen (drehen, verzerren, Verlauf, Kontur, Farben tauschen,
Signet zwischen Text) · 4 Wortmarke und Kombination · 5 Farbsystem mit Hex/RGB/CMYK/Pantone-
Näherung (CMYK und Pantone von der Grafikerin bestimmen; Bildschirmwerte oben sind verbindlich)
· 6 Typografie (Website-Schrift, Schnitte, Größenstaffel) · 7 Anwendungen (Briefpapier,
Visitenkarte, E-Mail-Signatur, Präsentation, Social) · 8 Dateiübersicht.

## 6. Geschäftsausstattung

- **Briefbogen (DIN A4):** Signet oben links, 12 mm hoch, 20 mm vom linken und oberen Rand;
  Wortmarke rechts daneben nach Regel 3. Absender-/Fußzeile in `--tinte`, Trennlinie in
  `--graualt`, Seitenzahl/Folgeseiten nur Signet 8 mm. Keine Farbflächen im Brieftext.
- **Visitenkarte (85 × 55 mm):** Vorderseite weiß, Signet + Wortmarke links oben; Rückseite
  Wein `#5A1230` vollflächig mit Signet in der dunklen Fassung, mittig, 22 mm.
- **E-Mail-Signatur:** Signet 48 px (PNG `favicon-transparent-64.png` auf 48 px skaliert),
  daneben Name/Funktion in `--tinte`, Kontaktzeile in `--graualt`, Link in `--himbeere`.
- **Präsentation (Word/PowerPoint):** Titelfolie Grund `#F2EFE7`, Signet + Wortmarke; Inhaltsfolien
  Signet 10 mm rechts unten; Akzentfarbe Gold für Marker, Himbeere für Überschriften-Akzent,
  Diagramme in Himbeere/Wein/Gold/Warmgrau.
- **Social-Profile:** Profilbild = `png/favicon/favicon-512.png` (Signet auf weißer Kachel);
  Titelbild Grund `#F2EFE7` mit Signet + Wortmarke mittig.
- **Stempel/Prägung:** einfarbige Fassung, Signet ≥ 8 mm.

## 7. Dateien

```
svg/haka-tax-signet.svg                    Master, heller Grund, transparent, Schutzraum enthalten
svg/haka-tax-signet-dunkler-grund.svg      aufgehellte Fassung für dunklen Grund
svg/haka-tax-signet-einfarbig.svg          Schwarz
svg/haka-tax-signet-einfarbig-weiss.svg    Creme, für dunklen Grund einfarbig
svg/haka-tax-favicon.svg                   Signet auf weißer gerundeter Kachel
svg/haka-tax-wortmarke.svg                 Signet + „haka tax“ (Text als Textobjekt)
svg/haka-tax-wortmarke-dunkler-grund.svg
png/signet/…                               256 / 512 / 1024 / 2048 px, transparent; plus auf Weiß/Dunkel
png/favicon/…                              16 / 32 / 48 / 64 / 128 / 180 / 192 / 512 px
png/wortmarke/…                            3000 px breit, transparent und auf Grund
png/einfarbig/…                            512 / 2048 px, Schwarz und Creme
```

Vor der endgültigen Freigabe: formale Markenrecherche (DPMA/EUIPO) auf die Bildmarke.
