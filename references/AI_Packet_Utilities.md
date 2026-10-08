# AI Stock Review Packet: Utilities

**Version 2.3.0 — Last updated 2026-10-08.** Supersedes v2.2.4. v2.3.0 adds branch routing: Branch A (regulated utilities — unchanged analytical behavior for identical evidence) and Branch B (competitive generation and retail — independent power producers, merchant fleets, competitive retail) with its own metrics, pillar decision rules, red flags with escalation conditions, weights, expectations adaptation, and a companion procedures file (`merchant_power_procedures.md`); scopes regulated-only sections to Branch A; rewrites the shared evidence-for-ratings rule and the score-change rule. v2.2.4 adds one shared expectations-module sentence: where a sector packet defines an expectations adaptation, it governs the variables solved for and the value split (Banks and Insurers now define one). v2.2.3 adds the expectations-embedded valuation module: the universal expectations test (reverse-solve the price for required growth, margin, reinvestment and discount rate), the proven-vs-unproven enterprise-value split with its valuation-pillar caps, and the "Estimated — expectations-implied" sub-label. v2.2.2 adds the weak-on-current-evidence conclusion category. v2.2.1 extends the v4 provenance labels (adds Calculated — verified inputs and Not disclosed; Severe-flag caps require verified evidence). Supersedes v2.1: upgraded from a general sector guide to a strict execution file (v4 verification and provenance standard, regulatory and leverage disambiguation, payout-definition rules, holdco/opco rules, scoring and audit-trail rules). Educational framework — not investment advice. No buy/sell/hold language.

*Branch A: electric, gas, water — rate-regulated. Branch B: competitive generation and retail.* — GICS: Utilities (Electric, Gas, Water, Multi-Utilities, Independent Power and Renewable Electricity Producers)

**Core principle: Verified does not mean Positive.** Verification proves the number is real; the sector thresholds and the trend determine the rating. A verified FFO/debt of 12% is still Watch. A verified payout of 88% of EPS is still Watch-to-Negative.

## Prompt

> Analyze [company name / ticker] using the uploaded Core Framework and this Utilities guide.
> Do not use buy/sell/hold language.
> Provide: 1. Business model summary · 2. Route (Branch A / Branch B / both) with the merchant vs regulated share and its basis · 3. Peer group with rationale · 4. Key metrics for the branch with provenance labels · 5. Values vs peers and 5-year history · 6. Positive/Watch/Negative assessment · 7. Severe red flags, if any · 8. Valuation (Branch A: P/E vs rate-base growth, yield spread, FFO/debt; Branch B: forward-curve and normalized cash-flow cases) · 9. Data confidence: High/Medium/Low · 10. Neutral research conclusion: strong on current evidence / mixed, needs more evidence / weak on current evidence / high-risk, special situation / insufficient data.
> Use primary sources (10-K, 10-Q, earnings releases, rate-case filings, regulatory orders, credit-agency reports; for Branch B also hedge disclosures and ISO/RTO market reports). Do not rely only on screeners or summaries.

## Routing and branch scope

State the route before scoring anything. Measure the share of **normalized operating earnings** that comes from competitive generation, wholesale trading, and competitive retail (merchant share) versus rate-regulated operations (regulated share). Use consistently scoped operating profit; use reconciled segment adjusted EBITDA only when operating profit is unavailable or demonstrably distorted (hedge mark-to-market, impairments, acquisition effects, corporate allocations). State the period, the source, and every adjustment. Non-positive or unstable denominators require a disclosed classification judgment, not mechanical percentages.

| Merchant share | Route |
|---|---|
| > 50% | **Branch B dominant** — Competitive generation and retail |
| < 50% | **Branch A dominant** — Regulated utilities |
| exactly 50% | No dominant branch — score both and blend |

The dominant branch leads the dashboard and the conclusion narrative; it does not change the blend.

**Both branches are scored whenever each represents ≥ 20% of normalized operating earnings**, whichever dominates. Below 20%, the minor share is not scored as a branch, but a material-risk override applies: collateral exposure, parent guarantees, or funding support for that business are still assessed as red flags — a small earnings contribution does not make them immaterial. A reported segment that mixes merchant and regulated activity (e.g., "Power & Other") is not a merchant share until the merchant operations are isolated; if they cannot be, state the sensitivity of the route to that uncertainty.

**Blending (when both branches are scored):** consolidate using estimated segment EV shares — a framework convention shared with the Health Technology packet, not a claim that EV weighting is universally superior. Disclose each segment's valuation method, the allocation of corporate costs and liabilities, and whether the conclusion category changes if the weights shift by ±10 points. Never back the segment split out of the company's current aggregate market value. If reliable shares cannot be established, report the two branch scores separately and conclude **mixed, needs more evidence** without forcing a consolidated percentage. Assess parent liquidity, guarantees, and structural subordination at group level; apply any qualifying group Severe cap after blending. The segment-EV method is in `merchant_power_procedures.md` (section 6).

**Scope of this packet's sections:** shared sections — provenance labels, the verification standard and the four shared rules, debt definition and holdco/opco rules, payout-basis rule, score-change audit trail, data confidence, conclusion template — apply to both branches. Sections marked **(Branch A)** apply to regulated earnings only. Branch B uses its own section, which replaces the Branch A metrics, valuation logic, dashboard, verification priorities, red flags, weights, and checklist. "Branch A unchanged" means unchanged analytical behavior and weights for identical evidence. Applying Branch A thresholds to Branch B earnings, or the reverse, is a routing error.

## Sector context (Branch A)

Bought for stable dividends, not growth. Regulators cap returns, so the story is dividend safety, rate-base growth, regulatory quality, and debt cost. Heavy regulated capex makes free cash flow look weak — that can be fine, because regulators allow a return on that spending. Always state the regulated/unregulated earnings mix before applying regulated-utility thresholds.

## Key metrics & rule-of-thumb ranges (Branch A)

| Metric | Positive | Watch | Negative | How to read it |
|---|---|---|---|---|
| **EPS / rate-base growth** | 5–7% | 3–5% | < 3% | Steady mid-single-digit growth is normal and fine. |
| **Allowed ROE & earned vs allowed** | Earning ≥ allowed (~9–10%) | Small gap | Persistent shortfall | A persistent gap signals regulatory lag or poor cost control. |
| **Dividend yield** | 3–5% | 2–3% or > 6% | Cut risk | A very high yield is the market pricing a possible cut. |
| **Payout ratio (state basis)** | 50–70% of EPS | 70–85% | > 90% | Above ~90% leaves little cushion. State EPS vs cash-flow basis. |
| **FFO / debt** | > 15% | 10–15% | < 10% | The credit-agency lens; below ~10% pressures the rating. |
| **Debt/EBITDA** | < 5x | 5–6x | > 6x | Higher leverage is normal here, but watch the trend. |
| **Interest coverage** | > 3x | 2–3x | < 2x | Critical given heavy debt loads. |
| **Fixed vs floating debt** | Mostly fixed, laddered | Some floating | Heavy floating / near-term wall | Rate spikes hit floating-rate borrowers immediately. |

**Formulas:** FFO/debt = funds from operations (cash flow before working capital) ÷ total debt — note credit agencies apply their own adjustments (leases, hybrids, pensions); state whose definition. Payout ratio = dividends per share ÷ EPS (state GAAP vs adjusted/operating EPS), or dividends ÷ FFO for the cash-flow basis. Rate base = the asset base on which the regulator allows the utility to earn a return. Allowed ROE = the return the regulator authorizes in rate cases. Earned ROE = the return actually achieved on regulated equity. Regulatory lag = delay between spending money and recovering it in rates. Interest coverage = EBITDA (or EBIT — state which) ÷ interest expense.

## Provenance labels (v4 standard)

Every key metric carries exactly one label. The label reflects what the review itself verified, not how plausible the number is:

| Label | Meaning |
|---|---|
| **Verified** | The review itself directly read the source document and quotes the exact label next to the value |
| **Calculated — verified inputs** | Derived by a stated, reproducible formula whose inputs are each individually Verified. Derived ratios (FCF margin, coverage ratios, EV multiples) are never plain "Verified" |
| **User-provided filing excerpt** | The user pasted verbatim filing text containing the label and value; usable for rating decisions with provenance stated, but not "Verified" |
| **Reported, pending direct verification** | The value came from another AI, an evaluator, a search summary, a secondary source, or a relayed table |
| **Estimated** | Derived from market data, aggregators, or calculation with unverified or mixed inputs; "Estimated proxy" is its sub-type |
| **Needs verification** | An important metric not found or not confirmed |
| **Not disclosed** | The relevant primary sources were checked and do not contain the metric — a disclosure fact, not a performance judgment |

Rules: external confirmation never upgrades a label to Verified — only directly reading the source does. "Reported" is Medium confidence at most. **Evidence for ratings:** first-pass factual ratings may use Reported evidence provisionally; the label tells the reader how much to trust it. New or revised factual inputs used to change a rating in a follow-up require Verified or Calculated — verified inputs evidence. Model outputs keep their applicable Estimated label even when every input is Verified; changes in assumptions, judgments, arithmetic, or framework version require an explicit audit trail (the packet's score-change audit trail where it has one) and must not be described as newly verified performance. A derived ratio takes "Calculated — verified inputs" only when every input meets the verification standard; if any input is weaker, the ratio takes the weakest input's label. Only Verified or Calculated — verified inputs evidence can activate a Severe-flag score cap.

## Utility metric verification standard

A metric is **Verified** only when the output includes all seven evidence items: 1. metric name · 2. exact value · 3. source document (filing type and date) · 4. exact table, note, or section · 5. short quote showing the metric label next to the value · 6. definition match to this guide · 7. score impact.

Search summaries, aggregator snippets, and unlabeled extracted numbers cannot verify utility metrics. Never reuse a number from a nearby table unless the label exactly matches the intended metric — allowed ROE, earned ROE, equity ratio, and authorized equity layer are all percentages in the same rate-case documents. The label controls the meaning.

**Conflicting figures rule:** when two figures for the same metric appear to conflict, do not choose one immediately. First classify the difference: 1. different scope — group vs segment, consolidated vs ex-subsidiary · 2. different basis — gross vs net, reported vs adjusted · 3. different period — quarterly, annualized, LTM, fiscal year · 4. different currency · 5. different definition — company-defined vs packet-defined. Show both figures with provenance labels, then rate the pillar based on the figure that best matches the packet definition. If neither figure matches the packet definition, keep the pillar at Watch or Needs verification.

**Estimated proxy:** when a metric is calculated from available inputs but does not match the company's exact disclosed definition, label it **"Estimated proxy"** and state the inputs used. Examples: an AFFO payout proxy estimated above 100% when AFFO itself is not disclosed; an interest coverage proxy estimated from verified income-statement inputs but not company-disclosed; a net debt/EBITDAre proxy estimated when EBITDAre is not disclosed or JV/pro-rata treatment is unresolved. Never imply the proxy is the same as the company's official metric: a proxy is a sub-type of Estimated, is never Verified, never High confidence, and any rating that rests on it must say so.

**Guidance is not achievement:** guidance, targets, and management plans can support a Watch or directional comment, but they should not receive full Positive credit unless supported by achieved results, binding regulatory approval, or directly verified realized performance. This applies especially to: utilities rate-base growth guidance · REIT rent ramp / stabilized rent targets · energy production or capex targets · SaaS margin expansion targets · bank medium-term ROE targets.

**Expectations are not results (universal):** a price already contains a forecast, and a review that only compares multiples never states what that forecast is. Run this test whenever the valuation pillar would otherwise rest on a multiple above the company's own 5-year range, or whenever the market or management thesis rests on segments with no achieved results; otherwise record "expectations test not triggered" and move on. Invert the valuation — hold the current price fixed and solve for what it requires: revenue CAGR over a stated horizon, steady-state operating or FCF margin, reinvestment (sales-to-capital or reinvestment rate), the discount rate with its components, and a terminal growth rate no higher than the long-run risk-free rate. Convert the requirement into absolute end-of-horizon revenue and test it three ways: against the company's own achieved 5-year record, against the best verified peer analog at comparable scale, and against the current size of the market being addressed. **TAM × assumed share is not a valuation output — it is the assumption under test.** Where a sector packet defines an expectations adaptation, the adaptation governs the variables solved for and the value split; the triggers, caps and labels of this module still apply.

**Proven vs unproven enterprise value:** split EV into the part the proven business supports under the sector packet's normal valuation method and the residual the market is paying for optionality. A segment counts as proven only when the company discloses its revenue AND either its operating profit or a company-defined unit economic; anything else is unproven, is valued separately and labeled, and is never blended into the base multiple. Report the residual as a share of total EV. Rules: required inputs that exceed anything the company has achieved — or anything a verified peer has achieved at comparable scale — cap the valuation pillar at Watch unless the review names the specific verified evidence supporting the higher requirement · residual EV above ~50% of total EV caps the valuation pillar at Watch and obliges the conclusion to state the residual share, whatever the operating pillars show · disclosure too thin to build the test (no segment detail, no margin path) makes valuation **Needs verification**, never a favorable default · do not penalize the same optimism twice by both discounting the required growth and inflating the discount rate — pick one and say which.

**Estimated — expectations-implied:** every output of this test carries that label, a sub-type of Estimated. It is never Verified and never High confidence, because the solution depends on assumptions the review itself chose; only the inputs (price, period-end share count, net debt, disclosed segment figures) carry labels of their own. **Avoid:** analyst price targets as evidence of value · forward multiples built on margins the company has never achieved · "cheap versus its own history" when that history sits entirely inside one expansion regime · peer multiples where the peers are themselves priced on expectations.

## Regulatory metric disambiguation (Branch A)

| Term | What it is |
|---|---|
| Allowed ROE | The return the regulator authorizes — set in rate cases; varies by jurisdiction and segment |
| Earned ROE | The return actually achieved on regulated equity — the gap vs allowed is the key signal |
| Authorized equity layer | The equity share of the capital structure the regulator allows — not an ROE |
| Rate base growth | Growth in the asset base earning a regulated return — the real growth engine; capex plans are not rate base until approved and in service |
| Regulatory lag | Delay between spending and recovery — quantified by earned-vs-allowed gap and rate-case timing |
| Rate-case outcome | Approved ROE, equity layer, and rate increase vs requested — read the order or the company's summary, not headlines |

Rules: never present allowed ROE as earned ROE or vice versa. A capex plan is a rate-base growth *forecast* — label it as company guidance, not achieved growth. A persistent earned-below-allowed gap rates the regulatory pillar Watch at best even if allowed ROE is high. Rate-case outcomes must state jurisdiction, date, and approved-vs-requested numbers.

## Earnings-mix and payout definition rules

The earnings mix is set by the routing section: regulated-utility thresholds apply only to the regulated share, and merchant generation, trading, and competitive retail are scored under Branch B.

**The payout ratio must state its basis:** dividends ÷ GAAP EPS, dividends ÷ adjusted/operating EPS (company-defined — read the reconciliation), or dividends ÷ FFO/cash flow. A payout comfortable on adjusted EPS but above 100% of GAAP EPS requires the GAAP gap to be explained (one-off impairments vs recurring add-backs). If only one basis is disclosed, say which and label the others Needs verification. Never compare one company's adjusted-EPS payout to another's GAAP payout.

## Utility debt definition rules

A leverage figure is incomplete until the output specifies: 1. gross debt or net debt · 2. EBITDA basis (reported, adjusted, LTM vs annualized) · 3. consolidated vs holdco vs opco scope · 4. whether hybrids/preferreds are treated as debt or equity · 5. currency. If any of these is unclear, label the metric **"Reported, pending direct verification"** or **"Needs verification"** — do not present an ambiguous ratio as Verified, and say which definition element is missing. Branch B adds project-level debt and the other scope items in its definition rules.

**Scope-dependence rule:** leverage figures reported at different scopes (e.g., consolidated group vs a single regulated opco) are scope-dependent rather than contradictory — report each figure with its scope stated. The balance-sheet pillar cannot rate above Watch until the branch's preferred consolidated basis (Branch A: FFO/debt and net debt/EBITDA; Branch B: consolidated net debt/adjusted EBITDA) is verified or soundly reconciled.

**Holdco vs opco:** holding-company debt sits structurally behind opco debt and is serviced by upstreamed dividends. Report holdco debt as a share of total where disclosed; heavy holdco leverage with regulated-dividend restrictions is a Moderate flag even when consolidated ratios look acceptable. Fixed vs floating mix and the maturity ladder must be characterized; heavy floating or a near-term wall in a rising-rate cycle is at least Moderate.

## Valuation logic (Branch A)

Use: P/E versus rate-base/EPS growth (state which EPS basis) · dividend yield spread versus long bonds · FFO/debt for credit quality. Avoid: FCF alone — regulated capex is recovered through rates, so weak FCF is often structural, not a flaw · revenue growth comparisons with other sectors · Rule of 40 and growth-stock metrics generally. A high yield is not automatically attractive: **a yield far above the peer group usually prices dividend or regulatory risk, not a bargain.**

## Default first-pass dashboard (Branch A)

Header must show: company / ticker · sector classification · regulated/unregulated earnings mix · key jurisdictions · analysis date and data freshness · provisional score.

Then six to eight key metrics — use a table, not a long paragraph:

| Metric | Value | Rating | Provenance | Comment |
|---|---|---|---|---|
| EPS (state basis) & growth | | | | |
| Rate-base growth (achieved vs guided) | | | | |
| Allowed vs earned ROE | | | | |
| Dividend, yield & payout (state basis) | | | | |
| FFO/debt (state whose definition) | | | | |
| Net debt/EBITDA (state definition status) | | | | |
| Interest coverage | | | | |
| Fixed/floating mix & maturity wall | | | | |

Then: red flags by severity (each with provenance status) · missing or unverified data, listed explicitly · neutral research conclusion.

The first-pass utility score is always provisional unless: the payout basis is resolved, the leverage definition (including holdco/opco split) is resolved, allowed-vs-earned ROE is sourced, rate-base growth is distinguished from capex guidance, and at least partial peer comparison is performed.

## Utility-specific "Verify missing data" action (Branch A)

When the user picks Verify missing data, prioritize in this order: 1. FFO/debt (whose definition, which scope) · 2. payout basis (GAAP vs adjusted EPS vs cash flow) · 3. holdco vs opco debt split · 4. earned vs allowed ROE by jurisdiction · 5. rate-case status and outcomes · 6. fixed/floating mix and maturity wall · 7. equity-issuance needs for the capex plan · 8. regulated/unregulated earnings mix.

Other follow-up actions: deeper analysis · compare vs peers · deep dive: valuation · deep dive: risks · deep dive: regulatory quality / dividend safety / balance sheet · full research memo. Priority logic: payout above 85% or basis unclear → verify payout first. FFO/debt near 10% → verify before rating balance sheet. Large capex plan → check equity needs and dilution. Earned ROE persistently below allowed → deep dive regulatory quality.

## Score-change audit trail

Whenever a follow-up action changes the score, show all nine items: 1. previous score · 2. updated score · 3. metric that changed · 4. old status · 5. new verified value · 6. source document · 7. exact quote showing label and value · 8. pillar affected · 9. reason for the change.

Rules: if the exact quote for a new factual input cannot be provided, do not change the score on that input — keep the metric at its prior label. A score changes only when a pillar's Positive/Watch/Negative rating changes — through a newly verified input, or through a disclosed change in assumption, judgment, arithmetic, or framework version (name the type in item 9; items 5–7 then read "not applicable"); verification alone does not automatically change the score.

## Utility data confidence rules

**High:** recent 10-K / 10-Q / earnings release / rate-case order / credit-agency report with the exact table label and value quoted. **Medium:** investor presentation with a labeled table; reputable provider cross-checked against filings; user-provided filing excerpts; reported values pending direct verification. **Low:** aggregator-only data, search-summary data, payout ratios with unstated bases, FFO/debt with unstated definitions, unlabeled numbers.

Rules: price, P/E, and yield from aggregators may be used as Estimated. FFO/debt and earned ROE are never High confidence unless the source clearly labels them. If a key metric is Low confidence or missing, state how it affects the pillar score.

## What NOT to use (Branch A)

Free cash flow as a quality test — regulated capex is recovered through rates, so weak FCF is often structural, not a flaw. Revenue growth comparisons with other sectors. Rule of 40 and growth-stock metrics generally. Yield alone as a valuation signal.

## Common mistakes to avoid

Presenting allowed ROE as earned ROE · treating capex guidance as achieved rate-base growth · quoting a payout ratio without its basis · comparing adjusted-EPS payouts to GAAP payouts · presenting an ambiguous leverage ratio as verified · ignoring the holdco/opco debt split · ignoring hybrids and preferreds in leverage · applying regulated thresholds to a majority-unregulated business · reading weak FCF as a flaw without checking the regulated capex cycle · calling a far-above-peer yield cheap · upgrading a pillar because a metric was found, even though the metric is still in Watch range · applying one branch's thresholds to the other branch's earnings · treating hedge percentage as protection or a forward curve as mid-cycle.

## Red flags (Branch A)

**Severe** — dividend not covered by earnings with payout above 90% and rising debt · hostile regulatory ruling cutting allowed ROE materially · FFO/debt below ratings thresholds with a downgrade to junk in play · going-concern language, covenant pressure, or liability events (wildfire, environmental) large vs equity.

**Moderate** — FFO/debt below 10% — credit downgrade risk · heavy floating-rate or short-maturity debt in a rising-rate cycle · heavy holdco leverage with restricted opco dividends · persistent earned-below-allowed ROE gap · large equity-issuance needs for the capex plan (dilution offsetting rate-base growth) · payout above 85% on the stated basis · pending rate case with a materially adverse staff recommendation.

**Minor** — modest earned-vs-allowed ROE gap from one-off costs · small floating-rate drift · one-quarter weather-driven earnings miss.

Grade findings Minor / Moderate / Severe and attach a provenance status to each before applying any cap.

## Scoring weights (Branch A)

| Pillar | Weight |
|---|---|
| Regulatory quality & allowed ROE | 25% |
| Balance sheet (FFO/debt, coverage) | 25% |
| Rate-base / EPS growth | 20% |
| Dividend safety | 20% |
| Valuation (P/E vs growth, yield spread) | 10% |

Score each pillar 2 (Positive), 1 (Watch), 0 (Negative) vs peers and own history; weighted total ÷ 2 = 0–100%. ~75%+ strong on current evidence; 50–75% mixed — investigate the weak pillar; <50% with sufficient evidence and no verified Severe flag = weak on current evidence. Any verified Severe red flag caps the score at 50% until resolved; two or more usually mean high-risk / special situation. Verify flags against primary sources before capping. The score is a research organizer, not a prediction engine.

## Branch B — Competitive generation and retail

*Independent power producers, merchant nuclear and gas fleets, wholesale trading, competitive retail electricity.* Typical names: Vistra, Constellation (re-check its mix after the Calpine acquisition, closed January 2026), NRG, Talen. Yieldcos and contracted-renewables developers are not yet calibrated: if one is routed here, say so and label every rating provisional.

**Core principle: hedge volume is not protection, and a forward curve is not mid-cycle.** These businesses earn the spread between power and fuel prices in markets that move by region, and they carry delivery obligations that bite hardest when plants fail during scarcity. The questions are how much of the next few years' margin is actually protected, what is left exposed, whether liquidity survives a stress event, and what the price assumes.

### Step zero — market conditions by region and revenue source

Before rating anything, state conditions for each material market (e.g., ERCOT, PJM, NYISO, CAISO) and revenue source: energy prices, fuel spreads, capacity prices, contracts, and support mechanisms. Explain auction caps or collars and relevant rule changes — a capacity auction that clears at an administratively approved cap is not an unrestricted scarcity signal. Nuclear production tax credit support is not a fixed-price contract: the credit declines as qualifying receipts rise and applies only for a limited statutory period. There is no single US power cycle. Where market exposure is material to value and conditions cannot be determined, cap the valuation pillar at Watch. A change in forward curves updates the relevant cash-flow calculations; it does not create an additional discretionary penalty for the same effect.

### Key metrics (Branch B)

Bands are provisional research checkpoints, not rating-agency thresholds. Each pillar's decision rule (next section) decides the rating.

| Metric | Positive | Watch | Negative | How to read it |
|---|---|---|---|---|
| **Hedge / contract coverage by delivery year** | descriptive | descriptive | descriptive | Report by year and as-of date; separate financial hedges, physical contracts, retail offsets, and tax-credit protection; state whether the current-year figure covers the full year or remaining generation; compare with the company's stated hedging policy. Coverage alone earns no rating |
| **Residual earnings sensitivity (Y+1)** | ≤ ~10% of guided EBITDA | 10–25%, or not disclosed | > ~25% | EBITDA impact of the company's disclosed price move on open volumes. State what the sensitivity excludes (fuel, basis, outages, collateral) |
| **Net debt / adjusted EBITDA** | < 2.5x | 2.5–3.5x | > 3.5x | Consistently scoped LTM. Show the company definition (often excludes project-level debt) and the consolidated figure; never present one as the other |
| **Cash interest coverage** | > 5x | 3–5x | < 3x | EBITDA ÷ cash interest; exclude swap mark-to-market and capitalized interest effects — state treatment |
| **Liquidity vs stressed needs** | Usable resources exceed stated stress needs | Not disclosed, or scenario inadequate | Evidenced obligations exceed usable resources | Method in `merchant_power_procedures.md` (section 5) |
| **FCF before growth conversion** (multi-year FCFbG ÷ adjusted EBITDA) | > 50% | 35–50% | < 35% | Company-defined measure: read the reconciliation to GAAP operating cash flow and required recurring spending. Peer comparison only on reconciled definitions |
| **FCFbG per share, 3-yr CAGR** | > 8% | 3–8% | < 3% | Comparable positive endpoints; split-adjusted share count. Separate changes in total cash generation, portfolio scope, and share count |
| **Fleet availability / forced outages** | context | context | context | Grade outages by duration, portfolio exposure, replacement cost, and contractual consequences — not by the number of units |

**Definition rules (Branch B):** FCFbG and adjusted EBITDA are company-defined and differ across issuers (working capital, margin deposits, collateral, nuclear fuel, customer-acquisition costs, acquisition adjustments); unreconciled definitions cannot support comparative credit, but a company's own verified reconciliation and comparable history can still be rated — cap the pillar only when the unresolved difference materially prevents assessment. Leverage must also state the treatment of project-level (non-recourse) debt, restricted cash, leases, minority interests, capitalized interest, and cash hedge settlements. **GAAP vs adjusted:** unrealized hedge mark-to-market is not an earnings-quality failure by itself; every other recurring add-back must be named and sized.

### Pillars, primary evidence, and decision rules (Branch B)

| Pillar | Weight | Primary evidence |
|---|---|---|
| Earnings visibility and protection | 25% | Residual sensitivity, coverage detail, delivery and liquidity flags |
| Balance sheet and liquidity | 25% | Leverage, cash interest coverage, liquidity vs stressed needs |
| Cash generation and per-share growth | 20% | FCFbG conversion, FCFbG-per-share growth with attribution |
| Capital allocation | 15% | Funding discipline, achieved acquisition returns, distributions vs available cash |
| Valuation | 15% | Price against the justified cash-flow cases |

1. **Earnings visibility and protection.** Positive requires all three: (a) residual Y+1 sensitivity ≤ ~10% of guided EBITDA; (b) no unresolved Moderate-or-worse flag on delivery, basis, fuel, or liquidity; (c) the sensitivity's exclusions stated. Watch if any condition fails or is not disclosed. Negative if residual sensitivity exceeds ~25% or a delivery/liquidity flag has escalated under its stated conditions. **Hedge carve-out to "guidance is not achievement":** verified enforceable protection (executed hedges and contracts) can support Positive visibility. This credits the protection already established, not achievement of forecast generation, margin, or earnings.
2. **Balance sheet and liquidity.** Rate leverage and coverage on the bands; the pillar takes the weaker of the leverage/coverage reading and the liquidity reading. Strong leverage never compensates for unresolved material liquidity exposure. The shared scope-dependence rule applies: no rating above Watch until the consolidated basis is verified or soundly reconciled.
3. **Cash generation and per-share growth.** Positive requires conversion in the Positive band (or a verified company-specific history equivalent to it) AND per-share growth > 8% with total cash generation also growing — not share-count reduction alone. A missing acquisition bridge limits organic-growth claims; it does not prove poor acquisition economics.
4. **Capital allocation.** Positive: leverage held within the company's own target through acquisitions, distributions plus buybacks within FCFbG after required reinvestment, and disclosed acquisition returns achieved. Watch: any of these unproven. Negative: debt-funded distributions beyond FCFbG, or leverage above the company's own target for 12+ months because of allocation choices. Repurchases already credited in pillar 3 are not credited again here — this pillar judges their funding and price only.
5. **Valuation.** Positive only when the procedures in `merchant_power_procedures.md` were run and the current price is supported in both the forward-curve case and the normalized case. Watch when supported in one case, or when the procedures were not run. Negative when supported in neither. EV/EBITDA vs own 5-year history and Branch B peers, and FCFbG yield, are cross-checks only; a low multiple on peak or fully hedged earnings is not cheapness.

Caps are ceilings, not additive deductions. Correlated flags count as one event, not separate Severe events. When one development legitimately affects several pillars (e.g., collateral funding and future margins), name each consequence explicitly.

### Expectations adaptation (Branch B)

This adaptation replaces the standard variables and split; the module's triggers, caps, and labels still apply. **Reverse-solve an explicit cash-flow model** that funds the investment implied growth requires and reflects contract expiry and asset life (license dates, retirement schedules). Use FCFE with market capitalization and cost of equity, or FCFF with enterprise value and WACC — never mix them. A yield shortcut (FCF yield ≈ cost of equity − growth) is permitted only as a steady-state cross-check with its assumptions stated; it does not fund growth, and the sign of long-run growth for an aging fleet must come from an explicit cash-flow path, not an assumption.

**Proven vs unproven value:** the established-business base keeps achieved recurring earnings from operating plants and operating contracts. Future contracts whose economics are not disclosed earn their verified contractual visibility but no unsupported incremental earnings or contract premium; annotate them "contracted, economics not disclosed" beside their provenance label. Where contract economics can be modeled, replace the covered merchant cash flows rather than adding a second value for the same output. Assess termination rights, delivery obligations, required investment, and conditions precedent. Unsigned large-load deals, uprates without approval, and uncontracted new builds are the unproven residual.

**Loading rule:** the detailed procedures live in `merchant_power_procedures.md`, loaded automatically during the first pass whenever the expectations test triggers or the valuation pillar would rate above Watch. If the required analysis cannot be completed, valuation is **Needs verification** and scores no higher than Watch. Guidance and disclosed sensitivities cannot independently justify Positive valuation while the expectations gate is unresolved.

### What NOT to use (Branch B)

Allowed or earned ROE and rate base · the Branch A FFO/debt and debt/EBITDA bands · GAAP EPS as a quality test (hedge mark-to-market distorts it) · dividend yield as a valuation signal · the "weak FCF is structural" defense (that applies only to regulated capex recovered through rates) · hedge percentage as protection · current forward curves as mid-cycle earnings · peak-year or fully hedged-year multiples as evidence of cheapness.

### Red flags (Branch B)

Each flag has a default severity and objective escalation conditions. A Severe cap additionally requires Verified or Calculated — verified inputs evidence that the stated Severe condition is met; an analyst-designed stress failure stays an Estimated warning.

| Flag | Default | Escalates to Severe when |
|---|---|---|
| Liquidity short of stated stress needs (collateral, replacement power, maturities) | Moderate | Directly evidenced obligations exceed usable resources |
| Generation-vs-delivery mismatch: short power during scarcity (retail or contract obligations exceed reliable supply) | Moderate if material | Resulting losses, penalties, or funding needs threaten liquidity or covenant compliance |
| Unprotected basis or load-shape exposure; fuel-delivery vulnerability (firm gas, winterization) | Moderate if material | Same as above |
| Repeated forced outages; material capacity-performance obligations | Moderate | Same as above |
| Realized hedge or trading losses | Assess net of offsetting physical margin; Moderate if material net | Net losses threaten liquidity or covenant compliance |
| Downgrade below investment grade in play | Moderate | Collateral or funding consequences exceed usable liquidity or breach covenants |
| Leverage above the company's own target for 12+ months or after an acquisition | Moderate | — (balance-sheet pillar handles it) |
| Material unfunded decommissioning, retirement, or environmental obligations | Moderate | Funding demands threaten liquidity |
| Single counterparty or single market dominating margin | Moderate | — |
| Policy / market-design risk: capacity price caps, large-load interconnection reviews, co-location rules | Moderate | — |
| Contract term beyond current operating license or asset life | Minor | Moderate when contract value depends on a renewal not yet granted and no substitution right exists |
| Growth mostly acquired with no organic bridge | Minor | — (limits organic-growth claims only) |
| Commitments outside the core business | Minor | Moderate when debt-funded or above the company's stated limit |
| Going-concern language, covenant breach | Severe | — |
| Weather-driven quarter | Minor | — |

### First-pass dashboard (Branch B)

Header: company / ticker · route and merchant share (basis, period) · material markets · analysis date and data freshness · next catalyst · provisional score. Then:

| Metric | Value | Rating | Provenance | Comment |
|---|---|---|---|---|
| Market conditions by region (step zero) | | | | |
| Hedge / contract coverage by delivery year (descriptive) | | — | | |
| Residual earnings sensitivity (Y+1) | | | | |
| Net debt / adjusted EBITDA (both definitions) | | | | |
| Cash interest coverage | | | | |
| Liquidity vs stressed needs | | | | |
| FCFbG conversion and FCFbG/share growth | | | | |
| Valuation cross-checks (EV/EBITDA, FCFbG yield) and procedures status | | | | |

The Branch B score is always provisional unless: the route and merchant share are sourced, the leverage scope is resolved, residual sensitivity is disclosed, the valuation procedures were run, and at least partial peer comparison is done.

**Verify missing data (Branch B) — priority:** 1. liquidity, collateral postings, and facility restrictions · 2. leverage scope (project debt, restricted cash) · 3. residual sensitivity and hedge-price disclosure · 4. FCFbG reconciliation · 5. merchant share for routing · 6. contract terms (start dates, termination rights, conditions precedent) · 7. market exposure by region. Other follow-ups: deep dive hedge book and delivery exposure · liquidity and collateral · market exposure by region · valuation · full memo.

**Peers:** default Vistra, Constellation, NRG, Talen (excluding the subject); confirm each peer's current mix before comparing.

### Scoring (Branch B)

Weights as in the pillar table (25 / 25 / 20 / 15 / 15). Score each pillar 2 / 1 / 0; weighted total ÷ 2 = 0–100%. Same conclusion bands and Severe-cap rule as Branch A.

### Checklist (Branch B)

1. Route and merchant share stated with basis, period, and adjustments; both branches scored if each ≥ 20%. 2. Step zero completed by region and revenue source. 3. Coverage reported descriptively; residual sensitivity and its exclusions stated. 4. Leverage shown in both definitions with scope items. 5. Liquidity vs stressed needs assessed or marked Not disclosed. 6. FCFbG reconciled; per-share growth attributed. 7. Capital allocation rated without re-crediting buybacks. 8. Valuation procedures run or valuation held at Watch / Needs verification. 9. Contracts with undisclosed economics annotated, not valued. 10. Flags graded with escalation conditions and provenance before any cap. 11. Weighted score, weakest pillar, neutral conclusion.

## Conclusion template

End with exactly one of: **strong on current evidence** / **mixed, needs more evidence** (name the evidence) / **weak on current evidence** (score <50% with sufficient evidence and no verified Severe flag) / **high-risk, special situation** / **insufficient data** — plus data confidence (High/Medium/Low) and a two-sentence thesis including what would break it. No buy/sell/hold language.

## Final sector checklist (Branch A)

1. Route confirmed (routing section): regulated and merchant shares stated with basis; Branch B also scored if the merchant share is ≥ 20%.
2. Jurisdictions identified; regulatory quality assessed per jurisdiction where material.
3. Peer group built on regulated mix, jurisdiction quality, size, growth stage, leverage profile.
4. Utility metrics labeled with provenance; Verified only with exact quoted labels from primary sources.
5. Regulatory metrics disambiguated: allowed vs earned ROE, equity layer, rate base vs capex guidance, regulatory lag, rate-case outcomes.
6. Payout basis stated: GAAP EPS vs adjusted EPS vs cash flow.
7. Debt definition resolved: gross/net, EBITDA basis, holdco/opco scope, hybrids, currency; fixed/floating and maturity wall characterized.
8. Earnings mix respected: regulated thresholds not applied to unregulated earnings.
9. "What NOT to use" respected.
10. Quality-of-earnings and geographic/currency checks run (Core Framework).
11. Red flags graded, provenance-labeled, and verified before applying the Severe cap.
12. Valuation done with P/E vs growth, yield spread, FFO/debt — not yield or FCF alone.
13. Weighted score computed; weakest pillar identified.
14. Score-change audit trail shown if any follow-up action changed the score.
15. Neutral research conclusion written with data confidence and unresolved gaps.

*This is general information only and not financial advice. For personal guidance, please talk to a licensed professional.*
