# Cursor Landing Page — Recreation

A pixel-faithful recreation of [cursor.com](https://cursor.com)'s marketing landing page, built with plain HTML, CSS, and Vite as the dev server.

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or later recommended)
- [Bun](https://bun.sh/) or npm

### Installation

```bash
# Install dependencies
npm install
# or
bun install
```

### Development

```bash
npm run dev
# or
bun dev
```

The site will be available at `http://localhost:5173` (Vite default).

### Build for Production

```bash
npm run build
```

### Preview Production Build

```bash
npm run preview
```

---

## 📄 Sections Recreated

| Section | Description |
|---|---|
| **Navbar / Header** | Fixed top navigation with the Cursor SVG wordmark logo, nav links (Product, Enterprise, Pricing, Resources), and Sign In / Download pill buttons |
| **Hero** | Full-width headline, primary CTA download button, and product screenshot |
| **Trusted By** | "Trusted every day by millions of professional developers" copy with an 8-column grid of company logos (Stripe, OpenAI, Linear, Datadog, NVIDIA, Figma, Ramp, Adobe) |
| **Features** | Three alternating image-and-text feature blocks — *Agent turns ideas into code*, *Magically accurate autocomplete*, and *Everywhere software gets built* |
| **Testimonials** | "The new way to build software" heading with a 3×2 card grid of real quotes from Diana Hu (YC), Jensen Huang (NVIDIA), Andrej Karpathy, Patrick Collison (Stripe), shadcn, and Greg Brockman (OpenAI) |
| **Stay on the Frontier** | Three use-case cards with auto-playing looped video demos — model selection, codebase understanding, and enterprise |
| **Changelog** | Four-column grid of recent release entries with dates and titles |
| **About** | Company mission banner with team photo |
| **Recent Highlights** | Sticky-heading layout with three article/blog post cards (Research, Product, Customers) |
| **Try Cursor Now** | Full-width CTA section with large heading and download button |
| **Footer** | Five-column link grid (Product, Resources, Company, Legal, Connect) plus copyright, SOC 2 badge, and language selector |

---

## 🎨 Fonts & Colors

### Typography

| Font | Source | Usage |
|---|---|---|
| **CursorGothic Regular** | Self-hosted `.woff2` (`/fonts/CursorGothic_Regular-s.p.a361088d.woff2`) | Primary body & UI text |
| **CursorGothic Italic** | Self-hosted `.woff2` (`/fonts/CursorGothic_Italic-s.p.00bb2606.woff2`) | Italic variants |
| **CursorGothic Bold** | Self-hosted `.woff2` (`/fonts/CursorGothic_Bold-s.p.95169710.woff2`) | Bold headings |
| **CursorGothic Bold Italic** | Self-hosted `.woff2` (`/fonts/CursorGothic_BoldItalic-s.p.036859cb.woff2`) | Bold italic |
| **System fallback stack** | Browser native | `system-ui, Helvetica Neue, Helvetica, Arial, sans-serif` |

### Color Palette

| CSS Variable / Usage | Hex | Description |
|---|---|---|
| `--bg-theme` | `#14120b` | Main page background — very dark warm black |
| `--logo-bg-theme` | `#1b1913` | Card / section backgrounds — slightly lighter warm dark |
| `--btn-theme` | `#edecec` | Primary text & button color — off-white |
| Accent (CTA links / buttons) | `#f54e00` | Cursor orange — used for "Learn about Agent →" links and card link anchors |
| Nested card background | `#201e18` | Inner CTA cards in the Recent Highlights section |
| Language button background | `#26241e` | Footer language selector background |
| Body text | `#edecec` | Same as `--btn-theme` |
| Muted text | `#edecec` at `opacity: 60%` | Secondary/subtext content throughout |

> **Palette summary:** The entire design operates on a warm dark-brown/charcoal family (`#14120b` → `#1b1913` → `#201e18` → `#26241e`) with a single high-contrast off-white (`#edecec`) and one vivid accent orange (`#f54e00`).

---

## 🗂 Project Structure

```
Cursor - Landing Page/
├── index.html          # All markup — sections, nav, footer
├── src/
│   └── style.css       # All styles — design tokens, layout, components
├── public/
│   ├── fonts/          # Self-hosted CursorGothic woff2 files
│   ├── card-img/       # Testimonial avatar images
│   ├── animation-videos/  # Looping feature demo .mp4 files
│   ├── image-product.png
│   ├── feature-1.png / feature-2.png / feature-3.png
│   ├── about-img.png
│   └── card-img-1.webp
├── package.json
└── bun.lock
```

---

## 📝 Notes

- Company logos in the **Trusted By** section are loaded directly from Cursor's public Vercel blob storage URLs.
- The Cursor favicon is sourced from `https://cursor.com/marketing-static/favicon.svg`.
- All nav links point to the live `cursor.com` domain; internal page routing is not implemented.
- This project is a **peer review / study exercise** and is not affiliated with Anysphere, Inc.
