# Design Context & System — Yusong Zhu Homepage

**Date:** 2026-04-08  
**Reference:** Skipped by user  
**Visual Direction:** B. Cool minimal  
**Aesthetic Choice:** D. Soft Technical  
**Target Output:** `/Users/shishi/Documents/ZYS/index.html`

---

## Design Context

### Users
Faculty, collaborators, researchers, students, and recruiting teams looking for a fast understanding of Yusong Zhu's academic background, research themes, and publication history.

### Brand Personality
**Three words:** Precise, Thoughtful, Contemporary  
**Voice & Tone:** Academic and clear, but not stiff. The page should feel current and design-aware without drifting into startup aesthetics.  
**Emotional Goals:** Communicate rigor, curiosity, and visual intelligence. Make the research feel approachable and organized.

### Aesthetic Direction
**Soft Technical** within a **cool minimal** frame. The page should use cool-tinted neutrals, crisp dividers, restrained motion, and quietly structured surfaces. It should feel like a research dashboard translated into an editorial homepage: calm, legible, and modern.

This aesthetic should avoid glossy product-marketing language and avoid flat generic portfolio grids. The effect should be "designed systems thinking" rather than "template personal site."

### Design Principles
1. **Faithful Content Rendering** — Preserve the section order and wording from `homepage.md`; styling should reveal structure, not rewrite the story.
2. **Structured Reading** — Convert lists into clearer semantic patterns: timelines, publication records, badges, and academic entries.
3. **Quiet Interfaces** — Minimal ornament, but enough framing to feel intentional: hairlines, cool surfaces, and subtle depth.
4. **Academic Utility** — Navigation, typography, and scanning behavior should work for quick review as well as long reading.
5. **Responsive Discipline** — Desktop can use a sidebar reading aid; mobile collapses to a strong single-column flow with no content loss.

---

## Design System

### Color Palette

**Light Mode**
- **Background:** `#f3f6f8`
- **Surface:** `#fbfcfd`
- **Surface Strong:** `#eef2f5`
- **Text Primary:** `#13202b`
- **Text Secondary:** `#556472`
- **Accent:** `#2e5b7a`
- **Accent Soft:** `#d9e7f2`
- **Line:** `#d6e0e7`

**Dark Mode**
- **Background:** `#0d1419`
- **Surface:** `#121d24`
- **Surface Strong:** `#17242d`
- **Text Primary:** `#edf4f8`
- **Text Secondary:** `#a4b6c3`
- **Accent:** `#8cb8d6`
- **Accent Soft:** `#1a3140`
- **Line:** `#263744`

### Typography
- **Display / Headings:** `"Fraunces", "Times New Roman", serif`
- **Body / UI:** `"Manrope", "Helvetica Neue", sans-serif`

**Scale**
- H1: `clamp(3rem, 7vw, 5.6rem)`
- H2: `clamp(1.4rem, 2vw, 1.9rem)`
- H3: `1.05rem`
- Body: `1rem`
- Small metadata: `0.9rem`

### Style & Effects
- Tinted neutral backgrounds instead of white/black extremes
- Hairline borders and low, diffuse shadow only on grouped surfaces
- Oversized name treatment with compact metadata
- Section labels in uppercase UI text with increased tracking
- Motion limited to reveal/active states and theme transitions

### Anti-Patterns To Avoid
- No purple-blue AI gradients
- No glassmorphism
- No repetitive card grid
- No giant hero metrics or generic startup badges
- No fully centered one-column layout on desktop

### Aesthetic Implementation

**Layout structure**
- Desktop: sticky left rail for identity + section navigation, scrollable main content on the right
- Mobile: single-column stack with the rail collapsing into a top intro block

**Surface treatment**
- Main content groups use `background: var(--surface)` with `border: 1px solid var(--line)`
- Border radius is restrained: `20px` for major groups, `14px` for smaller pills/items
- Shadows are subtle and broad, never glossy

**Typography expression**
- Large serif H1 for memorability
- Sans-serif UI labels, metadata, dates, and navigation
- Publication titles and institution names use medium-weight sans with tighter line-height than body text

**Decorative rules**
- Allowed: gridline borders, subtle radial highlight in background, section anchors, timeline spine, pill chips
- Forbidden: decorative gradients on text, oversized iconography, noisy patterns, unnecessary illustrations

**Spatial rhythm**
- Airy overall, but internally structured
- Large top offsets and section spacing
- Compact grouping inside records so lists feel efficient rather than sparse

**Signature CSS**
1. `background: radial-gradient(circle at top left, color-mix(in oklab, var(--accent) 14%, transparent), transparent 32%)`
2. `backdrop-filter: blur(10px)` is forbidden; surfaces rely on tint and linework instead
3. `border: 1px solid var(--line); box-shadow: 0 18px 50px rgba(17, 32, 43, 0.08)`
4. `font-family: "Fraunces", "Times New Roman", serif` on the H1 only, with cool sans system elsewhere
5. `position: sticky; top: 2rem` on the desktop rail for continuous orientation
