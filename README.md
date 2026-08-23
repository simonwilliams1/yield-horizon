# Yield Horizon

Marketing site for Yield Horizon — cost-of-capital benchmarking for European private equity and credit fund managers.

**Live site:** https://yieldhorizon.co.uk/

## What this repository contains

| File | Purpose |
|---|---|
| `index.html` | The entire website — all three views, styling, behaviour and images, in one self-contained file |
| `README.md` | This file. Description only; not part of the published site |
| `CNAME` | Created automatically by GitHub when a custom domain is set. Do not edit or delete |

## How the site is built

One file, no build step, no dependencies. All styling and behaviour is inside `index.html`. To make a change, edit that file and commit — GitHub Pages republishes automatically within a couple of minutes.

The site has three views:

- **Home** — the pitch: the ICC argument, the five cost components, delivery, pricing, and fit criteria
- **Methodology** — the full ClarityStack™ v1.2 calculation, including a plain-English glossary, the input schedule with sources, the component build, and the IC output block
- **About** — the practitioner: background, why the framework exists, and credentials

Switching between them is handled by CSS rather than JavaScript, so the site works with scripts disabled. JavaScript only adds the tabbed navigation on the methodology page and the bar animations; without it, all content still displays correctly.

Images — the logo mark, the footer lockup and the portrait — are embedded as base64 data URIs rather than separate files. That is why `index.html` is around 170KB. It means one file to deploy and nothing that can break a link, at the cost of a larger single request.

## Content source

Figures shown on the site come from `Yield_Horizon_ClarityStack_ICC_Calculator_v1_2.xlsx`, run on an illustrative EUR 500mm fund. That workbook is **not** stored in this repository.

If the model is revised, these figures must be updated in `index.html` to match:

- Marginal ICC: 868 bps
- Static hurdle comparison: 800 bps
- Component split: 727 / 63 / 0 / 18 / 59 bps
- Deal spread: +552 bps
- Drawn capital illustration: EUR 641,096 vs EUR 2,367,123
- Idle cash placement permission: worth 42 bps (net idle drag of 63 bps becomes 105 bps gross)

## Outstanding

The About view carries three bracketed placeholders awaiting real figures — search `index.html` for `add:`. They render in amber on the page so they cannot ship unnoticed:

- Number of funds and AUM covered by the Oaktree desk
- Currencies and jurisdictions
- Concurrent engagement capacity

## Publishing

Served by GitHub Pages from the `main` branch, root directory. The repository must remain public for free Pages hosting.

Because it is public, **do not commit** the ClarityStack workbook, client data, framework documents, or anything else not intended for publication.

## Local preview

Download `index.html` and open it in a browser. It runs fully offline.

---

ClarityStack™ is a proprietary Yield Horizon framework.
