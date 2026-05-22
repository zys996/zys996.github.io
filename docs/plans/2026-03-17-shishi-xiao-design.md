# Design Context & System — Shishi Xiao Homepage

**Date:** 2026-03-17  
**Aesthetic Direction:** A. Institutional Minimalism  
**Theme:** Clean & Academic with Dark Mode option  

---

## Design Context

### Users
Academic researchers and peers in visualization/HCI fields. Primary context: discovering research background, reading publication details, accessing contact/social links. Secondary context: exploring research interests and experience trajectory.

### Brand Personality
**Three words:** Thoughtful, Rigorous, Visual  
**Voice & Tone:** Scholarly yet approachable; focused on clarity over decoration; let the work speak.  
**Emotional Goals:** Inspire confidence in research depth; make complex visual research accessible; convey carefully curated thinking.

### Aesthetic Direction
**Institutional Minimalism** — Traditional scholarship aesthetic with serif typography, subtle structure, and timeless elegance. Serif fonts evoke scholarly depth; generous margins and whitespace create breathing room; content hierarchy through subtle size/weight shifts, not color or decoration. No visual clutter. Static, reading-forward. Single-column center layout with generous margins. Dark mode support using desaturated tonal variants.

**Anti-references:** Avoid corporate "startup minimalism" (sans-serif, flat elements, aggressive spacing). Avoid portfolio-gallery aesthetic (image-heavy, grid-based). Avoid technical/monospace feel (too cold for scholarship).

### Design Principles
1. **Content First** — Typography and hierarchy surface what matters; whitespace shapes perception, not decoration
2. **Scholarly Clarity** — Multi-level reading support: skim headings, read body, explore links (publications, social)
3. **Restrained Elegance** — Subtle serif details + generous margins create timeless feel; no trendy effects
4. **Accessibility as Standard** — Robust contrast, keyboard navigation, semantic structure; dark mode fully supported
5. **Responsive Harmony** — Single-column layout adapts gracefully; no breakpoint surprises; mobile = desktop content, not simplified version

---

## Design System

### Color Palette

**Light Mode:**
- **Background:** `#FAFAF8` (warm off-white)
- **Surface:** `#FFFFFF` (pure white for contacts/links sections)
- **Text Primary:** `#1A1A18` (near-black with warmth)
- **Text Secondary:** `#6B6B68` (medium gray for metadata, timestamps)
- **Accent (Primary):** `#2C3E50` (slate-blue, for links, hover states)
- **Accent (Hover):** `#C05C3E` (warm rust, subtle but warm, for link hover + active states)
- **Border/Divider:** `#E8E8E5` (very light gray)

**Dark Mode:**
- **Background:** `#0F0F0E` (near-black with slight warmth)
- **Surface:** `#1A1A18` (dark slate for cards/contact sections)
- **Text Primary:** `#F5F5F0` (off-white with warmth)
- **Text Secondary:** `#A0A09D` (medium-light gray for metadata)
- **Accent (Primary):** `#B8C6DB` (desaturated blue, maintains link identity)
- **Accent (Hover):** `#D4956F` (warm rust, same warmth as light mode)
- **Border/Divider:** `#2A2A28` (very dark gray)

**Contrast Ratios:**
- Primary text on background: 15:1+ (exceeds WCAG AAA)
- Secondary text on background: 8:1+ (exceeds WCAG AA)
- Links on background: 7.5:1+ (WCAG AAA)

### Typography

**Font Stack:**
- **Serif (Headings):** `"Merriweather", "Georgia", serif` — warm, readable serif with scholarly weight
- **Serif (Body):** `"Merriweather", "Georgia", serif` — differentiated only by weight/size, not family
- **Monospace (Code blocks if needed):** `"Fira Code", "Courier New", monospace`

**Type Scale & Weights:**
| Element | Size | Line-Height | Weight | Use |
|---------|------|------------|--------|-----|
| H1 | 48px | 1.2 | 500 | Page title (name) |
| H2 | 28px | 1.3 | 600 | Section headers |
| H3 | 20px | 1.4 | 500 | Publication title, subsection |
| Body | 16px | 1.6 | 400 | Prose, publication details |
| Small | 14px | 1.5 | 400 | Metadata, dates, role |
| Label | 12px | 1.4 | 600 | Platform labels (if shown) |

**Letter Spacing:** Default (0). No artificial tracking.

### Spacing & Rhythm

**Base Unit:** 8px incremental scale (4px fine-tuning allowed)

| Layer | Px | Example |
|-------|-----|---------|
| Tight | 8–12 | Line spacing adjustments, icon spacing |
| Medium | 16– 24 | Paragraph margins, card padding |
| Generous | 32–48 | Section gaps, margins around main content |
| Extreme | 64–96 | Top margin of viewport, bottom padding before footer |

**Single-Column Layout:**
- Max content width: 700px (comfortable reading line-length ~65–75 chars)
- Horizontal margins: 20px (mobile), 40px (desktop)
- Vertical margin above H2: 32px
- Vertical margin after H2: 16px
- Vertical gap between major sections: 64px (breathing room)

### Shadows & Depth

**Philosophy:** No shadows in light mode (flat, minimal). Dark mode uses subtle depth to separate surfaces.

**Shadow scale:**
- None (light mode default)
- Dark mode surface elevation:
  - Subtle: `0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24)`
  - Contact/link cards: `0 3px 6px rgba(0, 0, 0, 0.15), 0 2px 4px rgba(0, 0, 0, 0.12)`

### Effects & Decoration

**Explicitly Forbidden:** gradients, blur, rounded corners on content containers, box-shadows in light mode, animations beyond hover states

**Hover/Focus States:**
- **Links:** Underline highlight on hover; color shift to rust accent
- **Navigation items:** Subtle opacity or background shift
- **Focus Ring:** 2px solid accent color (visible tap/keyboard target)

**Dividers:** Subtle horizontal line (`1px solid #E8E8E5` light / `1px solid #2A2A28` dark) between sections or before new content blocks if needed for breathing room

### Responsive Breakpoints

| Breakpoint | Usage |
|------------|-------|
| 375px | Mobile minimum |
| 768px | Tablet |
| 1024px+ | Desktop |
|  |  |

**Mobile Strategy:** Single column always. Generous vertical padding. No horizontal scroll. Touch-friendly link targets (min 44×44px).

**Typography on Mobile:** Base 16px preserved; no scaling-down. Headings scale proportionally (H1 36px, H2 22px, H3 18px on mobile).

---

## Aesthetic Implementation

### Layout Structure
**Single-Centered-Column:** Hero/name at top, then stacked sections (Research Interests, Research Goals, Publications, News, Education, Experience, Skills, Misc). Max content width 700px, centered on desktop with 40px side margins. Mobile: full width with 20px margins. Vertical rhythm dominates; no sidebars, no grids, no multi-column layouts.

### Surface Treatment
**Light Mode:** Flat, no depth. `#FFFFFF` sections for contact/social links (subtle `#E8E8E5` border if needed to show grouping, not elevation).  
**Dark Mode:** `#1A1A18` surfaces for grouped content (contacts, social) with subtle shadow to show layering.

### Typography Expression
**Serif throughout:** Headings 600 weight, body 400. Clear hierarchy via size scale (H1 48px down to small 14px), not font family switching. All serif = scholarly, consistent, traditional. Weight contrast carries hierarchy.

### Decorative Rules
- **Allowed:** Horizontal divider lines (subtle, between sections), underlines on link hover, focus rings (2px)
- **Forbidden:** Shadows (light mode), gradients, rounded corners, blur, excessive color (limit to primary + secondary + accent), animation beyond hover/focus states

### Spatial Rhythm
**Airy & Scholarly:** Extreme whitespace around sections. 64px gaps between major section clusters. Generous top/bottom padding throughout. Publications and news items breathe independently — not cramped into cards or grids. Density: low-to-medium per section, never cramped.

### Signature CSS
1. **Serif Typography Commitment** — `font-family: 'Merriweather', Georgia, serif;` across all text, weight differentiation for hierarchy
2. **Generous Margins & Line-Height** — `margin-top: 64px`, `line-height: 1.6` for body, creating scholarly spaciousness
3. **Flat, Colorless Surfaces** — No shadows in light mode, no border-radius, no gradients; color change only on dark mode surfaces
4. **Link Underline on Hover** — `text-decoration: underline; color: var(--accent-hover)` triggers on `:hover` + `:focus-visible`
5. **Centered Max-Width** — `max-width: 700px; margin: 0 auto;` with side padding, single-column always

---

## Dark Mode Implementation

- **Toggle Button:** Top-right corner, sun/moon icon, 24×24px, accessible
- **Storage:** `localStorage.setItem('theme', 'dark' | 'light')`
- **CSS Variables:** All colors use `var(--bg-primary)`, `var(--text-primary)`, etc.
- **System Preference:** Initial load respects `prefers-color-scheme: dark`
- **Smoothness:** Transitions via `transition: background-color 200ms ease-in-out` on `html` element
