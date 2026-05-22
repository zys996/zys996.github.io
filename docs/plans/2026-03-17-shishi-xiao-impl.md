# Implementation Plan — Shishi Xiao Homepage

**Date:** 2026-03-17  
**Source:** Design System (2026-03-17-shishi-xiao-design.md)  
**Deliverable:** `/Users/shishi/Documents/ZYS/index.html` (single-file self-contained)

---

## Task Breakdown

### Phase 1: HTML Structure
- [ ] 1.1 Create semantic HTML5 structure with lang attribute, proper meta tags (viewport, charset, description)
- [ ] 1.2 Build centered single-column container (max-width: 700px, margin: 0 auto)
- [ ] 1.3 Create header with name (H1) and intro paragraph
- [ ] 1.4 Nest all page sections (Research Interests, Research Goals, Publications, News, Education, Experience, Skills, Misc) as `<section>` elements
- [ ] 1.5 Render Publications list from page-story: each publication as article element with title (H3), authors, conference/journal
- [ ] 1.6 Render News list (dates + events) as timeline/chronological list
- [ ] 1.7 Render Education list with institution, degree, dates
- [ ] 1.8 Render Research Experience list with role, dates, advisor, bullet points
- [ ] 1.9 Render Skills as comma-separated list or subtle badges
- [ ] 1.10 Render Misc section (Creative work list)

### Phase 2: CSS — Core Styling
- [ ] 2.1 Define CSS custom properties for all colors (light & dark mode variants):
  - `--bg-primary`, `--bg-surface`
  - `--text-primary`, `--text-secondary`
  - `--accent-primary`, `--accent-hover`
  - `--border-color`
- [ ] 2.2 Set default light mode on `:root`
- [ ] 2.3 Create dark mode variant with `html[data-theme="dark"]`
- [ ] 2.4 Apply base styles: `font-family: 'Merriweather', Georgia, serif`, base font-size 16px, line-height 1.6
- [ ] 2.5 Set body background, text color using CSS variables
- [ ] 2.6 Define typography scale (H1 48px, H2 28px, H3 20px, body 16px, small 14px)
- [ ] 2.7 Apply weight hierarchy (H1/H2: 600, H3/labels: 500, body: 400)
- [ ] 2.8 Set line-heights: headings 1.2–1.4, body 1.6, small 1.5
- [ ] 2.9 Remove default margins where needed, apply custom spacing (margin-top: 64px for sections, margin-top: 32px for H2, margin-bottom: 16px for H2)

### Phase 3: CSS — Spacing & Layout
- [ ] 3.1 Center single column container with `max-width: 700px`, `margin: 0 auto`
- [ ] 3.2 Apply horizontal padding: 40px (desktop), 20px (mobile, @media max-width 768px)
- [ ] 3.3 Add vertical padding/margin: top 96px, bottom 96px (breathing room above/below content)
- [ ] 3.4 Define section gap: 64px vertical margin-top for each `<section>`
- [ ] 3.5 Publications/News/Education items: 24px margin-bottom between items
- [ ] 3.6 Groups (Research Experience roles, Skills, etc.): 16px gap
- [ ] 3.7 Divider lines between major sections (subtle 1px border-top): apply if visual grouping feels needed

### Phase 4: CSS — Links & Interactive States
- [ ] 4.1 Style `<a>` default: inherit color from text hierarchy, no underline
- [ ] 4.2 `:hover` state: add underline, shift color to `var(--accent-hover)`
- [ ] 4.3 `:focus-visible` state: 2px solid focus ring in `var(--accent-primary)`
- [ ] 4.4 Ensure all links meet 7.5:1 contrast ratio with background
- [ ] 4.5 Social/icon links (when rendered as SVGs): inherit color, scale 1.1 on hover

### Phase 5: CSS — Dark Mode Toggle
- [ ] 5.1 Create toggle button HTML in header (sun icon / moon icon, positioned top-right)
- [ ] 5.2 Style button: 24×24px, transparent background on hover, accessible focus ring
- [ ] 5.3 JavaScript: toggle `html[data-theme]` attribute on click
- [ ] 5.4 JavaScript: persist theme choice to `localStorage` (key: 'theme')
- [ ] 5.5 JavaScript: on page load, check `localStorage`, then fall back to `prefers-color-scheme`
- [ ] 5.6 CSS: Add `transition: background-color 200ms ease-in-out, color 200ms ease-in-out` on `html` for smooth theme switch

### Phase 6: Rendering Conventions
- [ ] 6.1 Publications: render as unordered list or stacked blocks; each with title (link if available), authors, venue/year
- [ ] 6.2 News timeline: chronologically ordered (newest first); format: "**Month Year** – Event description"
- [ ] 6.3 Education: start + end year on same line as degree; institution as heading
- [ ] 6.4 Experience: role + institution + dates; bullet descriptions; advisor mention
- [ ] 6.5 Social links (if provided): render as inline icon-based links using SVG (no text, icon links only)
- [ ] 6.6 Skills: render as simple comma-separated list if minimal; consider subtle badges with consistent styling

### Phase 7: Responsive Design
- [ ] 7.1 Add viewport meta tag: `width=device-width, initial-scale=1, maximum-scale=5`
- [ ] 7.2 No horizontal scroll at 375px or 1200px
- [ ] 7.3 Mobile breakpoint (max-width: 768px): reduce H1 to 36px, H2 to 22px, H3 to 18px; padding 20px
- [ ] 7.4 Test: content reflows naturally, no text truncation, links easily tappable (44×44px minimum)
- [ ] 7.5 Tablet (768–1024px): intermediate sizing/spacing
- [ ] 7.6 Desktop (1024px+): full 40px side padding, comfortable reading

### Phase 8: Accessibility
- [ ] 8.1 Semantic HTML: use H1–H6 sequentially, no skips; `<section>`, `<article>`, `<nav>` tags where appropriate
- [ ] 8.2 Form elements: all interactive elements have visible `:focus-visible` states
- [ ] 8.3 Color contrast: verify 4.5:1 for normal text, 3:1 for large text in both modes
- [ ] 8.4 Alt text: (if images present) all meaningful images have descriptive alt text
- [ ] 8.5 Links: all links have descriptive text (no "click here"); underline on focus/hover visible
- [ ] 8.6 Skip navigation (optional but good): skip to main content link for keyboard users
- [ ] 8.7 Reduced motion: wrap animations in `@media (prefers-reduced-motion: no-preference)` (theme transition only)
- [ ] 8.8 ARIA landmarks: main content inside `<main>` tag; footer in `<footer>`

### Phase 9: Validation & Polish
- [ ] 9.1 W3C HTML validation: no errors
- [ ] 9.2 CSS validation: no errors
- [ ] 9.3 Keyboard navigation: tab order matches visual order; all interactive elements reachable
- [ ] 9.4 Screen reader test (optional): headings, links, content structure sound logical
- [ ] 9.5 Visual balance: inspect margins, alignment, whitespace; ensure no empty regions unless intentional
- [ ] 9.6 Line length check: 65–75 characters per line in body text on desktop; verify readability
- [ ] 9.7 Aesthetic consistency: serif use consistent, no mixed fonts; color palette adhered to; no decorative excess

### Phase 10: Final Quality Pass (Polish + Audit)
- [ ] 10.1 Polish: alignment refinement, detail fixes, hover states feel smooth
- [ ] 10.2 Audit: accessibility compliance, performance (asset optimization if any), anti-patterns
- [ ] 10.3 Dark mode visual check: all elements visible, colors readable, no contrast failures
- [ ] 10.4 Mobile visual check: layout stable, no unexpected reflows, interactive elements functional
- [ ] 10.5 Performance: single HTML file, no external HTTP requests except fonts; CSS inlined or minimal

---

## Notes
- **Content Fidelity:** Render page-story sections in their original order and structure; no reordering or content removal
- **Serif Typography:** Merrieather font loaded via Google Fonts (CDN link in `<head>`)
- **Single-File Delivery:** All CSS inline in `<style>` tag, all JavaScript inline in `<script>` tag
- **No External Dependencies:** Except Google Fonts for Merriweather; all logic self-contained
