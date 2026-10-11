# GTO Labs — leaf site

`gto.okinent.org` — the GTO Labs leaf of hub.okinent.org.

## The shape this belongs to

- **hub** — `hub.okinent.org` (`BigBossRabbit/the-hub`): brand, navigation, the two doors (business /
  Bitcoin). Never a dependency.
- **leaves** — one repo per arm, own CNAME, same tokens and same scroll language. A leaf must stand
  alone; if it needs the hub to make sense, the split was wrong.
  - leaf #1 `bitcoin.okinent.org` — `easysats-site` (reference build)
  - leaf #2 `gto.okinent.org` — **this repo**

## The scroll language is LEAF

Dark `#0a0c08`, ink `#e8e4d8`, gold `#c9a84c`, Georgia serif, content that arrives as you travel.
Reference implementation: `ObsidianVault/Legion/reference/LEAF-scroll-story.html` (the original Mac
one-pager). Engine rules in `index.html`:

1. **Immediate pass** — anything already in the viewport is shown on load (no frame needed).
2. **IntersectionObserver** — progressive reveal while travelling; unobserves once done.
3. **Safety timer (1.5s)** — reveals whatever is left, always. A blank page is worse than no animation.

`prefers-reduced-motion` short-circuits all of it. Keyboard travel (`j`/`k`/arrows) jumps section to
section.

## Deploy

Static, single file. GitHub Pages from `main`, CNAME already present, `.nojekyll` so nothing is
processed. No build step, no dependencies.

## Content rule

Everything on the page traces to `ObsidianVault/BusinessOpportunities/GTOLabs_Structure_Brief_2026-09-28_v2.html`
and `Legion/Spawn/training/GTO-LABS-CONTEXT.md`. If a claim is not in those, it does not go on the site.
