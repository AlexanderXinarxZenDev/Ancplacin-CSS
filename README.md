# 🪐 Ancplacin 1.2v

A modern, component-based CSS library with built-in Light/Dark/System theming, a responsive grid, and a tiny vanilla JavaScript module.

## 🆕 New in v1.2.0

- 🪗 **Accordion** – Collapsible content panels
- 🎠 **Carousel** – Image/slideshow carousel
- 💬 **Tooltip** – Hover tooltips with 4 positions
- 👤 **Avatar** – Profile pictures with initials fallback
- 🦴 **Skeleton** – Loading placeholders
- ✨ **More Utilities** – Shadows, Z-index, Transforms, Animations

## Features

- 🎨 **20+ Components** – Buttons, Cards, Modals, Toasts, Navbars, Sidebars, Tabs, Dropdowns, Tables, and more.
- 🌗 **Built-in Theming** – Light, Dark, and System (follows OS) modes.
- 📐 **12-Column Grid** – Flexbox-based, fully responsive.
- 🧩 **Utility Classes** – Spacing, Flexbox, Display, and Text helpers.
- 🪄 **Vanilla JS** – Declarative data attributes (`data-anc-toggle`, `data-anc-dismiss`) – no dependencies.
- 📱 **Responsive** – Mobile-first with breakpoint utilities.
- 🎯 **Accessible** – Focus states, keyboard navigation, and semantic HTML.

## Quick Start

### CDN (via unpkg)
```html
<!-- CSS -->
<link rel="stylesheet" href="https://unpkg.com/ancplacin@1.0.0/css/ancplacin.css" />

```

### npm
```bash
npm install ancplacin
```

```css
@import 'ancplacin/css/ancplacin.css';
```

## Usage

### Buttons
```html
<button class="anc-btn">Primary</button>
<button class="anc-btn anc-btn--secondary">Secondary</button>
<button class="anc-btn anc-btn--pill">Pill</button>
<button class="anc-btn anc-btn--circle">✕</button>
```

### Modal
```html
<button data-anc-toggle="modal" data-anc-target="#myModal">Open Modal</button>

<div class="anc-modal" id="myModal">
  <div class="anc-modal__dialog">
    <div class="anc-modal__header">
      <h3>Modal Title</h3>
      <button data-anc-dismiss="modal">✕</button>
    </div>
    <div class="anc-modal__body">Content here</div>
    <div class="anc-modal__footer">
      <button class="anc-btn anc-btn--outline" data-anc-dismiss="modal">Close</button>
      <button class="anc-btn">Save</button>
    </div>
  </div>
</div>
```

### Toast
```html
<button data-anc-toggle="toast" data-anc-message="Hello World!" data-anc-type="success">Show Toast</button>
```

### Theme Switcher
```html
<select id="themeToggle">
  <option value="light">Light</option>
  <option value="dark">Dark</option>
  <option value="system">System</option>
</select>

<script>
  document.getElementById('themeToggle').addEventListener('change', (e) => {
    document.documentElement.setAttribute('data-theme', e.target.value);
    localStorage.setItem('anc-theme', e.target.value);
  });
</script>
```

## Documentation

Full documentation is available at [https://ancplacin.dev](https://ancplacin.dev) *(Coming soon)*.

## License

MIT
```

---

### 📦 How to Publish to npm

1. **Create an npm account** (if you don't have one):
   ```bash
   npm adduser
   ```

2. **Login** (if already have an account):
   ```bash
   npm login
   ```

3. **Publish your library**:
   ```bash
   npm publish
   ```

4. **Update your version** (after changes):
   ```bash
   npm version patch  # 1.0.0 → 1.0.1
   npm version minor  # 1.0.0 → 1.1.0
   npm version major  # 1.0.0 → 2.0.0
   npm publish
   ```

---

### 🧪 Add to `index.html` for CDN Testing (Optional)
To test the npm package locally before publishing, you can replace your local imports in `index.html` with:

```html
<!-- Local -->
<link rel="stylesheet" href="./css/ancplacin.css" />

<!-- CDN (after publishing) -->
<link rel="stylesheet" href="https://unpkg.com/ancplacin@1.0.0/css/ancplacin.css" />
```
