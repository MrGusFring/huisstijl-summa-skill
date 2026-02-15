# Summa Huisstijl - Quick Reference Guide

Snelle referentie voor ontwikkelaars die met de Summa huisstijl werken.

## 📦 Installatie

```html
<link rel="stylesheet" href="path/to/summa-styles.css">
```

## 🎨 Kleuren

| Naam | Hex | RGB | Gebruik |
|------|-----|-----|---------|
| Indigo | `#20126E` | `32, 18, 110` | Primaire kleur, tekst, CTA's |
| Wit | `#FFFFFF` | `255, 255, 255` | Neutraal, achtergronden |
| Lichtgrijs | `#F4F4F4` | `244, 244, 244` | Assen, subtiele achtergronden |

### CSS Variabelen

```css
var(--summa-indigo)
var(--summa-white)
var(--summa-lightgrey)
```

### Contrast Richtlijnen (WCAG AA)
- Normale tekst: **minimaal 4.5:1**
- Grote tekst (≥18pt of ≥14pt bold): **minimaal 3:1**

## ✍️ Typografie

### Fonts

```css
/* Primary - Body tekst */
font-family: var(--font-primary);
/* Myriad Pro, Open Sans, sans-serif */

/* Secondary - Koppen & Quotes */
font-family: var(--font-secondary);
/* Bitter, Amasis Bold, Georgia, serif */
```

### Font Sizes

```css
--text-xs: 0.75rem    /* 12px */
--text-sm: 0.875rem   /* 14px */
--text-base: 1rem     /* 16px */
--text-lg: 1.125rem   /* 18px */
--text-xl: 1.25rem    /* 20px */
--text-2xl: 1.5rem    /* 24px */
--text-3xl: 2rem      /* 32px */
--text-4xl: 2.5rem    /* 40px */
--text-5xl: 3rem      /* 48px */
```

### Heading Schaal

```html
<h1><!-- 48px, Bitter Bold --></h1>
<h2><!-- 40px, Bitter Bold --></h2>
<h3><!-- 32px, Bitter Bold --></h3>
<h4><!-- 24px, Bitter Bold --></h4>
<h5><!-- 20px, Bitter Bold --></h5>
<h6><!-- 18px, Bitter Bold --></h6>
```

## 🔘 Components

### Buttons

```html
<!-- Primaire button -->
<button class="btn btn-primary">Klik hier</button>

<!-- Secundaire button -->
<button class="btn btn-secondary">Meer info</button>

<!-- Sizes -->
<button class="btn btn-primary btn-sm">Klein</button>
<button class="btn btn-primary">Normaal</button>
<button class="btn btn-primary btn-lg">Groot</button>
```

### Cards

```html
<!-- Standaard card -->
<div class="card">
  <div class="card-header">
    <h3 class="card-title">Titel</h3>
  </div>
  <div class="card-body">
    <p>Content hier...</p>
  </div>
  <div class="card-footer">
    <button class="btn btn-primary">Actie</button>
  </div>
</div>

<!-- Indigo card -->
<div class="card card-indigo">
  <!-- Witte tekst automatisch -->
</div>
```

### Forms

```html
<div class="form-group">
  <label class="form-label" for="naam">Naam</label>
  <input type="text" id="naam" class="form-input">
  <div class="form-help">Helpende tekst</div>
</div>

<div class="form-group">
  <label class="form-label" for="bericht">Bericht</label>
  <textarea id="bericht" class="form-textarea"></textarea>
</div>
```

## 📐 Layout

### Container

```html
<div class="container">
  <!-- Max-width 1200px, gecentreerd -->
</div>

<div class="container-fluid">
  <!-- Volledige breedte met padding -->
</div>
```

### Grid

```html
<div class="grid grid-cols-2"><!-- 2 kolommen --></div>
<div class="grid grid-cols-3"><!-- 3 kolommen --></div>
<div class="grid grid-cols-4"><!-- 4 kolommen --></div>

<!-- Automatisch responsive: 1 kolom op mobiel -->
```

### Sections

```html
<section class="section"><!-- Standaard padding --></section>
<section class="section-sm"><!-- Kleine padding --></section>
<section class="section-lg"><!-- Grote padding --></section>
```

## 🖼️ Logo & Vignet

### Logo Gebruik

```html
<!-- Op lichte achtergrond -->
<img src="assets/SUMMA_Logo_RGB_Indigo.png" alt="Summa" class="summa-logo">

<!-- Op donkere/indigo achtergrond -->
<img src="assets/SUMMA_Logo_RGB_Wit.png" alt="Summa" class="summa-logo">

<!-- Sizes -->
<img src="..." class="summa-logo-sm">  <!-- 120px -->
<img src="..." class="summa-logo">     <!-- 200px -->
<img src="..." class="summa-logo-lg">  <!-- 300px -->
```

### Vignet (Compact Beeldmerk)

```html
<!-- Voor avatars, icons, kleine ruimtes -->
<img src="assets/SUMMA_Vignet_indigo_RGB.png" class="summa-vignet">

<!-- Sizes -->
<img src="..." class="summa-vignet-sm">  <!-- 32px -->
<img src="..." class="summa-vignet">     <!-- 48px -->
<img src="..." class="summa-vignet-lg">  <!-- 64px -->
```

**Keuzeregel:**
- Lichte achtergrond → Indigo variant
- Donkere achtergrond → Witte variant
- **Geen** effecten, schaduwen, of borders

## 📏 Afgeronde Hoeken

### Formule
```
radius = korte zijde / 50
vlak-in-vlak = radius × 0.8
```

### CSS Variabelen

```css
--radius-sm: 4px    /* Kleine elementen */
--radius-md: 8px    /* Standaard (buttons, cards) */
--radius-lg: 12px   /* Grote cards */
--radius-xl: 16px   /* Hero sections */
--radius-2xl: 24px  /* Zeer grote sections */
```

### Classes

```html
<div class="rounded-sm"><!-- 4px --></div>
<div class="rounded-md"><!-- 8px --></div>
<div class="rounded-lg"><!-- 12px --></div>
<div class="rounded-xl"><!-- 16px --></div>
```

## 🎯 Pay Off

```html
<!-- Standaard (indigo op wit) -->
<div class="summa-payoff">
  Samen<br>kun je<br>meer.
</div>

<!-- Inverted (wit op indigo) -->
<div class="summa-payoff-inverted">
  Samen<br>kun je<br>meer.
</div>
```

**Let op:** Gebruik alleen wanneer nodig, niet automatisch met logo combineren.

## 🎨 Backgrounds

```html
<div class="bg-white"><!-- Witte achtergrond, indigo tekst --></div>
<div class="bg-indigo"><!-- Indigo achtergrond, witte tekst --></div>
<div class="bg-lightgrey"><!-- Lichtgrijze achtergrond --></div>
```

## 📱 Spacing

```css
--space-1: 0.25rem   /* 4px */
--space-2: 0.5rem    /* 8px */
--space-3: 0.75rem   /* 12px */
--space-4: 1rem      /* 16px */
--space-5: 1.25rem   /* 20px */
--space-6: 1.5rem    /* 24px */
--space-8: 2rem      /* 32px */
--space-10: 2.5rem   /* 40px */
--space-12: 3rem     /* 48px */
--space-16: 4rem     /* 64px */
--space-20: 5rem     /* 80px */
```

### Utility Classes

```html
<!-- Margins -->
<div class="mt-4"><!-- margin-top --></div>
<div class="mb-8"><!-- margin-bottom --></div>

<!-- Flexbox -->
<div class="flex items-center justify-between gap-4"></div>
<div class="flex flex-col gap-6"></div>

<!-- Text alignment -->
<div class="text-center"></div>
<div class="text-left"></div>
<div class="text-right"></div>
```

## 📞 Microregels

### Telefoonnummers
```
✓ Correct: 040 269 4000
✗ Fout: 040-269-4000
✗ Fout: 0402694000
```

**Regel:** Altijd met spaties, **nooit** met streepjes.

## ♿ Toegankelijkheid

### Focus States
```css
/* Automatisch voor alle interactieve elementen */
*:focus-visible {
  outline: 3px solid var(--summa-indigo);
  outline-offset: 2px;
}
```

### Skip Link
```html
<a href="#main-content" class="skip-link">Spring naar hoofdinhoud</a>
<!-- Onzichtbaar tot focus -->
```

### Reduced Motion
```css
/* Respecteert prefers-reduced-motion automatisch */
```

## 📋 Checklist voor Implementatie

- [ ] **Kleuren:** Alleen indigo, wit, lichtgrijs gebruikt
- [ ] **Contrast:** Minimaal 4.5:1 voor tekst online
- [ ] **Fonts:** Myriad Pro (body) + Bitter (koppen) met fallbacks
- [ ] **Logo:** Juiste variant op basis van achtergrond (indigo/wit)
- [ ] **Vignet:** Alleen voor compacte toepassingen
- [ ] **Radius:** Formule toegepast (korte zijde / 50)
- [ ] **Effecten:** Geen schaduwen/borders op logo
- [ ] **Telefoon:** Met spaties, zonder streepjes
- [ ] **Toegankelijkheid:** Focus states, skip links, alt teksten
- [ ] **Responsive:** Mobile-first, test op verschillende schermen

## 🔗 Bestanden

- `summa-styles.css` - Volledig CSS framework
- `demo.html` - Demo van alle elementen
- `components.html` - Component bibliotheek met voorbeelden
- `assets/` - Logo's en vignetten (indigo + wit varianten)

## 💡 Tips

1. **Start met de demo:** Open `demo.html` om alle mogelijkheden te zien
2. **Gebruik components:** Kopieer code uit `components.html` voor veelgebruikte patronen
3. **CSS Variabelen:** Gebruik altijd variabelen voor consistentie
4. **Contrast eerst:** Check online tools voor WCAG compliance
5. **Mobile-first:** Test altijd op verschillende schermformaten

## 📞 Vragen?

Raadpleeg het volledige Summa Huisstijlhandboek (februari 2026) of gebruik `/huisstijl-summa` in Claude Code.
