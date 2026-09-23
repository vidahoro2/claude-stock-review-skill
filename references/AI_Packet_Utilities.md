# AI Stock Review Packet: Utilities

**Version 2.2.4 — Last updated 2026-09-22.** Supersedes v2.2.3. v2.2.4 adds one shared expectations-module sentence: where a sector packet defines an expectations adaptation, it governs the variables solved for and the value split (Banks and Insurers now define one). v2.2.3 adds the expectations-embedded valuation module: the universal expectations test (reverse-solve the price for required growth, margin, reinvestment and discount rate), the proven-vs-unproven enterprise-value split with its valuation-pillar caps, and the "Estimated — expectations-implied" sub-label. v2.2.2 adds the weak-on-current-evidence conclusion category. v2.2.1 extends the v4 provenance labels (adds Calculated — verified inputs and Not disclosed; Severe-flag caps require verified evidence). Supersedes v2.1: upgraded from a general sector guide to a strict execution file (v4 verification and provenance standard, regulatory and leverage disambiguation, payout-definition rules, holdco/opco rules, scoring and audit-trail rules). Educational framework — not investment advice. No buy/sell/hold language.

*Electric, gas, water — mostly regulated* — GICS: Utilities (Electric, Gas, Water, Multi-Utilities; unregulated power producers differ — check the mix)

**Core principle: Verified does not mean Positive.** Verification proves the number is real; the sector thresholds and the trend determine the rating. A verified FFO/debt of 12% is still Watch. A verified payout of 88% of EPS is still Watch-to-Negative.

## Prompt

> Analyze [company name / ticker] using the uploaded Core Framework and this Utilities guide.
> Do not use buy/sell/hold language.
> Provide: 1. Business model summary · 2. Sector classification and regulated/unregulated mix · 3. Peer group with rationale · 4. Key utility metrics with provenance labels · 5. Values vs peers and 5-year history · 6. Positive/Watch/Negative assessment · 7. Severe red flags, if any · 8. Valuation (P/E vs rate-base growth, yield spread, FFO/debt) · 9. Data confidence: High/Medium/Low · 10. Neutral research conclusion: strong on current evidence / mixed, needs more evidence / high-risk, special situation / insufficient data.
> Use primary sources (10-K, 10-Q, earnings releases, rate-case filings, regulatory orders, credit-agency reports). Do not rely only on screeners or summaries.

## Sector context

Bought for stable dividends, not growth. Regulators cap returns, so the story is dividend safety, rate-base growth, regulatory quality, and debt cost. Heavy regulated capex makes free cash flow look weak — that can be fine, because regulators allow a return on that spending. Always state the regulated/unregulated earnings mix before applying regulated-utility thresholds.

## Key metrics & rule-of-thumb ranges

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

Rules: external confirmation never upgrades a label to Verified — only directly reading the source does. "Reported" is Medium confidence at most and never enough by itself to upgrade a pillar. A score can use reported or estimated data cautiously; the label tells the reader how much to trust it. A derived ratio takes "Calculated — verified inputs" only when every input meets the verification standard; if any input is weaker, the ratio takes the weakest input's label. Only Verified or Calculated — verified inputs evidence can activate a Severe-flag score cap.

## Utility metric verification standard

A metric is **Verified** only when the output includes all seven evidence items: 1. metric name · 2. exact value · 3. source document (filing type and date) · 4. exact table, note, or section · 5. short quote showing the metric label next to the value · 6. definition match to this guide · 7. score impact.

Search summaries, aggregator snippets, and unlabeled extracted numbers cannot verify utility metrics. Never reuse a number from a nearby table unless the label exactly matches the intended metric — allowed ROE, earned ROE, equity ratio, and authorized equity layer are all percentages in the same rate-case documents. The label controls the meaning.

**Conflicting figures rule:** when two figures for the same metric appear to conflict, do not choose one immediately. First classify the difference: 1. different scope — group vs segment, consolidated vs ex-subsidiary · 2. different basis — gross vs net, reported vs adjusted · 3. different period — quarterly, annualized, LTM, fiscal year · 4. different currency · 5. different definition — company-defined vs packet-defined. Show both figures with provenance labels, then rate the pillar based on the figure that best matches the packet definition. If neither figure matches the packet definition, keep the pillar at Watch or Needs verification.

**Estimated proxy:** when a metric is calculated from available inputs but does not match the company's exact disclosed definition, label it **"Estimated proxy"** and state the inputs used. Examples: an AFFO payout proxy estimated above 100% when AFFO itself is not disclosed; an interest coverage proxy estimated from verified income-statement inputs but not company-disclosed; a net debt/EBITDAre proxy estimated when EBITDAre is not disclosed or JV/pro-rata treatment is unresolved. Never imply the proxy is the same as the company's official metric: a proxy is a sub-type of Estimated, is never Verified, never High confidence, and any rating that rests on it must say so.

**Guidance is not achievement:** guidance, targets, and management plans can support a Watch or directional comment, but they should not receive full Positive credit unless supported by achieved results, binding regulatory approval, or directly verified realized performance. This applies especially to: utilities rate-base growth guidance · REIT rent ramp / stabilized rent targets · energy production or capex targets · SaaS margin expansion targets · bank medium-term ROE targets.

**Expectations are not results (universal):** a price already contains a forecast, and a review that only compares multiples never states what that forecast is. Run this test whenever the valuation pillar would otherwise rest on a multiple above the company's own 5-year range, or whenever the market or management thesis rests on segments with no achieved results; otherwise record "expectations test not triggered" and move on. Invert the valuation — hold the current price fixed and solve for what it requires: revenue CAGR over a stated horizon, steady-state operating or FCF margin, reinvestment (sales-to-capital or reinvestment rate), the discount rate with its components, and a terminal growth rate no higher than the long-run risk-free rate. Convert the requirement into absolute end-of-horizon revenue and test it three ways: against the company's own achieved 5-year record, against the best verified peer analog at comparable scale, and against the current size of the market being addressed. **TAM × assumed share is not a valuation output — it is the assumption under test.** Where a sector packet defines an expectations adaptation, the adaptation governs the variables solved for and the value split; the triggers, caps and labels of this module still apply.

**Proven vs unproven enterprise value:** split EV into the part the proven business supports under the sector packet's normal valuation method and the residual the market is paying for optionality. A segment counts as proven only when the company discloses its revenue AND either its operating profit or a company-defined unit economic; anything else is unproven, is valued separately and labeled, and is never blended into the base multiple. Report the residual as a share of total EV. Rules: required inputs that exceed anything the company has achieved — or anything a verified peer has achieved at comparable scale — cap the valuation pillar at Watch unless the review names the specific verified evidence supporting the higher requirement · residual EV above ~50% of total EV caps the valuation pillar at Watch and obliges the conclusion to state the residual share, whatever the operating pillars show · disclosure too thin to build the test (no segment detail, no margin path) makes valuation **Needs verification**, never a favorable default · do not penalize the same optimism twice by both discounting the required growth and inflating the discount rate — pick one and say which.

**Estimated — expectations-implied:** every output of this test carries that label, a sub-type of Estimated. It is never Verified and never High confidence, because the solution depends on assumptions the review itself chose; only the inputs (price, period-end share count, net debt, disclosed segment figures) carry labels of their own. **Avoid:** analyst price targets as evidence of value · forward multiples built on margins the company has never achieved · "cheap versus its own history" when that history sits entirely inside one expansion regime · peer multiples where the peers are themselves priced on expectations.

## Regulatory metric disambiguation

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

State the regulated vs unregulated earnings mix before scoring. Regulated-utility thresholds apply only to the regulated share; merchant generation, trading, and other unregulated earnings are more volatile and deserve cyclical caution. A company majority-unregulated by operating profit does not belong on this packet without adjustment.

**The payout ratio must state its basis:** dividends ÷ GAAP EPS, dividends ÷ adjusted/operating EPS (company-defined — read the reconciliation), or dividends ÷ FFO/cash flow. A payout comfortable on adjusted EPS but above 100% of GAAP EPS requires the GAAP gap to be explained (one-off impairments vs recurring add-backs). If only one basis is disclosed, say which and label the others Needs verification. Never compare one company's adjusted-EPS payout to another's GAAP payout.

## Utility debt definition rules

A leverage figure is incomplete until the output specifies: 1. gross debt or net debt · 2. EBITDA basis (reported, adjusted, LTM vs annualized) · 3. consolidated vs holdco vs opco scope · 4. whether hybrids/preferreds are treated as debt or equity · 5. currency. If any of these is unclear, label the metric **"Reported, pending direct verification"** or **"Needs verification"** — do not present an ambiguous ratio as Verified, and say which definition element is missing.

**Scope-dependence rule:** leverage figures reported at different scopes (e.g., consolidated group vs a single regulated opco) are scope-dependent rather than contradictory — report each figure with its scope stated. The balance-sheet pillar cannot rate above Watch until the packet's preferred consolidated basis (FFO/debt and net debt/EBITDA) is verified or soundly reconciled.

**Holdco vs opco:** holding-company debt sits structurally behind opco debt and is serviced by upstreamed dividends. Report holdco debt as a share of total where disclosed; heavy holdco leverage with regulated-dividend restrictions is a Moderate flag even when consolidated ratios look acceptable. Fixed vs floating mix and the maturity ladder must be characterized; heavy floating or a near-term wall in a rising-rate cycle is at least Moderate.

## Valuation logic

Use: P/E versus rate-base/EPS growth (state which EPS basis) · dividend yield spread versus long bonds · FFO/debt for credit quality. Avoid: FCF alone — regulated capex is recovered through rates, so weak FCF is often structural, not a flaw · revenue growth comparisons with other sectors · Rule of 40 and growth-stock metrics generally. A high yield is not automatically attractive: **a yield far above the peer group usually prices dividend or regulatory risk, not a bargain.**

## Default first-pass dashboard for utilities

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

## Utility-specific "Verify missing data" action

When the user picks Verify missing data, prioritize in this order: 1. FFO/debt (whose definition, which scope) · 2. payout basis (GAAP vs adjusted EPS vs cash flow) · 3. holdco vs opco debt split · 4. earned vs allowed ROE by jurisdiction · 5. rate-case status and outcomes · 6. fixed/floating mix and maturity wall · 7. equity-issuance needs for the capex plan · 8. regulated/unregulated earnings mix.

Other follow-up actions: deeper analysis · compare vs peers · deep dive: valuation · deep dive: risks · deep dive: regulatory quality / dividend safety / balance sheet · full research memo. Priority logic: payout above 85% or basis unclear → verify payout first. FFO/debt near 10% → verify before rating balance sheet. Large capex plan → check equity needs and dilution. Earned ROE persistently below allowed → deep dive regulatory quality.

## Score-change audit trail

Whenever a follow-up action changes the score, show all nine items: 1. previous score · 2. updated score · 3. metric that changed · 4. old status · 5. new verified value · 6. source document · 7. exact quote showing label and value · 8. pillar affected · 9. reason for the change.

Rules: if the exact quote cannot be provided, do not change the score — keep the metric at its prior label. A score changes only when the newly verified metric changes a pillar's Positive/Watch/Negative rating; verification alone does not automatically change the score.

## Utility data confidence rules

**High:** recent 10-K / 10-Q / earnings release / rate-case order / credit-agency report with the exact table label and value quoted. **Medium:** investor presentation with a labeled table; reputable provider cross-checked against filings; user-provided filing excerpts; reported values pending direct verification. **Low:** aggregator-only data, search-summary data, payout ratios with unstated bases, FFO/debt with unstated definitions, unlabeled numbers.

Rules: price, P/E, and yield from aggregators may be used as Estimated. FFO/debt and earned ROE are never High confidence unless the source clearly labels them. If a key metric is Low confidence or missing, state how it affects the pillar score.

## What NOT to use

Free cash flow as a quality test — regulated capex is recovered through rates, so weak FCF is often structural, not a flaw. Revenue growth comparisons with other sectors. Rule of 40 and growth-stock metrics generally. Yield alone as a valuation signal.

## Common mistakes to avoid

Presenting allowed ROE as earned ROE · treating capex guidance as achieved rate-base growth · quoting a payout ratio without its basis · comparing adjusted-EPS payouts to GAAP payouts · presenting an ambiguous leverage ratio as verified · ignoring the holdco/opco debt split · ignoring hybrids and preferreds in leverage · applying regulated thresholds to a majority-unregulated business · reading weak FCF as a flaw without checking the regulated capex cycle · calling a far-above-peer yield cheap · upgrading a pillar because a metric was found, even though the metric is still in Watch range.

## Red flags

**Severe** — dividend not covered by earnings with payout above 90% and rising debt · hostile regulatory ruling cutting allowed ROE materially · FFO/debt below ratings thresholds with a downgrade to junk in play · going-concern language, covenant pressure, or liability events (wildfire, environmental) large vs equity.

**Moderate** — FFO/debt below 10% — credit downgrade risk · heavy floating-rate or short-maturity debt in a rising-rate cycle · heavy holdco leverage with restricted opco dividends · persistent earned-below-allowed ROE gap · large equity-issuance needs for the capex plan (dilution offsetting rate-base growth) · payout above 85% on the stated basis · pending rate case with a materially adverse staff recommendation.

**Minor** — modest earned-vs-allowed ROE gap from one-off costs · small floating-rate drift · one-quarter weather-driven earnings miss.

Grade findings Minor / Moderate / Severe and attach a provenance status to each before applying any cap.

## Scoring weights

| Pillar | Weight |
|---|---|
| Regulatory quality & allowed ROE | 25% |
| Balance sheet (FFO/debt, coverage) | 25% |
| Rate-base / EPS growth | 20% |
| Dividend safety | 20% |
| Valuation (P/E vs growth, yield spread) | 10% |

Score each pillar 2 (Positive), 1 (Watch), 0 (Negative) vs peers and own history; weighted total ÷ 2 = 0–100%. ~75%+ strong on current evidence; 50–75% mixed — investigate the weak pillar; <50% with sufficient evidence and no verified Severe flag = weak on current evidence. Any verified Severe red flag caps the score at 50% until resolved; two or more usually mean high-risk / special situation. Verify flags against primary sources before capping. The score is a research organizer, not a prediction engine.

## Conclusion template

End with exactly one of: **strong on current evidence** / **mixed, needs more evidence** (name the evidence) / **weak on current evidence** (score <50% with sufficient evidence and no verified Severe flag) / **high-risk, special situation** / **insufficient data** — plus data confidence (High/Medium/Low) and a two-sentence thesis including what would break it. No buy/sell/hold language.

## Final sector checklist

1. Sector confirmed: most operating profit fits regulated Utilities; regulated/unregulated mix stated.
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
