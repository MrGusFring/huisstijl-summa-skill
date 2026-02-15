# Huisstijl Summa Skill

Deze custom skill helpt bij het toepassen van de Summa huisstijl.

## Installatie

### Via GitHub
```bash
cd ~/.claude/skills
git clone https://github.com/JOUW-USERNAME/huisstijl-summa-skill.git huisstijl-summa
```

### Via download
1. Download en pak het archief uit
2. Plaats de `huisstijl-summa` folder in `~/.claude/skills/`
3. Herstart Claude Code

De skill is nu beschikbaar via `/huisstijl-summa`

## Gebruik

Roep de skill aan met:
```
/huisstijl-summa
```

## Aanpassen

Je kunt de skill aanpassen door `skill.md` te bewerken:

1. Open het bestand: `~/.claude/skills/huisstijl-summa/skill.md`
2. Vul de specifieke Summa huisstijl richtlijnen in:
   - Kleurencodes
   - Lettertypes
   - Logo specificaties
   - Andere visuele elementen
3. Voeg eventueel extra instructies toe

## Structuur

```
~/.claude/skills/huisstijl-summa/
├── skill.md        # Hoofdbestand met skill definitie en instructies
├── README.md       # Deze documentatie
└── assets/         # (Optioneel) Map voor logo's, voorbeelden, etc.
```

## Tips

- Voeg voorbeeldbestanden toe in een `assets/` map
- Voeg specifieke kleurencodes toe in hexadecimaal formaat
- Documenteer alle huisstijl regels duidelijk in het skill.md bestand
- Test de skill door `/huisstijl-summa` uit te voeren
