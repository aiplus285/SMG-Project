# SMG Project — East Pattaya Villa Development Configurator

An interactive, single-file investor configurator built from the "Investment
Recommendation — Family Housing Development, East Pattaya" report (24 Aug 2026,
prepared for the Investment Committee).

**⚠️ Access note:** the live site sits behind a client-side password screen
(password shared separately). This is a soft gate for casual visitors only —
it is **not real security**. The page source, including the password check and
all report-derived figures, is fully visible in this public repository and in
the deployed page's HTML/JS. Do not rely on this for protecting genuinely
sensitive data.

## What it does

**Part 1 — Investment Committee Parameters** (left column): exposes the six
open questions from Section 7 of the report as adjustable inputs — confirmed
land parcel size, distance to the Highgate campus gate, ownership structure,
target sales velocity/hold period, all-in budget ceiling, target margin/IRR,
launch approach (phased vs. simultaneous), and contractor/developer tier. An
"Advanced" section adds two extra levers beyond Section 7: total unit count
and price-positioning target.

**Part 2 — Recommended Configuration** (right column): recomputes instantly,
with no submit button, using a deterministic rules engine — not a generative
or AI-driven output. Every constant (unit type specs, price bands, the
30/14/6 mix ratio, the 30–35% common-area allowance, the phasing logic) is
sourced directly from Sections 2, 3, 5, and 6 of the report. The one
quantity not in the source report — an illustrative all-in construction cost
per sqm, used only for the budget/margin sanity check — is explicitly labeled
as an assumption in the UI.

Outputs: recommended unit mix table, estimated GDV, land-utilization check,
budget/margin feasibility flags, a walking-distance marketing-claim flag, a
contractor-tier consistency flag, a generated phasing plan, a market-gap
positioning narrative (vs. the comparable set in Section 2), and an
ownership-structure buyer-pool impact note.

## Tech

Single self-contained `index.html` — no build step, no external dependencies,
no CDNs, no backend. Works fully offline.

## Status

Preliminary concept & positioning tool — for internal discussion only.
Figures are indicative and require validation via a full feasibility study.
