# Implementation Plan — Yusong Zhu Homepage

**Date:** 2026-04-08  
**Source:** `docs/plans/2026-04-08-yusong-zhu-design.md`  
**Deliverable:** `/Users/shishi/Documents/ZYS/index.html`

---

## Build Tasks

### 1. Semantic structure
- Create a single-file HTML document with proper metadata and accessible landmarks
- Preserve the section order from `homepage.md`
- Add a sticky desktop rail containing name, short intro, and section anchors

### 2. Structured rendering
- Render research interests as compact chips
- Render research goals as a numbered-looking vertical list
- Render publications as publication records with venue/year labels and author lines
- Render news as a vertical timeline
- Render education entries as institutional records
- Keep teaching inside the education section as a sub-block
- Render creative work as small pills

### 3. Styling system
- Implement light and dark themes with CSS custom properties
- Apply cool-tinted neutral backgrounds and bordered surfaces
- Use a serif-only H1 with sans-serif UI and body text
- Ensure three or more clear hierarchy levels

### 4. Interaction
- Add hover and focus-visible states to all links and buttons
- Add a theme toggle with localStorage persistence
- Add section-aware nav highlighting via IntersectionObserver
- Respect `prefers-reduced-motion`

### 5. Responsive behavior
- Use a two-column layout on larger screens and a single-column layout below tablet widths
- Verify no horizontal overflow at narrow widths
- Keep touch targets at least 44px for nav and theme controls

### 6. Quality pass
- Review against local `polish` guidance: spacing consistency, alignment, interaction states
- Review against local `audit` guidance: semantics, contrast, responsive stability, anti-pattern avoidance
