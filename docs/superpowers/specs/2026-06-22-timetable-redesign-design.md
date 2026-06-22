# ELF Timetable Redesign — "Festivalplakat"
*2026-06-22*

## Ziel

Komplettes Redesign der Electric Love Festival 2026 Timetable-Webseite. Die aktuelle Version wirkt generisch. Ziel: professionell, unverwechselbar, zum Festival passend — hell, mutig, klar.

## Design-Richtung: Festivalplakat

Die Bühnenfarben sind die einzigen Farben auf der Seite. Alles andere ist schwarz oder weiß. Dadurch wirken die Stage-Header-Blöcke und Card-Akzente viel stärker.

## Typografie

- **Display:** Bebas Neue — Tagesnamen (108px), große Labels
- **UI/Body:** Inter — Bühnen, Künstler, Zeiten, Navigation
- Tagesnamen in der jeweiligen Tagesfarbe, sehr groß, volle Breite

## Farben

| Rolle | Wert |
|---|---|
| Hintergrund | `#FFFFFF` |
| Navigation | `#0D0D0D` |
| Text primär | `#111111` |
| Text sekundär | `#6B7280` |
| Grid-Linie | `#E8E8E8` |
| Card-Schatten | `0 1px 4px rgba(0,0,0,0.08), 0 0 0 1px rgba(0,0,0,0.04)` |

Bühnenfarben unverändert: Mainstage `#D62839`, Heineken `#007A40`, Circus `#E07B00`, BlueBoXX `#0050CC`, Shutdown `#7A00BB`, Hard Dance Valley `#CC3600`, Nordic `#007C88`.

## Komponenten

### Navigation
- Sticky, `#0D0D0D`
- Aktiver Tag-Tab: farbig gefüllt (Tagesfarbe), weiß Text, border-radius 8px
- Inaktive Tabs: nur Text, grau, kein Rahmen
- Raster/Liste Toggle rechts

### Tagesheader
- Weißer Hintergrund
- Tagesname: Bebas Neue 108px, Tagesfarbe, linksbündig
- Datum: Inter 14px, `#6B7280`, rechts daneben
- Dünne Akzentlinie unten in Tagesfarbe

### Stage-Header
- Voller Farbblock pro Bühne
- Weißer Text, Inter Bold, 13px, Großbuchstaben
- Keine Rahmen zwischen Spalten (nur Farbe trennt)

### Cards (Desktop/Grid)
- Weißer Hintergrund
- 4px linke Border in Bühnenfarbe
- Artist-Name: Inter Bold 13px, `#111111`
- Zeit: Inter 11px, Bühnenfarbe
- Schatten: wie oben
- border-radius: 8px

### Cards (Mobile < 680px)
- Volle Breite
- Hintergrund: Bühnenfarbe mit 10% Deckkraft (kein linker Streifen)
- Kein Grid, vertikale Liste
- Tagesname bleibt groß

### Listenansicht
- Sortierbar: nach Zeit, nach Bühne
- Jeder Eintrag: farbiger Punkt (Bühnenfarbe), Bühnenname, Künstler, Zeit
- Sauber, minimal, viel Weißraum

### Druckansicht (A4 quer)
- Dediziertes `#print-layout` div
- Pro Tag eine Seite
- Stage-Spalten mit vollem Farbblock-Header
- Kleiner weißer Text in Stage-Headern

## Technische Constraints

- Single HTML file, kein Build-Step
- Google Fonts (Bebas Neue + Inter, bereits im Code)
- GitHub Pages Hosting
- Keine externen Dependencies außer Google Fonts
