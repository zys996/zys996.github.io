# Design Context & System — Yusong Zhu Homepage

**Date:** 2026-04-08  
**Reference:** Skipped by user  
**Visual Direction:** UT Austin warm minimal
**Aesthetic Choice:** Soft Technical Editorial
**Target Output:** `index.html`

---

## Design Context

### Users
Theoretical computer science and machine learning faculty, collaborators, researchers, students, and prospective academic contacts looking for a quick understanding of Yusong Zhu's work on generative models, advisors, publications, teaching, and service.

### Brand Personality
**Three words:** Precise, Thoughtful, Rigorous

**Voice & Tone:** Academic and clear, but not stiff. The page should feel current and carefully organized without drifting into startup aesthetics.

**Emotional Goals:** Communicate mathematical rigor, curiosity, and intellectual depth. Make work on the theoretical foundations, sampling, evaluation, and auditing of generative models approachable and easy to scan.

### Aesthetic Direction
**Soft Technical Editorial** within a **warm minimal** frame. The page should use paper-like neutrals, UT Austin burnt orange, crisp dividers, restrained motion, and quietly structured surfaces. It should feel like a concise research index translated into an editorial homepage: calm, legible, and modern.

This aesthetic should avoid glossy product-marketing language and flat, generic portfolio grids. The intended effect is an intentional academic system rather than a template personal site.

### Design Principles
1. **Faithful Content Rendering** — Treat `homepage.md` as the content source of truth; styling should reveal its structure without changing biographical or publication facts.
2. **Structured Reading** — Present research areas, publication records, news, education, teaching, and professional service in clear semantic patterns.
3. **Quiet Interfaces** — Use minimal ornament with enough framing to feel intentional: hairlines, cool surfaces, and subtle depth.
4. **Academic Utility** — Make the advisor names, research focus, email address, paper links, and publication venues easy to find.
5. **Responsive Discipline** — Desktop can use a sidebar reading aid; mobile collapses to a strong single-column flow with no content loss.

---

## Design System

### Color Palette

**Light Mode**
- **Background:** `#f9f8f4`
- **Surface:** `#fffaf3`
- **Text Primary:** `#1d1a17`
- **Text Secondary:** `#665d54`
- **Accent:** `#bf5700`
- **Accent Soft:** `#f5e1d2`
- **Line:** `#d9cbbb`

**Dark Mode**
- **Background:** `#12100e`
- **Surface:** `#181412`
- **Text Primary:** `#f6ede3`
- **Text Secondary:** `#c7b8a7`
- **Accent:** `#ffb45c`
- **Accent Soft:** `#3a2415`
- **Line:** `#30271f`

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
- Warm neutral backgrounds instead of white/black extremes
- Hairline borders and low, diffuse shadow only on grouped surfaces
- Oversized name treatment with compact academic metadata
- Section labels in uppercase UI text with increased tracking
- Motion limited to reveal states, active navigation, and theme transitions

### Anti-Patterns To Avoid
- No purple-blue AI gradients
- No glassmorphism
- No repetitive card grid
- No giant hero metrics or generic startup badges
- No fully centered one-column layout on desktop

### Aesthetic Implementation

**Layout structure**
- Desktop: sticky left rail for identity, affiliation, research summary, email, and section navigation; scrollable main content on the right
- Mobile: single-column stack with the rail collapsing into a compact top introduction

**Surface treatment**
- Main content groups use `background: var(--surface)` with `border: 1px solid var(--line)`
- Border radius is restrained, with near-square editorial panels and rounded pills only where useful
- Shadows are subtle and broad, never glossy

**Typography expression**
- Large serif H1 for memorability
- Sans-serif UI labels, metadata, dates, and navigation
- Publication titles and institution names use medium-weight sans with tighter line-height than body text

**Decorative rules**
- Allowed: gridline borders, subtle radial background highlight, section anchors, timeline spine, and research-area chips
- Forbidden: decorative gradients on text, oversized iconography, noisy patterns, and unnecessary illustrations

**Spatial rhythm**
- Airy overall, but internally structured
- Large top offsets and section spacing
- Compact grouping inside publication records so the bibliography remains efficient to scan

**Signature CSS**
1. `background: radial-gradient(circle at top left, color-mix(in srgb, var(--accent) 10%, transparent), transparent 28%)`
2. `backdrop-filter: blur(10px)` is forbidden; surfaces rely on tint and linework instead
3. `border: 1px solid var(--line); box-shadow: 0 10px 28px rgba(61, 42, 28, 0.06)`
4. `font-family: "Fraunces", "Times New Roman", serif` on the H1 only, with cool sans-serif type elsewhere
5. A fixed desktop rail for continuous orientation, collapsing into the single-column mobile flow
