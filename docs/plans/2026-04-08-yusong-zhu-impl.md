# Implementation Plan — Yusong Zhu Homepage

**Date:** 2026-04-08  
**Source:** `docs/plans/2026-04-08-yusong-zhu-design.md`  
**Content Source:** `homepage.md`

**Deliverable:** `index.html`

---

## Build Tasks

### 1. Semantic structure
- Create a single-file HTML document with accurate metadata and accessible landmarks
- Use `homepage.md` as the source of truth for biography, research areas, publications, news, education, and teaching
- Add a sticky desktop rail containing the name, UT Austin affiliation, research summary, email and academic-profile links, and section anchors

### 2. Structured rendering
- Render generative model theory, sampling, model evaluation and auditing, and high-dimensional statistics interests as compact chips
- Render publications as records with title, venue or preprint status, year, author line, and paper link
- Visually distinguish conference papers from arXiv preprints without implying a different publication status
- Render news as a vertical timeline
- Render the current UT Austin Ph.D., Tsinghua software engineering B.S., and statistics minor as academic records
- Keep teaching and professional service as separate compact sections

### 3. Styling system
- Implement light and dark themes with CSS custom properties
- Apply warm paper-like neutrals, UT Austin burnt orange, and bordered surfaces
- Use a serif-only H1 with sans-serif UI and body text
- Ensure at least three clear hierarchy levels

### 4. Interaction
- Add hover and focus-visible states to all links and buttons
- Add a theme toggle with `localStorage` persistence
- Add section-aware navigation highlighting via `IntersectionObserver`
- Respect `prefers-reduced-motion`

### 5. Responsive behavior
- Use a two-column layout on larger screens and a single-column layout below tablet widths
- Verify no horizontal overflow at narrow widths
- Keep touch targets at least 44px for navigation and theme controls
- Preserve readable wrapping for long paper titles and author lists

### 6. Content verification
- Confirm the introduction identifies Yusong Zhu as a UT Austin Computer Science Ph.D. student advised by Kevin Tian and Eric Price
- Confirm the contact address is `zhuys@utexas.edu`
- Confirm the Google Scholar profile, education dates, teaching history, and reviewer service against `homepage.md`
- Confirm all five publication titles, authors, venues or preprint labels, years, and paper URLs against `homepage.md`
- Ensure metadata describes the theoretical foundations, sampling, evaluation, and auditing of modern generative models accurately

### 7. Quality pass
- Review against local `polish` guidance for spacing consistency, alignment, and interaction states
- Review against local `audit` guidance for semantics, contrast, responsive stability, and anti-pattern avoidance
