# Molly Davi | Utah Utes Commit

A three-page athlete portfolio site built for a D1 softball commit. Designed to showcase stats, story, and social presence in a clean, scroll-driven experience.

## Live Demo

https://necoliouss.github.io/molly-davi-site/

## What It Does

- Hero section with animated number reveal and softball-themed custom cursor
- Timeline of athletic journey from California to Utah
- Personality cards highlighting off-field interests
- Pre-game ritual section with animated braid visualization
- Full stats tables with sortable data
- National accolades and championship timeline
- Social link hub connecting all platforms

## Tech Stack

- Vanilla HTML/CSS/JS
- GSAP + ScrollTrigger for scroll animations
- Anime.js for entrance timelines and counter animations
- Google Fonts (Inter + Bebas Neue)
- PNG background textures with low opacity overlays

## What I Learned

GSAP's ScrollTrigger is powerful but unforgiving. I initially tried animating every element individually and hit performance issues on mobile. Switching to batching animations by section and using `start: 'top 85%'` as a universal trigger point kept things smooth. The custom baseball cursor was a fun experiment until I realized it breaks on touch devices — the `@media (max-width: 768px)` fallback disables it entirely.

The stats page has three different data sources (high school, travel ball, current team) and I wanted them visually distinct without breaking the design system. Using the same table component with different header labels kept it consistent. The counter animation for big numbers (226 strikeouts, 0.36 ERA) uses Anime.js with a custom `round` function because JavaScript's `toFixed` was adding trailing zeros where I didn't want them.

## Features

- Custom baseball cursor with hover states on interactive elements
- Responsive timeline that shifts from center-line to left-aligned on mobile
- Animated stat counters that trigger on scroll
- Consistent Utah red (#CC0000) design system across all pages
- No external CSS framework — everything is hand-written
