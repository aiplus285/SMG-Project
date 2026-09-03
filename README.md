# SMG Project — East Pattaya Villa Development Configurator

An interactive, single-file investor configurator built from the "Investor
Recommendation — Revised, 50-Unit Family Villa Development, East Pattaya" report
(Update 3, August 2026 — land ownership and site location confirmed).

**⚠️ Access note:** the live site sits behind a client-side password screen
(password shared separately). This is a soft gate for casual visitors only —
it is **not real security**. The page source, including the password check and
all report-derived figures, is fully visible in this public repository and in
the deployed page's HTML/JS. Do not rely on this for protecting genuinely
sensitive data.

## What it does

Three numbered sections, top to bottom:

**1. Parameters** — the decision levers still open after Update 3: unit-mix
positioning, ownership structure, target sales velocity/hold period,
construction budget ceiling (land excluded — already owned), target
margin/IRR, launch approach (phased vs. simultaneous), contractor/developer
tier, total unit count, and the corporate/expat rental-demand check (family
size, monthly housing budget, assumed rental yield). Two parameters from the
prior version were **removed** because the report resolved them: confirmed
land parcel size (the site is owned, ≈65–75 rai available against the
≈23–25 rai this mix needs) and distance to the Highgate campus gate (confirmed
≈320–450m, a genuine walking distance) — both now shown as static, sourced
facts instead of sliders.

**2. Executive Summary** — total units, est. GDV, blended avg. price, and
implied margin, plus a Market-Demand Fit score and a Profitability-at-a-glance
bar, both recomputing live.

**3. Details of Results** — recomputes instantly, with no submit button,
using a deterministic rules engine, not a generative or AI-driven output.
Every constant (the four unit tiers — Signature, Estate, Family,
Corporate-Ready — their price bands, the report's own 6/5/20/19 base-case
mix, the 30–35% common-area allowance, the phasing logic) is sourced directly
from the Update 3 report. The one quantity not in the source report — an
illustrative construction cost per sqm, used for the budget/margin check — is
explicitly labeled as an assumption in the UI, as is the fact that
site-clearing for this raw, forested land is not yet costed.

Outputs: the Demand–Offer Match score and its full factor breakdown, the
recommended unit mix table, a budget/cost/margin chart, feasibility flags, a
**Key Risks & Decisions Needed** card (land survey, the unidentified
neighboring compound, an on-site waterway, cost quotes, ownership structure,
and pricing headroom — lifted from the report's own risk list), the market
positioning map and benchmark table (11 corridor comparables), a revenue-mix
chart, a generated phasing plan, and the corporate/expat housing-budget
affordability table.

## Tech

Single self-contained `index.html` — no build step, no external dependencies,
no CDNs, no backend. Works fully offline.

## Status

Preliminary concept & positioning tool — for internal discussion only.
Figures are indicative and require validation via a full feasibility study.
