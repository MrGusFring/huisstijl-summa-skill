# Huisstijl Summa Skill

Complete Summa huisstijl implementatie met CSS framework, component bibliotheek en demo's volgens het officiële Huisstijlhandboek (versie februari 2026).

## 📦 Installatie

### Via GitHub
```bash
cd ~/.claude/skills
git clone https://github.com/MrGusFring/huisstijl-summa-skill.git huisstijl-summa
```

### Via download
1. Download en pak het archief uit
2. Plaats de `huisstijl-summa` folder in `~/.claude/skills/`
3. Herstart Claude Code

De skill is nu beschikbaar via `/huisstijl-summa`

## 🚀 Gebruik

### Als Claude Code Skill
Roep de skill aan in Claude Code voor interactieve hulp:
```
/huisstijl-summa
```

De skill helpt je met:
- Keuze maken tussen logo en vignet varianten
- Kleuren en contrast bepalen
- Typografie toepassen
- Componenten samenstellen volgens huisstijl
- Toegankelijkheid waarborgen

## 📁 Bestandsstructuur

```
~/.claude/skills/huisstijl-summa/
├── skill.md                    # Skill definitie met volledige huisstijl richtlijnen
├── README.md                   # Deze documentatie
└── assets/                     # Officiële Summa assets
    ├── SUMMA_Logo_RGB_Indigo.png       # Logo voor lichte achtergronden
    ├── SUMMA_Logo_RGB_Wit.png          # Logo voor donkere achtergronden
    ├── SUMMA_Vignet_indigo_RGB.png     # Vignet (compact) voor lichte achtergronden
    └── SUMMA_Vignet_wit_RGB.png        # Vignet (compact) voor donkere achtergronden
```

## 🎨 Wat zit erin?

## 🎨 Belangrijkste Huisstijl Regels

### Kleuren
- **Primair:** Indigo `#20126E`
- **Neutraal:** Wit `#FFFFFF`, Lichtgrijs `#F4F4F4`
- **Online contrast:** Minimaal 4.5:1 voor tekst (WCAG AA)

### Typografie
- **Body:** Myriad Pro (fallback: Open Sans)
- **Koppen:** Bitter Bold (fallback: Georgia)
- **Instellingen:** Letter-spacing metrisch, geen ligaturen

### Logo
- **Lichte achtergrond:** Indigo variant
- **Donkere achtergrond:** Witte variant
- **Geen effecten:** Geen schaduwen, borders, of kleurvarianten

### Afgeronde Hoeken
- **Formule:** `radius = korte zijde / 50`
- **Vlak-in-vlak:** `radius × 0.8`

### Telefoonnummers
- **Format:** `040 269 4000` (met spaties, zonder streepjes)

## 📚 Resources

- **Demo bekijken:** Open `demo.html` in je browser
- **Componenten:** Bekijk `components.html` voor code voorbeelden
- **Snelle referentie:** Check `QUICK_REFERENCE.md`
- **Skill gebruiken:** Roep `/huisstijl-summa` aan in Claude Code

## ✅ Implementatie Checklist

Voordat je live gaat:

- [ ] Alleen officiële kleuren gebruikt (indigo, wit, lichtgrijs)
- [ ] Contrast gecheckt voor online gebruik (min. 4.5:1)
- [ ] Juiste fonts met fallbacks (Myriad Pro, Bitter)
- [ ] Correcte logo variant op basis van achtergrond
- [ ] Afgeronde hoeken volgens formule toegepast
- [ ] Telefoonnummers met spaties (geen streepjes)
- [ ] Alt-teksten voor afbeeldingen
- [ ] Focus states voor toetsenbordnavigatie
- [ ] Responsive design getest op mobiel
- [ ] Prefers-reduced-motion gerespecteerd

## 💡 Tips voor Ontwikkelaars

1. **Begin met de demo:** Open `demo.html` om te zien wat mogelijk is
2. **Kopieer componenten:** Gebruik `components.html` als startpunt
3. **CSS Variabelen:** Gebruik altijd `var(--summa-indigo)` etc. voor consistentie
4. **Logo keuze:** Lichte achtergrond = indigo, donkere achtergrond = wit
5. **Vignet gebruiken:** Voor compacte ruimtes waar het logo niet past
6. **Test toegankelijkheid:** Gebruik browser dev tools voor contrast checks
7. **Mobile first:** Test altijd op verschillende schermen

## 🔧 Aanpassen

Het framework is volledig customizable via CSS variabelen in `summa-styles.css`.

Wil je de skill instructies aanpassen?
1. Open `skill.md`
2. Pas de instructies aan
3. Test met `/huisstijl-summa`

## 📞 Support

- **GitHub Issues:** Report bugs of vraag features aan
- **Documentatie:** Raadpleeg het Summa Huisstijlhandboek (februari 2026)
- **Claude Code:** Gebruik `/huisstijl-summa` voor interactieve hulp

## 📄 Licentie

Deze skill en assets zijn eigendom van Summa College. Gebruik alleen voor Summa-gerelateerde projecten.
