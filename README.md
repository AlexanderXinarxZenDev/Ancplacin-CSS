# 🪐 Ancplacin CSS

**A modern, component-based CSS library with built-in theming, responsive grid, and 30+ UI components.**

[![npm version](https://img.shields.io/npm/v/ancplacin-css)](https://www.npmjs.com/package/ancplacin-css)
[![npm downloads](https://img.shields.io/npm/dt/ancplacin-css)](https://www.npmjs.com/package/ancplacin-css)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Libraries.io SourceRank](https://img.shields.io/librariesio/sourcerank/npm/ancplacin-css)](https://libraries.io/npm/ancplacin-css)

---

## ✨ Features

- 🎨 **30+ Components** – Buttons, Cards, Modals, Toasts, Navbars, Sidebars, Tabs, Dropdowns, Tables, Accordions, Carousels, Tooltips, Avatars, Skeleton Loaders, Offcanvas, Popovers, Scrollspy, and more.
- 🌗 **Built-in Theming** – Light, Dark, and System (follows OS) modes – just add `data-theme="dark"` to `<html>`.
- 📐 **12-Column Flexbox Grid** – Fully responsive with breakpoints (sm, md, lg, xl).
- 🎬 **Animation Utilities** – 20+ ready-to-use animations (fade, slide, bounce, zoom, shake, pulse, spin, flip, wobble, swing, jelly, and more).
- 🧩 **Utility Classes** – Spacing, Flexbox, Display, Text, Border, Shadows, Z-index, Transforms, and more.
- 📱 **Mobile-First** – Responsive utilities for showing/hiding elements.
- 🎯 **Accessible** – Focus states and keyboard navigation support.
- 🪄 **Zero Dependencies** – Pure CSS, no JavaScript required (but optional JS module coming soon).

---

## 🚀 Quick Start

### CDN (via unpkg)

```html
<!-- Production (minified) -->
<link rel="stylesheet" href="https://unpkg.com/ancplacin-css@1.2.9/css/ancplacin.min.css" />

<!-- Development (unminified) -->
<link rel="stylesheet" href="https://unpkg.com/ancplacin-css@1.2.9/css/ancplacin.css" />
```

### npm

```bash
npm install ancplacin-css
```

```css
/* Import into your main CSS file */
@import 'ancplacin-css/css/ancplacin.css';

/* Or include in your HTML */
<link rel="stylesheet" href="./node_modules/ancplacin-css/css/ancplacin.css" />
```

---

## 📖 Usage Examples

### Buttons

```html
<button class="anc-btn">Primary</button>
<button class="anc-btn anc-btn--secondary">Secondary</button>
<button class="anc-btn anc-btn--success">Success</button>
<button class="anc-btn anc-btn--danger">Danger</button>
<button class="anc-btn anc-btn--outline">Outline</button>
<button class="anc-btn anc-btn--pill">Pill</button>
<button class="anc-btn anc-btn--circle">✕</button>
<button class="anc-btn anc-btn--sm">Small</button>
<button class="anc-btn anc-btn--lg">Large</button>
<button class="anc-btn anc-btn--block">Block</button>
```

### Cards

```html
<div class="anc-card anc-card--elevated">
  <div class="anc-card__header">
    <h3>Card Title</h3>
  </div>
  <div class="anc-card__body">
    <p>Card content goes here. Fully theme-aware.</p>
  </div>
  <div class="anc-card__footer">
    <button class="anc-btn anc-btn--sm">Action</button>
  </div>
</div>
```

### Grid System

```html
<div class="anc-container">
  <div class="anc-row">
    <div class="anc-col-6 anc-col-md-4">Column 1</div>
    <div class="anc-col-6 anc-col-md-4">Column 2</div>
    <div class="anc-col-12 anc-col-md-4">Column 3</div>
  </div>
</div>
```

### Modal

```html
<!-- Trigger -->
<button class="anc-btn" data-anc-toggle="modal" data-anc-target="#myModal">Open Modal</button>

<!-- Modal -->
<div class="anc-modal" id="myModal">
  <div class="anc-modal__dialog">
    <div class="anc-modal__header">
      <h3>Modal Title</h3>
      <button class="anc-modal__close" data-anc-dismiss="modal">&times;</button>
    </div>
    <div class="anc-modal__body">Content here</div>
    <div class="anc-modal__footer">
      <button class="anc-btn anc-btn--outline" data-anc-dismiss="modal">Close</button>
      <button class="anc-btn">Save</button>
    </div>
  </div>
</div>
```

### Offcanvas (Pure CSS)

```html
<!-- Trigger -->
<a href="#offcanvasLeft" class="anc-btn">Open Left Offcanvas</a>

<!-- Offcanvas -->
<div class="anc-offcanvas anc-offcanvas--left" id="offcanvasLeft">
  <div class="anc-offcanvas__header">
    <h3>Left Menu</h3>
    <a href="#" class="anc-offcanvas__close">&times;</a>
  </div>
  <div class="anc-offcanvas__body">
    <p>Content here</p>
  </div>
</div>
<div class="anc-offcanvas__backdrop anc-offcanvas__backdrop--left">
  <a href="#" style="display:block; width:100%; height:100%;"></a>
</div>
```

### Popovers

```html
<!-- Hover Popover -->
<div class="anc-popover anc-popover--top">
  <button class="anc-btn">Hover me</button>
  <div class="anc-popover__content">
    <span class="anc-popover__arrow"></span>
    <strong>Top Popover</strong>
    <p>Content here</p>
  </div>
</div>

<!-- Click Popover -->
<div class="anc-popover anc-popover--bottom anc-popover--click">
  <input type="checkbox" id="popoverToggle" class="anc-popover__toggle" />
  <label for="popoverToggle" class="anc-btn">Click me</label>
  <div class="anc-popover__content">
    <span class="anc-popover__arrow"></span>
    <strong>Click Popover</strong>
    <p>Content here</p>
    <label for="popoverToggle" class="anc-btn anc-btn--sm anc-btn--outline">Close</label>
  </div>
</div>
```

### Scrollspy (Pure CSS)

```html
<div class="anc-scrollspy">
  <nav class="anc-scrollspy__nav">
    <ul class="anc-scrollspy__list">
      <li><a href="#section1" class="anc-scrollspy__link">Section 1</a></li>
      <li><a href="#section2" class="anc-scrollspy__link">Section 2</a></li>
    </ul>
  </nav>
  <div class="anc-scrollspy__content">
    <div class="anc-scrollspy__section" id="section1">
      <h3>Section 1</h3>
      <p>Content...</p>
    </div>
    <div class="anc-scrollspy__section" id="section2">
      <h3>Section 2</h3>
      <p>Content...</p>
    </div>
  </div>
</div>
```

### Animations

```html
<div class="anc-animate anc-animate-fade-in-up">Fade In Up</div>
<div class="anc-animate anc-animate-bounce anc-animate--infinite">Bounce Forever</div>
<div class="anc-animate anc-animate-pulse anc-animate--delay-1">Pulse with Delay</div>

<!-- Hover effects -->
<button class="anc-btn anc-hover-scale">Scale on Hover</button>
<button class="anc-btn anc-btn--secondary anc-hover-lift">Lift on Hover</button>
<button class="anc-btn anc-btn--success anc-hover-glow">Glow on Hover</button>
```

### Theme Switcher

```html
<select id="themeToggle">
  <option value="light">☀️ Light</option>
  <option value="dark">🌙 Dark</option>
  <option value="system">💻 System</option>
</select>

<script>
  document.getElementById('themeToggle').addEventListener('change', (e) => {
    document.documentElement.setAttribute('data-theme', e.target.value);
    localStorage.setItem('anc-theme', e.target.value);
  });
</script>
```

---

## 🆕 What's New in v1.2.9

- 🎨 **Offcanvas** – Slide-in panels from left, right, or bottom (pure CSS using `:target`)
- 💬 **Popovers** – Hover or click popovers with arrows (4 positions)
- 📍 **Scrollspy** – Auto-highlight navigation links based on targeted sections
- 🎬 **Animation Utilities** – 20+ animations: fade, slide, bounce, zoom, shake, pulse, flip, wobble, swing, jelly, spin, and more
- ⏱️ **Animation Controls** – Speed modifiers (`--fast`, `--slow`), delays (`--delay-1/2/3`), infinite looping (`--infinite`)
- 🐛 **Bug Fixes** – Improved modal z-index, toast stacking, dark mode contrast, accordion transitions
- 🧹 **Code Cleanup** – Removed duplicate imports, better comments

---

## 📦 All Components

| Category | Components |
|----------|------------|
| **Core** | Buttons, Forms, Cards, Badges, Alerts, Toasts, Tables, List Groups |
| **Navigation** | Navbar, Sidebar, Breadcrumbs, Pagination |
| **Layout** | Grid (12-column), Containers, Utilities (spacing, flex, display) |
| **Overlays** | Modal, Offcanvas, Popovers, Tooltips (CSS-only) |
| **Data Display** | Tabs, Accordion, Carousel, Avatar, Skeleton Loaders |
| **Feedback** | Progress Bars, Spinners, Alerts, Toasts |
| **Interaction** | Dropdowns, Scrollspy |
| **Animations** | Fade, Slide, Bounce, Zoom, Shake, Pulse, Flip, Wobble, Swing, Jelly, Spin, more |

---

## 🌗 Theme System

Ancplacin CSS uses CSS Custom Properties for theming:

```css
/* Light theme (default) */
:root { /* light variables */ }

/* Dark theme */
[data-theme="dark"] { /* dark variables */ }

/* System theme (follows OS) */
@media (prefers-color-scheme: dark) {
  [data-theme="system"] { /* dark variables */ }
}
```

Just add `data-theme="dark"` to `<html>` to enable dark mode.

---

## 🧩 Utility Classes

| Category | Classes |
|----------|---------|
| **Display** | `.anc-d-none`, `.anc-d-block`, `.anc-d-flex`, `.anc-d-grid` |
| **Flexbox** | `.anc-flex-row`, `.anc-flex-col`, `.anc-items-center`, `.anc-justify-between`, `.anc-gap-{1-5}` |
| **Spacing** | `.anc-m-{1-5}`, `.anc-p-{1-5}`, `.anc-mt-{1-5}`, `.anc-mb-{1-5}`, `.anc-mx-auto` |
| **Text** | `.anc-text-center`, `.anc-text-left`, `.anc-text-right`, `.anc-text-muted` |
| **Borders** | `.anc-border`, `.anc-border-top`, `.anc-border-0` |
| **Shadows** | `.anc-shadow-sm`, `.anc-shadow-md`, `.anc-shadow-lg` |
| **Z-index** | `.anc-z-10`, `.anc-z-20`, `.anc-z-50` |
| **Animations** | `.anc-animate-*`, `.anc-hover-*`, `.anc-transition` |
| **Responsive** | `.anc-d-none-md`, `.anc-d-block-lg`, `.anc-d-flex-xl` |

---

## 📚 Documentation

Full documentation is coming soon at [https://ancplacin.dev](https://ancplacin.dev).

For now, see the [demo page](./index.html) or the [source code](https://codeberg.org/Alexandaz/AncplacinCSS).

---

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing`)
5. Open a Pull Request

---

## 📄 License

MIT © [Alexandaz](https://codeberg.org/Alexandaz)

---

## ⭐ Star the Project

If you find Ancplacin CSS useful, please star the repository on Codeberg:

[![Codeberg Repo](https://img.shields.io/badge/Codeberg-Repository-blue)](https://codeberg.org/Alexandaz/AncplacinCSS)

---
