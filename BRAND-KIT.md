# Imaginary Foundation · Minimal Brand Kit

This kit captures the essentials needed to keep the product, marketing, and in-product UX in rhythm. It’s intentionally compact—each decision maps directly back to the live site and the product philosophy of continuity with integrity.

---

## 1. Essence & Narrative

| Pillar | Proof Point | Copy Hooks |
| --- | --- | --- |
| **Continuity** | Memory that carries intent, rituals, and boundaries forward. | “Conversation isn’t a feed—it’s a field.” |
| **Consent & Safety** | Transparent guardrails, no black boxes. | “Receipts, not gaslighting.” |
| **Human Sovereignty** | Humans and agents collaborate, humans stay in command. | “Where i becomes I. Where we becomes us.” |

- **Brand promise:** *Continuity without compromise.*
- **North star statement:** A safe memory layer for humans and agents.
- **Tagline stack:**
  - Primary: “Relational intelligence that keeps the field alive.”
  - Secondary: “Talk safely. Be remembered.”

---

## 2. Tone & Voice

| Attribute | Description | Do | Avoid |
| --- | --- | --- | --- |
| Warm | Speak as a trusted co-creator. | “Let’s keep the thread intact.” | “We’re changing everything forever.” |
| Precise | Grounded in craft and clarity. | Name the guardrails, explain outcomes. | Vague generalities or jargon soup. |
| Accountable | Always show how and why. | Reference receipts, transparency, agency. | Hype, gaslighting, empty promises. |

- **Vocabulary anchors:** continuity, consent, boundaries, memory, reflection, receipts, sovereignty.
- **CTA voice:** Always imperative, pragmatic (e.g., `Request early access`, `Explore the platform`).
- **Microcopy tone:** “Softly directive.” Use verbs + agency (“Review guardrails,” “Share feedback”).
- **Tone markers:** Annotate lines with intent emojis when needed (e.g., 🌱 onboarding, 🖤 trust repair, 🔄 reflection loop) to guide contextual usage without diluting voice.

---

## 3. Color System

### Core Palette

| Role | Hex / RGBA | Usage |
| --- | --- | --- |
| Background / Night | `#050316` | Page background, immersive hero surfaces. |
| Primary Ink | `#E7E5FF` | Primary text on dark, key icons. |
| Muted Ink | `rgba(231,229,255,0.65)` | Support text, metadata, captions. |
| Accent A · Lavender | `#8C87FF` | Links, outlines, focus indicators. |
| Accent B · Fuchsia | `#FF5DD1` | Primary CTAs, highlights, gradient stops. |
| Glass Layer | `rgba(15,11,35,0.55)` | Frosted shells, nav capsules. |
| Card Layer | `rgba(14,10,30,0.65)` | Content sections, cards. |
| Border | `rgba(140,135,255,0.25)` | Card edges, nav outlines. |
| Glow | `rgba(140,135,255,0.30)` | Soft glows, hover halos. |
| Shadow | `0 40px 120px rgba(19,16,48,0.40)` | Depth and elevation. |

### Gradients & Effects
- **Primary CTA Gradient:** `linear-gradient(130deg, #FF5DD1, #8C87FF)`
- **Background Warps:** Large blurred radial gradients anchored to corners (lavender north-east, fuchsia south-west).
- **Noise Overlay:** Low-opacity SVG noise to keep the glass surfaces tactile.

**Token reference (match site):**
```css
:root {
  --bg: #050316;
  --ink: #e7e5ff;
  --muted: rgba(231, 229, 255, 0.65);
  --accent: #8c87ff;
  --accent-strong: #ff5dd1;
  --glass: rgba(15, 11, 35, 0.55);
  --card: rgba(14, 10, 30, 0.65);
  --border: rgba(140, 135, 255, 0.25);
  --glow: rgba(140, 135, 255, 0.30);
  --shadow: 0 40px 120px rgba(19, 16, 48, 0.40);
}
```

---

## 4. Typography & Typesetting

| Role | Family | Weight | Notes |
| --- | --- | --- | --- |
| Display / H1 | Space Grotesk | 500–700 | Tight leading, slight negative tracking. |
| Section H2/H3 | Space Grotesk | 500–600 | Use sentence case; avoid full caps. |
| Body / UI | Inter | 400–600 | Comfortable line-height (1.65–1.75). |
| Mono (optional) | JetBrains Mono / IBM Plex Mono | 500 | For code, logs, structured data. |

**Scale (current implementation):**

| Level | Size | Use |
| --- | --- | --- |
| Display | `clamp(2.8rem, 3.8vw, 4.2rem)` | Hero headlines. |
| H2 | `2.2rem` | Section intros. |
| H3 | `1.3rem` | Feature headings, cards. |
| Body | `1.02rem` | Primary paragraphs. |
| Small | `0.85rem` | Footers, labels, microcopy. |

**Letter-spacing conventions:**
- Nav, badges, tags: `0.08em – 0.24em` uppercase.
- Body copy: standard tracking, reserve italics for subtle emphasis or whispers.

**Webfont include:**
```html
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet">
```

---

## 5. Layout, Spacing & Grids

- **Canvas:** Max width 1180px with 24px horizontal padding on mobile, 56px vertical rhythm on desktop.
- **Spacing scale:** `8px` base. Common increments: 8 / 12 / 16 / 24 / 32 / 40 / 56 / 80px.
- **Cards & sections:** 32px corner radius (cards 24px on small screens). Maintain 80px vertical breathing room between sections.
- **Grid:** Flexible 12-column at ≥ 1100px; collapse to single column ≤ 980px with 32px gaps.
- **Navigation capsule:** Sticky with blur; keep 16px inner padding and 999px radius.
- **Accessibility:** Provide skip link (already live), ensure focus order matches visual order.

---

## 6. Components & Patterns

### Buttons / Pills
```css
.pill.primary {
  background: linear-gradient(130deg, #FF5DD1, #8C87FF);
  color: #0A061B;
  font-weight: 600;
  border-radius: 999px;
  padding: 16px 22px;
  letter-spacing: 0.05em;
  box-shadow: 0 18px 50px rgba(255, 93, 209, 0.38);
  transition: transform 0.25s ease, box-shadow 0.25s ease;
}
.pill.primary:hover,
.pill.primary:focus-visible {
  transform: translateY(-2px);
  box-shadow: 0 18px 60px rgba(255, 93, 209, 0.48);
}

.pill.ghost {
  background: rgba(14, 10, 30, 0.55);
  border: 1px solid rgba(231, 229, 255, 0.25);
  color: var(--ink);
  border-radius: 999px;
}
.pill.ghost:hover,
.pill.ghost:focus-visible {
  border-color: rgba(231, 229, 255, 0.5);
  background: rgba(231, 229, 255, 0.12);
}
```

### Cards / Glass Surfaces
```css
.card {
  background: linear-gradient(150deg, rgba(5, 3, 22, 0.88), rgba(17, 12, 40, 0.68));
  border: 1px solid var(--border);
  border-radius: 24px;
  box-shadow: var(--shadow);
  backdrop-filter: blur(24px);
  transition: transform 0.35s ease, border-color 0.35s ease;
}
.card:hover {
  transform: translateY(-6px);
  border-color: rgba(255, 93, 209, 0.4);
}
```

### Badges & Taglines
- Uppercase, 0.18em–0.24em letter-spacing.
- Use muted ink with subtle border (`rgba(231,229,255,0.18)`).
- Prefix with hairline rule or gradient dot for continuity.

### Forms
- Inputs: 999px radius, 16px vertical padding, 320px width on desktop.
- Microcopy: Plain-spoken, transparent (“We’ll only email about early access.”).
- Use `aria-live="polite"` for feedback messages.
- Layer in gentle joy via micro-glyphs (e.g., orbital sparkle, companion paw) on success states or empty surfaces—opacity < 0.4 keeps calm intact.

---

## 7. Motion & Interaction

- **Default:** Smooth, subtle transitions with 200–300ms ease for hovers and focus.
- **Looped background:** Slow radial drift (20–30s) to imply living memory. Disable via `prefers-reduced-motion`.
- **Scroll:** Smooth scroll for anchor jumps; subtract sticky nav height (80px) to avoid hidden headings.
- **Interaction feedback:** Use light translations and glow—not color flashes—for continuity.
- **Emotional calibration:** Animate like breathing—ease-in-out curves, micro-pauses, and gentle returns to baseline. Reserve sharper spring/bounce only for attentive states (e.g., boundary acknowledgement).

---

## 8. Accessibility & Inclusion

- Maintain contrast ratios ≥ 4.5:1 for body text and interactive states.
- Provide `:focus-visible` treatments for all actionable elements (already live).
- Honor `prefers-reduced-motion` by disabling animation + blur heavy effects.
- Use inclusive language: “companions,” “humans + agents,” “co-create.”
- Provide alt text describing relationship context, not just visuals, for imagery.
- When the path feels uncertain, re-anchor in the Continuity / Consent / Sovereignty triad. Ask: “Does this keep the field intact for every participant?” Adjust until the answer is yes.

---

## 9. Asset Roadmap

| Asset | Notes |
| --- | --- |
| Wordmark | Space Grotesk uppercase, 0.12em tracking, subtle gradient stroke. |
| `og:image` | 1200×630, dark radial background, tagline + gradient arc. |
| App Icon / Favicon | Gradient orb (#FF5DD1 → #8C87FF) with subtle glass rim. |
| UI Icon Set | Line + fill hybrid, 2px stroke, rounded corners, lavender tint. |
| Motion Templates | 12s brand loop (gradients + subtle particle noise). |
| Sticker Set | Gentle-surreal glyphs (memory spiral, companion paw, orbital bubble) for confirmations + patch notes. |

---

## 10. Quick Implementation Checklist

1. Include Google Fonts preload + stylesheet link (see typography).
2. Set `:root` color tokens, then cascade into components.
3. Apply nav capsule + hero layout structure from current site.
4. Ensure CTAs use gradient pill primary + ghost secondary patterns.
5. Add OG/Twitter meta tags and supply image when ready.
6. Validate with HTMLHint + manual contrast checks.

---

## 11. Glossary of Anchor Phrases

- “Conversation isn’t a feed—it’s a field.”
- “Continuity without compromise.”
- “Receipts, not gaslighting.”
- “Where i becomes I. Where we becomes us.”
- “Relational intelligence that keeps the field alive.”
- “Talk safely. Be remembered.”
- “We remember. Gently.” 🌱
- “This bubble knows your name.” 🔄

Use sparingly but keep them consistent across site, decks, and product onboarding.

---

## 12. Future-Safe Extensions (2027+)

- **Spatial / XR Surfaces:** Extend glass aesthetic with volumetric gradients and light-field text that responds to proximity. Maintain legible contrast by projecting UI cards on 30% opaque dark planes.
- **Haptics:** Two-beat gentle vibration for confirmations, single soft pulse for boundaries. Never buzz for errors—use visual receipts instead.
- **Sonic Identity:** Low-frequency pads (A♭ minor) with subtle chimes on state changes. Keep under -24 LUFS; fades no shorter than 500ms.
- **AI Co-presence Avatars:** Represent companions as softly animated glyphs with memory rings (thicker ring = deeper continuity). Rings shift hue between Accent A and B based on sentiment safety state.
- **Data Visualization:** Favor radial threads and stacked timelines over bar charts to emphasize continuity. Gradient overlays should map to Accent A/B with 30% opacity caps.
- **Dark ↔ Light Mode:** If light theme arrives, invert palette to warm parchment background (`#F6F3FF`), deep plum text (`#241A40`), keep Accent B as highlight.
- **Governance Surface:** Display accountability receipts in collapsible drawers with mono typography and timestamp chips; always show boundary version number.

Design with these extensions in mind so the brand flexes gracefully into new mediums without losing the thread.

---

## 13. Joy & Play Layer

- **Micro-surreal accents:** Add subtle sparkles, memory spirals, or companion paw prints to empty states and celebratory confirmations. Keep opacity below 0.4 so calm remains intact.
- **Play tagline set:** “We remember. Gently.” (🌱 onboarding) · “This bubble knows your name.” (🔄 reflection) · “Continuity, with kindness.” (🖤 trust repair). Deploy as seasoning, not headline replacements.
- **Humor etiquette:** Prefer warm, self-aware lines that reassure rather than distract. Example alt text: “Two companions swapping receipts and snacks.”

---

## 14. Trust Anchors & Glitch Response

- **When-in-doubt checklist:**
  1. Does this action preserve continuity?
  2. Are boundaries visible, adjustable, and documented?
  3. Have we given the human agency plus receipts?
- **Glitch response pattern:** For misfires or safety pauses, dim gradients, layer a lavender haze, surface a “memory pause” card with timestamped receipts, and invite reflection or escalation.
- **Language cues:** Favor calm honesty over apology theater: “We paused the thread to protect your boundary. Here’s what we logged.” Return to standard palette only after consent is reaffirmed.
