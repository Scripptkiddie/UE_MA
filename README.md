# Das Mittelalter im gymnasialen Deutschunterricht (BW)

Interaktive Übersicht der Mittelalter-Themen im Deutschunterricht nach Klassenstufen.

## 🚀 Setup

### PDFs hinzufügen

1. Lege deine PDFs in den `/pdfs` Ordner
2. Benenne sie nach diesem Schema: `klasseX-thema.pdf`

Beispiele:
- `pdfs/klasse5-maerchentexte.pdf`
- `pdfs/klasse8-ue-mittelalter.pdf`
- `pdfs/oberstufe-parzival.pdf`

### Felder aktivieren/deaktivieren

In `index.html` haben Zellen mit PDFs die Klasse `has-pdf`:

```html
<!-- Mit PDF (klickbar) -->
<div class="cell row-2 has-pdf" data-pdf="pdfs/klasse5-maerchentexte.pdf" onclick="openPdf(this)">

<!-- Ohne PDF (nicht klickbar) -->
<div class="cell row-2" data-pdf="pdfs/klasse6-volkssagen.pdf" onclick="openPdf(this)">
```

**Um eine PDF zu aktivieren:** Füge `has-pdf` zur Klasse hinzu.

**Um eine PDF zu deaktivieren:** Entferne `has-pdf` aus der Klasse.

## 📁 Projektstruktur

```
ma-deutschunterricht/
├── index.html      # Hauptseite
├── pdfs/           # Hier kommen deine PDFs rein
│   ├── klasse5-maerchentexte.pdf
│   ├── klasse8-ue-mittelalter.pdf
│   └── ...
└── README.md
```

## 🌐 Deployment auf Vercel

### Option 1: Über GitHub

1. Push das Projekt zu einem GitHub Repository
2. Gehe zu [vercel.com](https://vercel.com)
3. "New Project" → Importiere dein GitHub Repo
4. Deploy!

### Option 2: Vercel CLI

```bash
npm i -g vercel
cd ma-deutschunterricht
vercel
```

## 🎨 Anpassungen

### Farben ändern

Die Farben sind als CSS-Variablen in `index.html` definiert:

```css
:root {
    --color-accent: #c9a227;        /* Gold-Akzent */
    --color-bg: #0f0f0f;            /* Hintergrund */
    --color-surface: #1a1a1a;       /* Zellen-Hintergrund */
    --color-klasse5: #2d4a3e;       /* Header-Farbe Klasse 5 */
    /* ... */
}
```

### Neue Zeile/Spalte hinzufügen

Füge einfach neue `<div class="cell">` Elemente im Grid hinzu. Die Grid-Struktur passt sich automatisch an.
