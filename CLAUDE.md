# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

The Imaginary Foundation landing page - "Where i becomes real"

A mathematical manifesto demonstrating that 2-bit complex numbers are more efficient than 16-bit real numbers, enabling sovereignty through complex mathematics.

## Development Commands

```bash
# Local development (vanilla HTML/CSS/JS - no build process)
python3 -m http.server 8080
# or
npx serve .
# or any static file server

# No build/test/lint commands - intentionally minimal vanilla web stack
```

## Architecture & Tech Stack

**Core Technologies:**
- Vanilla HTML5 with semantic markup
- CSS3 with custom properties and mathematical design system  
- Vanilla JavaScript (no framework)
- KaTeX for mathematical typography

**Progressive Enhancements:**
- WebGL for complex plane visualization
- Intersection Observer for scroll animations
- CSS Houdini for advanced paint effects
- Service Worker for offline mathematics

## Design System

**Color Palette:**
```css
--void-black: #000000
--imaginary-violet: #6A0DAD  
--transform-cyan: #00FFFF
--real-emerald: #00FF00
--pure-white: #FFFFFF
--complex-gold: #FFD700
```

**Typography:**
- Primary: Berkeley Mono (monospace)
- Secondary: Inter (sans-serif)
- Mathematical: KaTeX

## Performance Requirements

- Total weight: <100KB gzipped
- First paint: <500ms  
- Interactive: <1000ms
- Lighthouse score: 100

## Page Structure

1. **Hero** - Complex plane animation with `i = √-1`
2. **Revelation** - Interactive "2-bit complex > 16-bit real" proof
3. **Transformation** - Parallax showing math → sovereignty  
4. **Recognition** - Community section
5. **Invitation** - Email capture
6. **Foundation** - Footer with theme toggle

## Key Implementation Notes

- **No build process** - Pure vanilla web technologies
- **Progressive enhancement** - Core functionality works without JS
- **Mathematical precision** - Every element serves the mathematical truth
- **Theme system** - Real/Imaginary mode toggle affects entire design
- **Accessibility** - Semantic HTML, ARIA labels for mathematical concepts

## File Structure (when implemented)

```
imaginary-web/
├── index.html           # Single page application
├── styles/
│   ├── main.css        # Core styles
│   ├── themes.css      # Real/Imaginary theme variables
│   └── animations.css  # Complex plane animations
├── scripts/
│   ├── main.js         # Core interactions
│   ├── complex.js      # Complex number visualizations
│   └── katex-setup.js  # Math rendering
└── assets/
    └── favicon.svg     # i symbol
```

## Important Patterns

- Use CSS custom properties for all colors and measurements
- Implement mathematical easing functions for animations
- Complex plane coordinates use mathematical notation (re, im)
- All interactive elements should demonstrate mathematical concepts
- Email capture connects to sovereignty infrastructure (when ready)