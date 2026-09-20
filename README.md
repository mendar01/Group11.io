# Financial Inequality — EAP Group Presentation

A ready-to-present slide deck for an **EAP (English for Academic Purposes)** group presentation on **financial inequality**.
Built for the assignment brief: 4 speakers · 6–8 slides · 15–20 minutes · verified sources · topic vocabulary.

## Contents

```
index.html                       → the presentation (single file, no dependencies)
handouts/speaker-notes.md        → full scripts + timing plan per speaker
handouts/vocabulary.md           → 30 topic terms + academic phrases + pronunciation
handouts/references.md           → every figure with its source
handouts/peer-feedback.md        → feedback sheet based on the assessment criteria
.github/workflows/deploy.yml     → automatic publishing to GitHub Pages
```

## Slide plan (8 slides, 18 minutes)

| Slide | Content | Speaker |
|-------|---------|---------|
| 1 | Title, team, topic and roadmap | Speaker 1 |
| 2 | Income vs. wealth vs. economic inequality; how it is measured | Speaker 1 |
| 3 | The data: 52% / 8.5% global income, US wealth distribution | Speaker 2 |
| 4 | Causes: technology, bargaining power, capital returns, inheritance | Speaker 3 |
| 5 | Effects: economic, social, political + counter-argument | Speaker 3 |
| 6 | Solutions: four policy levers | Speaker 4 |
| 7 | Conclusion and prepared Q&A | Speaker 4 |
| 8 | References | all |

## How to open the presentation

**Locally:** double-click `index.html` — it opens in any browser. No internet connection is needed (fonts fall back to system fonts, all charts are built with CSS).

**Controls:**

| Key | Action |
|-----|--------|
| `→` `↓` `Space` | next slide |
| `←` `↑` | previous slide |
| `F` | fullscreen |
| `N` | show/hide speaker notes |
| `Home` / `End` | first / last slide |
| swipe | navigate on a tablet |

**Print / PDF:** `Ctrl+P` → *Save as PDF* → the CSS prints one slide per page, without the controls.

## Publishing it on GitHub Pages

```bash
# 1. create an empty repository on GitHub (e.g. eap-financial-inequality) — do NOT add a README
git init
git add .
git commit -m "EAP presentation: financial inequality"
git branch -M main
git remote add origin https://github.com/<your-username>/eap-financial-inequality.git
git push -u origin main
```

Then in the repository: **Settings → Pages → Source: GitHub Actions** (this repository already contains the workflow file).
After the first push, the deck appears at `https://<your-username>.github.io/eap-financial-inequality/`.

*Alternative without Actions:* Settings → Pages → Source: *Deploy from a branch* → select `main` and `/root`. Both `index.html` and the `handouts/` folder will then be published.

## Editing tips

- **Names and group number** — slide 1, the four `.member` blocks, and the first line of `handouts/speaker-notes.md`.
- **Colours** — the `:root` variables at the top of `index.html` (`--accent`, `--accent-2`, `--gold`).
- **Charts** — each bar is a `div.bar-fill` with an inline `width`. Change the width *and* the neighbouring `.bar-val` text together.
- **Adding a slide** — copy one `<section class="slide">…</section>` block and add a matching string to the `notes` array at the bottom of the file.

## Sources

World Inequality Report 2022 (WID.world) · World Bank Poverty and Inequality Platform · OECD *Society at a Glance 2024*, *A Broken Social Elevator?* (2018), *Taxation and Inequality* (2024) · U.S. Federal Reserve Survey of Consumer Finances 2022 · UBS *Global Wealth Report 2024* · Oxfam *Inequality Inc.* (2024) · IMF *Fiscal Monitor: Tackling Inequality* (2017).

Full citations with the exact figure each source supports: `handouts/references.md`.
