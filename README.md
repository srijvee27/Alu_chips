# Henrietta Said : Scandalously Spicy

An interactive, high-energy promotional web landing page for **Henrietta Said** featuring scandalously spicy flavored peanuts (Ancho Kimchi, Nashville Hot Chicken, Original Buffalo, and Lemon Pepper). Built with HTML5, custom interactive physics-based mouse animations, smooth parallax effects, Webflow interactions, and bundled with **Vite**.

---

## Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Prerequisites](#prerequisites)
- [Installation & Setup](#installation--setup)
- [Running Locally](#running-locally)
- [Build for Production](#build-for-production)
- [Project Structure](#project-structure)
- [Architecture & Mechanics](#architecture--mechanics)
- [Environment Variables](#environment-variables)
- [Troubleshooting](#troubleshooting)
- [License](#license)

---

## Overview

The application is a single-page interactive showcase presenting Henrietta Said's bold snack product line. It incorporates custom responsive typography, complex visual animations, micro-interactions, dynamic floating physics with mouse repulsion, and structured JSON-LD schema metadata for SEO and rich product results.

---

## Key Features

- **Interactive Physics & Parallax**: Custom requestAnimationFrame-based mouse repulsion and lerp physics that react dynamically as the user moves their cursor over food elements and spicy snack visuals.
- **Product Flavor Showcase**: Dedicated interactive sections highlighting signature flavors:
  - Ancho Kimchi Peanuts
  - Nashville Hot Chicken Peanuts
  - Original Buffalo Peanuts
  - Lemon Pepper Peanuts
- **Engaging Typography & Design**: WebFont loader integrations with Google Fonts (such as *Changa One* and *Anton*) along with custom-crafted layout systems.
- **Nutritional & Benefit Highlighting**: Interactive tabs detailing dietary specifications (Vegan, Gluten-Free, Keto-Friendly, No Artificial Flavors).
- **Vite-Powered Development**: Lightning-fast Hot Module Replacement (HMR) and optimized static production builds with zero unnecessary runtime overhead.

---

## Tech Stack

- **Core**: Vanilla HTML5, CSS3, JavaScript (ES6+)
- **Bundler / Tooling**: [Vite](https://vite.dev/) (v6.x)
- **Styling**: Custom CSS & Webflow shared CSS (`css/henrietta-said.webflow.shared.css`)
- **Package Manager**: npm

---

## Prerequisites

Before running this project, ensure you have the following installed:

- **Node.js**: `v18.0.0` or higher (recommended: LTS)
- **npm**: `v9.0.0` or higher

Verify your installation:

```bash
node -v
npm -v
```

---

## Installation & Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/srijvee27/Alu_chips.git
   cd Alu_chips
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

---

## Running Locally

To start the Vite local development server with live reload and network exposure:

```bash
npm run dev
```

The terminal will provide the local address (defaults to port `5173`):
- **Local**: `http://localhost:5173/`
- **Network**: Accessible from devices on the same local network

---

## Build for Production

To create an optimized production build:

```bash
npm run build
```

This generates compiled, minified HTML, CSS, and asset bundles in the `dist/` directory.

To preview the production build locally before deployment:

```bash
npm run preview
```

---

## Project Structure

```text
Potato/
├── css/
│   └── henrietta-said.webflow.shared.css  # Main stylesheet and layout styles
├── index.html                             # Main application entry point & scripts
├── package.json                           # Project metadata, scripts, and dependencies
├── package-lock.json                      # Dependency lockfile
├── .gitignore                             # Git exclusion rules (node_modules, dist, etc.)
└── README.md                              # Project documentation
```

### Key Files Explained

- **`index.html`**: Root markup file containing semantic HTML5 sections, JSON-LD schema metadata for products, WebFont loaders, and custom canvas/DOM animation loops.
- **`css/henrietta-said.webflow.shared.css`**: Complete responsive styles, keyframes, transitions, and layout rules.
- **`package.json`**: Configured with ES modules (`"type": "module"`) running Vite development server on port 5173 with `--strictPort` and `--host` flags.

---

## Architecture & Mechanics

- **Static Single-Page Application (SPA)**: Pure clientside rendering with zero backend or database requirements.
- **Mouse Repulsion & Parallax Engine**:
  - Embedded vanilla JavaScript tracks cursor coordinates and updates element offsets via linear interpolation (`lerp`).
  - Calculates radial distance and applies trigonometric wave offsets (`Math.sin`) for natural floating effects and inertia.
- **Asset Delivery**: Visual assets, product imagery, and web icons are hosted via high-availability CDNs and rendered natively without heavy third-party framework overhead.

---

## Environment Variables

This project does not require any external environment variables or API keys. It runs entirely as a static frontend application out of the box.

---

## Troubleshooting

### Port 5173 Already in Use
The dev script is configured with `--strictPort`. If port `5173` is occupied by another process:
```bash
# Terminate the conflicting process or run Vite directly on a different port:
npx vite --port 5174
```

### Styles or Fonts Not Loading Offline
The application references CDN fonts (`fonts.googleapis.com`, `fonts.gstatic.com`) and asset URLs. Ensure you have an active internet connection during initial loading.

---

## License

This project's source code and promotional branding are maintained for project demonstration and presentation. All trademarks and brand assets belong to their respective owners.
