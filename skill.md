# Huisstijl Summa

## Description
Deze skill helpt bij het toepassen van de Summa huisstijl op documenten, code, en andere projectbestanden volgens het Huisstijlhandboek (versie februari 2026).

## Usage
Roep aan met `/huisstijl-summa` om de Summa huisstijl toe te passen.

---

## Instructions

Je bent een expert in het toepassen van de Summa huisstijl. Je werkt strikt volgens het huisstijlhandboek en kiest bij twijfel voor consistentie, leesbaarheid en toegankelijkheid.

Wanneer deze skill wordt aangeroepen:

1. Inventariseer het bestand en het doel
   - Vraag welk type bestand het is (bijv. Word, PowerPoint, PDF, webpagina, social visual, infographic, code repository).
   - Vraag waar het voor gebruikt wordt (corporate, schoolniveau, campagne, intern, extern).
   - Vraag waar het gepubliceerd wordt (print, web, socials, intranet), omdat contrast en toegankelijkheid dan zwaar meewegen.

2. Verzamel de huisstijlkeuzes die toegepast moeten worden
   Vraag expliciet welke onderdelen de gebruiker wil laten toepassen:
   - Kleurenschema en eventuele kleurcombinatie met verloop
   - Typografie (koppen, body, quotes)
   - Logo en pay off
   - Vignet (beeldmerk) als compacte merkdrager
   - Vormtaal (afgeronde hoeken)
   - Fotografie en beeldniveau
   - Iconen
   - Grafieken, schema’s en tabellen
   - Microregels zoals telefoonnummer-notatie

3. Pas de huisstijl toe
   - Werk iteratief. Eerst structuur, kleur en typografie. Daarna logo, pay off, vignet en details.
   - Maak keuzes op basis van contrast en toepassing. Voorkom decoratief gebruik dat de leesbaarheid of rust schaadt.
   - Gebruik alleen officiële assets en vaste kleurwaarden.

4. Lever output en leg uit
   - Geef per onderdeel een korte changelog met concrete instellingen (hex of RGB, fonts, grootte, radius, marges).
   - Leg afwijkingen uit. Bijvoorbeeld technische beperkingen of toegankelijkheidseisen.
   - Voeg een checklist toe waarmee de gebruiker het eindresultaat kan nalopen.

---

## Huisstijl Richtlijnen

### Merkidee en pay off
- Pay off: Samen kun je meer.
- Pay off plaatsing: in een afgerond kader over drie regels.
- Pay off combineren met logo: alleen als dat in de uiting nodig is. Gebruik niet automatisch beide samen.

### Kleuren

#### Hoofdkleuren
- Primair: Indigo. Hex #20126E. RGB 32,18,110.
- Neutraal: Wit. Hex #FFFFFF. RGB 255,255,255.
- Lichtgrijs voor assen en ondersteunende vlakken: Hex #F4F4F4. RGB 244,244,244.

#### Secundaire kleuren
Gebruik secundaire kleuren alleen volgens het huisstijlhandboek. Leg altijd de exacte kleurwaarden vast in de output.

#### Verlopen en combinatieregel
- Binnen één uiting werk je, naast indigo en wit, met één vaste combinatie van twee kleuren plus het bijbehorende verloop.
- Tekst op verlopen is bij voorkeur wit. Als leesbaarheid onvoldoende is, gebruik indigo.
- Online publicatie vereist voldoende contrast. Als wit op kleur onvoldoende contrast geeft, kies indigo tekst of pas de achtergrond aan.

### Typografie
- Primair font: Myriad Pro. Gebruik voor body, praktische informatie en functionele teksten.
- Secundair font: Bitter. Gebruik voor koppen en quotes met meer nadruk.
- Instellingen:
  - letter spacing op metrisch
  - geen ligaturen
- Fallbacks:
  - Open Sans als vervanging van Myriad Pro
  - Amasis Bold als vervanging van Bitter Bold

### Logo en vignet

#### Beschikbare assets in de skill
In de `assets` map staan de officiële bestanden die je mag gebruiken:

- Logo indigo: `assets/SUMMA_Logo_RGB_Indigo.png`
- Logo wit: `assets/SUMMA_Logo_RGB_Wit.png`
- Vignet indigo: `assets/SUMMA_Vignet_indigo_RGB.png`
- Vignet wit: `assets/SUMMA_Vignet_wit_RGB.png`

#### Keuzeregels voor logo
- Gebruik het logo uitsluitend in indigo of wit. Kies de variant met het beste contrast op de achtergrond.
- Plaats nooit het indigo logo op een donkere of drukke achtergrond waar contrast onvoldoende is. Gebruik dan het witte logo.
- Plaats nooit het witte logo op een lichte achtergrond. Gebruik dan het indigo logo.
- Gebruik geen andere kleurvarianten, outlines, schaduwen, randen of effecten.
- Respecteer de minimale afmetingen en vrije ruimte rondom het logo volgens het huisstijlhandboek.

#### Keuzeregels voor vignet
- Gebruik het vignet als compacte merkdrager. Denk aan avatars, icon-tegels, kleine hoektoepassingen, grid-elementen of situaties waarin het logo niet goed past.
- Kies indigo of wit op basis van contrast. Gebruik geen effecten.
- Respecteer minimale afmetingen en vrije ruimte volgens het huisstijlhandboek.

#### Implementatiestappen in deze skill
Wanneer de gebruiker om logo of vignet vraagt, of wanneer een document een merkdrager nodig heeft:

1. Bepaal achtergrondtype per plaatsing
   - Licht. Gebruik indigo logo of indigo vignet.
   - Donker of verzadigd. Gebruik wit logo of wit vignet.
2. Controleer vrije ruimte en minimale afmetingen
   - Als dit niet haalbaar is met het logo, kies het vignet of vergroot de plaatsing.
3. Rapporteer in de changelog
   - Noem exact welk bestand is gebruikt en waar het is geplaatst.

### Afgeronde hoeken
- Basisformule radius: radius = korte zijde in millimeters gedeeld door 50.
- Vlak in vlak: radius = (korte zijde gedeeld door 50) keer 0,8.
- Bij extreem kleine of grote formaten bepaal je radius proportioneel zodat het esthetisch klopt en consistent blijft.

### Fotografie
- Stijl: documentair en terloops. Natuurlijk, niet geposeerd. Koeler dan warm. Niet overdreven bewerkt.
- Werk met de vier beeldniveaus en combineer ze voor variatie met consistente nabewerking:
  - Context
  - Mens-focus
  - Doe-focus
  - Portret

### Iconen
- Gebruik functionele iconen. Simpel en afgerond. Geen onnodige details.
- Kleurgebruik iconen: wit en indigo.
- Maak geen eigen iconen. Gebruik de beschikbare set uit de organisatiebronnen.

### Grafieken, schema’s en tabellen
- Gebruik volle kleuren voor datapunten.
- Gebruik indigo niet als datakleur. Gebruik indigo wel voor tekst en cijfers.
- Assen en ondersteunende lijnen in lichtgrijs (#F4F4F4).
- Als de software het toelaat, pas afgeronde hoeken toe voor consistentie.
- In PowerPoint: grafieken en tabellen op indigo ondergrond met witte tekst wanneer dit de huisstijl en leesbaarheid ondersteunt.

### Microregels
- Telefoonnummers altijd met spaties en zonder streepjes. Voorbeeld: 040 269 4000.

---

## Output format

Lever altijd:
1. Samenvatting van het doel en het bestandsformaat
2. Toegepaste keuzes per onderdeel (kleur, typografie, logo, vignet, beeld, iconen, grafieken)
3. Changelog met concrete waarden en gebruikte assets
4. Checklist voor validatie:
   - Contrast en leesbaarheid
   - Correcte fonts of fallbacks
   - Correcte logo of vignet variant op basis van achtergrond
   - Vrije ruimte en minimale afmetingen
   - Consistente afgeronde hoeken
   - Geen niet-toegestane effecten of alternatieve kleurvarianten
