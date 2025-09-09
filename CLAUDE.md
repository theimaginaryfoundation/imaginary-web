# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Current State

Minimal coming soon page - intentionally brutalist.

## Development Commands

```bash
# Local development
python3 -m http.server 8080
# or any static file server

# Deploy
git push  # GitHub Pages auto-deploys from main branch
```

## Architecture

**Current implementation:**
- Single index.html file (~1KB)
- Pure CSS, no JavaScript
- Monospace typography
- Formspree email capture

**Design philosophy:**
- Actually minimal, not "minimal"
- No animations, no gradients, no effects
- Black background, white text
- Single italic 'i' as focal point

## Files

```
imaginary-web/
├── index.html          # Everything
├── README.md          # Status
├── CLAUDE.md          # This file
└── IMAGINARY_FOUNDATION_COMING_SOON.md  # Future vision (not current implementation)
```

## Future Implementation

See IMAGINARY_FOUNDATION_COMING_SOON.md for the full mathematical manifesto vision. Current page is intentionally stripped back until ready to build the complete experience.