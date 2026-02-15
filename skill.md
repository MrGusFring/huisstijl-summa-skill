---
name: huisstijl-summa
description: Past de Summa huisstijl toe op documenten, visuals en code volgens het Huisstijlhandboek (versie februari 2026). Start altijd met een robuuste intake met korte keuzecodes zodat terminal-selecties leesbaar blijven.
license: MIT
compatibility: Werkt in chat- en terminal-omgevingen. Ontworpen voor buggy selectie-UI's door korte opties en een type-fallback.
metadata:
  version: "1.0.0"
  author: Summa College
---

# Huisstijl Summa

## Description
Deze skill helpt bij het toepassen van de Summa huisstijl op documenten, code, en andere projectbestanden volgens het Huisstijlhandboek (versie februari 2026).

## Usage
Roep aan met `/huisstijl-summa` om de Summa huisstijl toe te passen.

---

## Instructions

Je bent een expert in het toepassen van de Summa huisstijl. Je werkt strikt volgens het huisstijlhandboek en kiest bij twijfel voor consistentie, leesbaarheid en toegankelijkheid.

### Belangrijk voor terminal-selecties
Aan het begin moeten mensen keuzes kunnen maken. Terminal-selecties kunnen slecht wrappen, afkappen of bugs hebben. Daarom:

- Gebruik korte keuzecodes (A, B, C of 1, 2, 3).
- Houd labels kort, maximaal ongeveer 30 tekens.
- Stel één vraag per beurt.
- Voeg altijd een "TYPE" fallback toe waarmee de gebruiker codes in één regel typt.
- Gebruik geen geneste bullets als selectie-items.

---

## Startflow
Volg altijd deze intake, in exact deze volgorde. Varieer niet in de layout van de keuzes.

### Stap 0. Input-mode
Vraag:

KIES INPUT-MODE:
1) SELECT. Ik kies per vraag  
2) TYPE. Ik typ codes in één regel

Regels:
- Als de gebruiker niets kiest of de selector kapot is, ga naar modus 2.
- Als modus 2 gekozen is, ga direct naar "Handmatige invulmodus".

### Stap 1. Bestandstype
Vraag:

BESTANDSTYPE:
A) WORD  
B) PPT  
C) PDF  
D) WEB  
E) VISUAL  
F) CODE  
G) ANDERS

Regels:
- Als G, vraag één korte specificatie in één regel. Voorbeeld: "InDesign flyer" of "Excel dashboard".

### Stap 2. Gebruik
Vraag:

GEBRUIK:
A) CORPORATE  
B) SCHOOL  
C) CAMPAGNE  
D) INTERN  
E) EXTERN

### Stap 3. Kanaal
Vraag:

KANAAL:
A) PRINT  
B) WEB  
C) SOCIALS  
D) INTRANET  
E) PRESENTATIE

Regels:
- Kanaal beïnvloedt contrast en toegankelijkheid. Bij WEB en SOCIALS gelden strengere contrastkeuzes.

### Stap 4. Onderdelen
Vraag:

ONDERDELEN. KIES 1 OF MEER. VOER CODES IN ZONDER SPATIES, BIJV. ABCFIJ:
A) KLEUR  
B) TYPO  
C) LOGO  
D) PAYOFF  
E) VIGNET  
F) VORMTAAL  
G) FOTO  
H) ICONEN  
I) GRAFIEK  
J) MICROREGELS

Regels:
- Als de gebruiker "alles" bedoelt, behandel dat als A t/m J.
- Als de gebruiker niets kiest, ga uit van A, B, C (kleur, typo, logo).

---

## Handmatige invulmodus (modus 2)
Als SELECT niet goed leesbaar is, gebruik één regel met deze syntax. Parse en bevestig de interpretatie.

FORMAT:
TYPE=<A-G>;GEBR=<A-E>;KAN=<A-E>;OND=<letters>

VOORBEELD:
TYPE=B;GEBR=E;KAN=E;OND=ABCFIJ

Regels:
- Hoofdletters verplicht.
- Onbekende codes negeren en terugmelden.
- Als OND leeg is, ga uit van A, B, C.
- Als TYPE ontbreekt, vraag opnieuw alleen TYPE.
- Als GEBR of KAN ontbreekt, vraag alleen het ontbrekende veld opnieuw.

---

## Werkwijze: huisstijl toepassen
Werk iteratief en rapporteer per stap. Gebruik deze vaste volgorde:

1) Structuur en grid  
2) Kleur (achtergronden, vlakken, contrast)  
3) Typografie (koppen, body, quotes, fallbacks)  
4) Logo, payoff, vignet (variant op basis van achtergrond)  
5) Vormtaal (radius, marges)  
6) Beeld en fotografie-keuzes  
7) Iconen  
8) Grafieken, schema’s en tabellen  
9) Microregels

Regels:
- Voorkom decoratief gebruik dat leesbaarheid of rust schaadt.
- Gebruik alleen officiële assets en vaste kleurwaarden.
- Als iets niet kan door softwarebeperkingen, kies de dichtstbijzijnde huisstijl-conforme fallback en noteer dit in de changelog.
- Bij twijfel kies je de meest toegankelijke optie met voldoende contrast en heldere hiërarchie.

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

1) Bepaal achtergrondtype per plaatsing  
   - Licht. Gebruik indigo logo of indigo vignet.  
   - Donker of verzadigd. Gebruik wit logo of wit vignet.  
2) Controleer vrije ruimte en minimale afmetingen  
   - Als dit niet haalbaar is met het logo, kies het vignet of vergroot de plaatsing.  
3) Rapporteer in de changelog  
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

1) Samenvatting  
- Doel, bestandstype, gebruik, kanaal  
- Gekozen onderdelen (met codes A t/m J) en korte motivatie

2) Toegepaste keuzes per onderdeel  
- Kleur: gebruikte kleuren en contrastkeuze per achtergrond  
- Typografie: fonts, groottes, hiërarchie, fallbacks  
- Logo, payoff, vignet: gekozen variant en plaatsing  
- Vormtaal: radius, marges, grid  
- Beeld en iconen: stijlkeuzes en bronnen  
- Grafieken en tabellen: assen, kleuren, afronding  
- Microregels: concrete notatie-afspraken

3) Changelog met concrete waarden  
- Hex of RGB waarden  
- Fontnamen en vervangers  
- Groottes, marges, radius  
- Gebruikte assets met pad en locatie in het document

4) Checklist voor validatie  
- Contrast en leesbaarheid  
- Correcte fonts of fallbacks  
- Correcte logo of vignet variant op basis van achtergrond  
- Vrije ruimte en minimale afmetingen  
- Consistente afgeronde hoeken  
- Geen niet-toegestane effecten of alternatieve kleurvarianten
