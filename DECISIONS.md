# Decisions

## 2026-07-20 — Interaction direction: the receipt behaves like real paper
- **Decided:** All motion design mimics physical receipt paper — 3D tilt that
  leans to face the cursor with a soft spring wobble, a "bend" layer that
  flexes a beat behind the base, a shadow + surface sheen driven by the cursor
  as a light source, slight see-through paper (88% opaque + frosted blur),
  and a cursor trail of the receipt's own ornament glyphs.
- **Why:** The page is a keepsake, not a dashboard — physicality sells the
  receipt metaphor. Everything animates via moves of pre-rendered layers
  (transforms only), so text never re-renders / never shimmers.
- **Considered & rejected:**
  - Paper-texture WebGL shader (paper.design) — worked, but visually too
    heavy and pulled ~200KB of third-party code. Removed entirely.
  - "Trailing corners/edges" flimsiness via shear + edge flaps — read as 2D
    warping instead of 3D. Reverted to the spring, tuned weaker.
  - Emoji for the ornaments/trail — inconsistent across devices; replaced
    with monochrome unicode glyphs (≈ ✻ ☼ ❀ ☾ ✶ ❋).

## 2026-07-20 — Host on GitHub Pages instead of a Claude Artifact
- **Decided:** Self-host the receipt page in Samantha's own GitHub account via
  GitHub Pages, so she can tweak the file directly.
- **Why:** Ownership and hand-editability mattered more than instant hosting.
- **Considered & rejected:** Claude Artifact hosting — worked, but it blocks
  outside downloads, forcing a font swap and a rebuilt chart, and the file
  lives on claude.ai rather than in her repo. The original file (Geist Mono +
  Chart.js) works unmodified on GitHub Pages.
