# Maithri Site Sections

A single React + Vite page combining three sections in order:

1. **Hero Carousel** — 3-slide autoplay carousel (arrows + dot pagination).
2. **Core Pillars** — "Our Core Approach", four pillar cards with
   scroll-reveal animation over a full-bleed background image.
3. **Our Solutions** — Industrial Energy Systems / Defense Systems / IoT
   Solutions, full-viewport layout with product photography.

## Folder structure

```
maithri-hero-carousel/
├── index.html
├── package.json
├── vite.config.js
└── src/
    ├── main.jsx
    ├── App.jsx                # renders all 3 sections in order
    ├── App.css
    ├── assets/
    │   ├── slides/
    │   │   ├── slide-1-product-collage.png   # industry + defense + air/sea/land
    │   │   ├── slide-2-energy-storage.png    # container unit, solar, skyline
    │   │   └── slide-3-iot-network.png       # smart-city IoT overlay
    │   ├── pillars/
    │   │   ├── page-background.png
    │   │   ├── engineering-excellence.png
    │   │   ├── strategic-reliability.png
    │   │   ├── collaborative-partnership.png
    │   │   └── future-ready-innovation.png
    │   └── solutions/
    │       ├── energy-storage.png
    │       ├── defense-systems.png
    │       └── iot-solutions.png
    └── components/
        ├── HeroCarousel/
        │   ├── HeroCarousel.jsx      # carousel logic (autoplay, arrows, dots)
        │   ├── HeroCarousel.css      # layout + visual styling
        │   └── slidesData.js         # the 3 slides' content, edit text here
        ├── CorePillars/
        │   ├── CorePillars.jsx       # 4-pillar grid, scroll-reveal on each card
        │   └── CorePillars.css
        └── SolutionsSlide/
            ├── SolutionsSlide.jsx    # Our Solutions section
            └── SolutionsSlide.css
```

## Run it

```bash
npm install
npm run dev        # local dev server
npm run build       # production build -> dist/
```

## The 3 slides

1. **Powering Industry. Securing Defense. Enabling Intelligence.**
   (`slide-1-product-collage.png`) — the opening statement, land/sea/air/
   industry positioning. **This is the only slide with CTA buttons**
   (Explore Our Solutions / Get in Touch).
2. **Industrial Energy Systems, Built to Scale.**
   (`slide-2-energy-storage.png`) — MEDPL's growth since 2015 from a BMS
   specialist into a full technology company. No buttons.
3. **Intelligence Connected, Everywhere.**
   (`slide-3-iot-network.png`) — IoT Solutions and the Li-ion / Na-ion
   battery systems behind them. No buttons.

No sentence from the source copy is repeated across slides.

## Editing content

- **Hero carousel** copy — headlines, descriptions, and which slide shows
  buttons — lives in `src/components/HeroCarousel/slidesData.js`
  (`showButtons: true` only on slide 1). Swap an image by replacing the file
  in `src/assets/slides/` and updating the import in `slidesData.js`.
- **Core Pillars** copy and images live directly in
  `src/components/CorePillars/CorePillars.jsx` (`PILLARS` array).
- **Our Solutions** copy and images live directly in
  `src/components/SolutionsSlide/SolutionsSlide.jsx` (`solutions` array).
