# Technical Design Specification (`design.md`)

## 1. Visual Identity & Theme Overview

The design system for **Technolodia** establishes a modern, high-contrast, clean e-commerce interface utilizing a multi-color bento surface structure. The layout blends crisp neutral backgrounds (`--bg`, `--paper`) with deep structural ink (`--ink`) and vibrant indigo (`--indigo`) accents, delivering a polished tech ecosystem aesthetic.

---

## 2. Color Palette & CSS Variables

```css
:root {
  /* Surfaces & Backgrounds */
  --paper:        #FFFFFF;
  --bg:           #F8FAFC;
  --bg-soft:      #F1F5F9;
  --bg-deep:      #E2E8F0;

  /* Ink & Typography Colors */
  --ink:          #0F172A;
  --ink-soft:     #334155;
  --ink-mute:     #64748B;
  --ink-faint:    #94A3B8;

  /* Primary Indigo */
  --indigo:       #4F46E5;
  --indigo-deep:  #3730A3;
  --indigo-soft:  #EEF2FF;
  --indigo-line:  #C7D2FE;

  /* Multi-Color Bento Cards */
  --card-blue:    #1E2A78;
  --card-blue-2:  #2B3FB7;
  --card-purple:  #7C3AED;
  --card-purple-2:#C026D3;
  --card-orange:  #ff6a00; 
  --card-orange-2:#EA580C;
  --card-green:   #16A34A;
  --card-green-2: #15803D;
  --card-black:   #0A0A0A;

  /* Support & Utility */
  --rose:         #E11D48;
  --emerald:      #10B981;
  --amber:        #F59E0B;
  --rule:         #E2E8F0;
  --rule-strong:  #CBD5E1;

  /* Semantic Aliases */
  --accent:       var(--indigo);
  --accent-deep:  var(--indigo-deep);
  --accent-soft:  var(--indigo-soft);
  --fg:           var(--ink);
  --fg-soft:      var(--ink-soft);
  --fg-mute:      var(--ink-mute);
}

```

---

## 3. Typography & Hierarchy

* **Display Font (`--ff-display`):** `'Outfit', system-ui, -apple-system, 'Segoe UI', sans-serif` — Used for bold structural headings, hero blocks, and high-impact display titles.
* **Body Font (`--ff-body`):** `'Plus Jakarta Sans', system-ui, -apple-system, 'Segoe UI', sans-serif` — Used for clean, legible reading across UI components, descriptions, and buttons.
* **Monospace Font (`--ff-mono`):** `'Roboto Mono', ui-monospace, 'SF Mono', Menlo, monospace` — Used for technical data, code blocks, or tabular readouts.

### Type Scale

```css
:root {
  --text-xs:      12px;
  --text-sm:      13px;
  --text-base:    15px;
  --text-md:      17px;
  --text-lg:      20px;
  --text-xl:      24px;
  --text-2xl:     32px;
  --text-3xl:     40px;
  --text-display: clamp(1.75rem, 1rem + 2.4vw, 3.25rem);
  --text-hero:    clamp(2rem, 1.2rem + 3vw, 3.75rem);
}

```

---

## 4. Spacing, Layout & Radii

```css
:root {
  /* Spacing System */
  --s1: 4px; 
  --s2: 8px; 
  --s3: 12px; 
  --s4: 16px; 
  --s5: 20px;
  --s6: 28px; 
  --s7: 40px; 
  --s8: 56px; 
  --s9: 80px; 
  --s10: 112px;

  /* Layout Container */
  --container:    1280px;
  --container-pad: 24px;

  /* Border Radii */
  --r-sm: 6px;
  --r:    14px;
  --r-lg: 22px;
  --r-xl: 28px;
}

```

---

## 5. Shadows & Motion

```css
:root {
  /* Elevation Shadows */
  --shadow-sm:     0 1px 2px rgba(15,23,42,0.06);
  --shadow:        0 6px 18px -8px rgba(15,23,42,0.16), 0 2px 4px -2px rgba(15,23,42,0.06);
  --shadow-lg:     0 24px 60px -28px rgba(15,23,42,0.30), 0 8px 16px -10px rgba(15,23,42,0.08);
  --shadow-indigo: 0 12px 28px -10px rgba(79,70,229,0.35);

  /* Animation & Transition Ease */
  --ease: cubic-bezier(0.22, 1, 0.36, 1);
}

```

---

## 6. UI Component Patterns

### A. Bento Grid System

* Multi-color container configurations utilizing `--card-blue`, `--card-purple`, `--card-orange`, and `--card-green` variables to isolate promotional categories and showcase hero products with high visual contrast.

### B. Product & Content Cards

* Built on `--paper` surfaces with `--shadow` elevation, utilizing `--r` border radii (`14px`) and smooth hover transitions governed by `--ease`.

### C. Forms & Interactive Elements

* Form elements and action buttons leverage `--indigo` for primary CTAs, pairing `--ff-body` legibility with `--shadow-indigo` active states.
