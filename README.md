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

Gemaakt door MONA / V1.0 / SUMMA
