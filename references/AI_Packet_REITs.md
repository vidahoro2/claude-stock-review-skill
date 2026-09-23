# AI Stock Review Packet: Real Estate / REITs

**Version 2.2.4 — Last updated 2026-09-22.** Supersedes v2.2.3. v2.2.4 adds one shared expectations-module sentence: where a sector packet defines an expectations adaptation, it governs the variables solved for and the value split (Banks and Insurers now define one). v2.2.3 adds the expectations-embedded valuation module: the universal expectations test (reverse-solve the price for required growth, margin, reinvestment and discount rate), the proven-vs-unproven enterprise-value split with its valuation-pillar caps, and the "Estimated — expectations-implied" sub-label. v2.2.2 adds the weak-on-current-evidence conclusion category. v2.2.1 extends the v4 provenance labels (adds Calculated — verified inputs and Not disclosed; Severe-flag caps require verified evidence). Supersedes v2.1: upgraded from a general sector guide to a strict execution file (v4 verification and provenance standard, FFO/AFFO disambiguation, debt-definition rules, dividend-coverage rules, scoring and audit-trail rules). Educational framework — not investment advice. No buy/sell/hold language.

*Real estate investment trusts and property companies* — GICS: Real Estate (Equity REITs by property type: residential, industrial, office, retail, data centers, towers, healthcare; plus RE Management & Development)

**Core principle: Verified does not mean Positive.** Verification proves the number is real; the sector thresholds and the trend determine the rating. A verified AFFO payout ratio of 92% is still Negative-band. A verified net debt/EBITDAre of 6.2x is still Watch.

## Prompt

> Analyze [company name / ticker] using the uploaded Core Framework and this Real Estate / REITs guide.
> Do not use buy/sell/hold language.
> Provide: 1. Business model summary · 2. Sector classification and property type · 3. Peer group with rationale · 4. Key REIT metrics with provenance labels · 5. Values vs peers and 5-year history · 6. Positive/Watch/Negative assessment · 7. Severe red flags, if any · 8. Valuation (P/FFO, P/AFFO, NAV, implied cap rate) · 9. Data confidence: High/Medium/Low · 10. Neutral research conclusion: strong on current evidence / mixed, needs more evidence / high-risk, special situation / insufficient data.
> Use primary sources (10-K, 10-Q, supplemental information packages, earnings releases). Do not rely only on screeners or summaries.

## Sector context

REITs own income-producing property and must pay out most taxable income as dividends. Accounting depreciation makes net income and P/E nearly useless — the sector runs on FFO and AFFO. The three questions: is cash flow per share growing, is the dividend covered by AFFO, and can the balance sheet handle refinancing? Always state the property type — thresholds (occupancy especially) vary by type and must be compared to direct peers.

## Key metrics & rule-of-thumb ranges

| Metric | Positive | Watch | Negative | How to read it |
|---|---|---|---|---|
| **FFO / AFFO per share growth** | > 5%/yr | 0–5% | Declining | The REIT equivalent of EPS growth — always per share. |
| **AFFO payout ratio** | < 80% | 80–90% | > 90% | Above ~90% leaves no cushion; dividend cut risk rises. |
| **Occupancy** | > 95% | 90–95% | < 90% | Benchmark varies by property type — compare to direct peers. |
| **Same-property NOI growth** | > 3% | 0–3% | Negative | Organic growth from the existing portfolio, excluding acquisitions. |
| **Net debt / EBITDAre** | < 5.5x | 5.5–7x | > 7x | REITs run more leverage than corporates, but 7x+ is stretched. |
| **Interest coverage** | > 3x | 2–3x | < 2x | Critical in a rising-rate environment. |
| **Lease maturity schedule** | Laddered, long WALT | Some concentration | Big near-term wall | A wall of expiries in a weak market forces bad renewals. |
| **NAV premium / discount** | Near or below NAV | Modest premium | Large premium | Persistent deep discounts can also signal asset-quality doubts. |
| **Implied cap rate vs market** | Above private-market cap rates | In line | Well below | Compare the implied yield on the portfolio to where properties trade. |

**Formulas:** FFO (Nareit) = net income + real estate depreciation & amortization − gains on property sales. AFFO = FFO − recurring maintenance capex − straight-line rent adjustments. AFFO payout ratio = dividends per share ÷ AFFO per share. NOI = property revenue − property operating expenses (before corporate overhead and interest). Same-property NOI growth = NOI growth for properties owned in both periods. Cap rate = NOI ÷ property value; implied cap rate = portfolio NOI ÷ (market cap + net debt). Net debt/EBITDAre = (total debt − cash) ÷ EBITDA adjusted for real estate (Nareit definition). NAV = estimated market value of properties − net debt, per share.

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

## REIT metric verification standard

A metric is **Verified** only when the output includes all seven evidence items: 1. metric name · 2. exact value · 3. source document (filing type and date) · 4. exact table, note, or section · 5. short quote showing the metric label next to the value · 6. definition match to this guide · 7. score impact.

Search summaries, aggregator snippets, and unlabeled extracted numbers cannot verify REIT metrics. Never reuse a number from a nearby table unless the label exactly matches the intended metric — FFO, Core FFO, AFFO, and company-adjusted AFFO are all "per share" cash-flow figures and are easily confused. The label controls the meaning.

**Conflicting figures rule:** when two figures for the same metric appear to conflict, do not choose one immediately. First classify the difference: 1. different scope — group vs segment, consolidated vs ex-subsidiary · 2. different basis — gross vs net, reported vs adjusted · 3. different period — quarterly, annualized, LTM, fiscal year · 4. different currency · 5. different definition — company-defined vs packet-defined. Show both figures with provenance labels, then rate the pillar based on the figure that best matches the packet definition. If neither figure matches the packet definition, keep the pillar at Watch or Needs verification.

**Estimated proxy:** when a metric is calculated from available inputs but does not match the company's exact disclosed definition, label it **"Estimated proxy"** and state the inputs used. Examples: an AFFO payout proxy estimated above 100% when AFFO itself is not disclosed; an interest coverage proxy estimated from verified income-statement inputs but not company-disclosed; a net debt/EBITDAre proxy estimated when EBITDAre is not disclosed or JV/pro-rata treatment is unresolved. Never imply the proxy is the same as the company's official metric: a proxy is a sub-type of Estimated, is never Verified, never High confidence, and any rating that rests on it must say so.

**Guidance is not achievement:** guidance, targets, and management plans can support a Watch or directional comment, but they should not receive full Positive credit unless supported by achieved results, binding regulatory approval, or directly verified realized performance. This applies especially to: utilities rate-base growth guidance · REIT rent ramp / stabilized rent targets · energy production or capex targets · SaaS margin expansion targets · bank medium-term ROE targets.

**Expectations are not results (universal):** a price already contains a forecast, and a review that only compares multiples never states what that forecast is. Run this test whenever the valuation pillar would otherwise rest on a multiple above the company's own 5-year range, or whenever the market or management thesis rests on segments with no achieved results; otherwise record "expectations test not triggered" and move on. Invert the valuation — hold the current price fixed and solve for what it requires: revenue CAGR over a stated horizon, steady-state operating or FCF margin, reinvestment (sales-to-capital or reinvestment rate), the discount rate with its components, and a terminal growth rate no higher than the long-run risk-free rate. Convert the requirement into absolute end-of-horizon revenue and test it three ways: against the company's own achieved 5-year record, against the best verified peer analog at comparable scale, and against the current size of the market being addressed. **TAM × assumed share is not a valuation output — it is the assumption under test.** Where a sector packet defines an expectations adaptation, the adaptation governs the variables solved for and the value split; the triggers, caps and labels of this module still apply.

**Proven vs unproven enterprise value:** split EV into the part the proven business supports under the sector packet's normal valuation method and the residual the market is paying for optionality. A segment counts as proven only when the company discloses its revenue AND either its operating profit or a company-defined unit economic; anything else is unproven, is valued separately and labeled, and is never blended into the base multiple. Report the residual as a share of total EV. Rules: required inputs that exceed anything the company has achieved — or anything a verified peer has achieved at comparable scale — cap the valuation pillar at Watch unless the review names the specific verified evidence supporting the higher requirement · residual EV above ~50% of total EV caps the valuation pillar at Watch and obliges the conclusion to state the residual share, whatever the operating pillars show · disclosure too thin to build the test (no segment detail, no margin path) makes valuation **Needs verification**, never a favorable default · do not penalize the same optimism twice by both discounting the required growth and inflating the discount rate — pick one and say which.

**Estimated — expectations-implied:** every output of this test carries that label, a sub-type of Estimated. It is never Verified and never High confidence, because the solution depends on assumptions the review itself chose; only the inputs (price, period-end share count, net debt, disclosed segment figures) carry labels of their own. **Avoid:** analyst price targets as evidence of value · forward multiples built on margins the company has never achieved · "cheap versus its own history" when that history sits entirely inside one expansion regime · peer multiples where the peers are themselves priced on expectations.

## REIT cash-flow disambiguation

Five different things — never substitute one for another:

| Term | What it is |
|---|---|
| FFO (Nareit) | Net income + RE depreciation & amortization − gains on sales; the standardized base measure |
| Core FFO | Company-defined FFO with additional add-backs (transaction costs, impairments, etc.) — definitions vary by company |
| AFFO | FFO − recurring maintenance capex − straight-line rent; the cash measure that pays the dividend |
| Company-adjusted AFFO / FAD / CAD | Company-defined AFFO variants — add-backs differ; read the reconciliation table |
| GAAP net income / EPS | Distorted by depreciation; not a REIT cash-flow measure |

Rules: state which measure each figure is, using the company's own reconciliation table. Never compare one company's Core FFO to another's Nareit FFO. The **payout ratio must state its denominator** — dividends ÷ AFFO is the packet's preferred coverage measure; dividends ÷ FFO flatters coverage because FFO excludes maintenance capex. A payout that is comfortable on FFO and above 100% on AFFO is a Severe-flag candidate, not a comfortable dividend. If AFFO is not disclosed and not calculable, label dividend coverage "Needs verification" — do not silently substitute FFO.

## REIT operating-metric disambiguation

| Term | What it is |
|---|---|
| Same-property (same-store) NOI | NOI from properties owned in both periods — the organic growth measure |
| Total NOI | Includes acquisitions and developments — can mask organic decline |
| Physical occupancy | Space physically occupied |
| Leased occupancy | Space under signed leases, including not-yet-occupied — runs higher than physical |
| Economic occupancy | Rent-paying occupancy, adjusted for abatements and free rent |
| Lease spread (cash) | New rent vs prior rent on the same space, cash basis |
| Lease spread (straight-line/GAAP) | Includes future escalators — runs higher than cash spreads |

Rules: state which occupancy and which spread basis is quoted; never compare a leased-occupancy figure against a physical-occupancy threshold or a GAAP spread against a cash-spread history. Total NOI growth with negative same-property NOI is a Moderate flag (acquisitions masking organic decline), not growth.

## REIT debt definition rules

A leverage figure is incomplete until the output specifies: 1. gross debt or net debt · 2. EBITDA vs EBITDAre (Nareit) vs company-adjusted EBITDA · 3. LTM, annualized quarter, or fiscal year · 4. consolidated vs pro-rata share of JVs · 5. whether preferred equity is treated as debt. If any of these is unclear, label the metric **"Reported, pending direct verification"** or **"Needs verification"** — do not present an ambiguous ratio as Verified, and say which definition element is missing.

**Scope-dependence rule:** leverage figures reported at different scopes (e.g., consolidated vs pro-rata JV share) are scope-dependent rather than contradictory — report each figure with its scope stated. The balance-sheet pillar cannot rate above Watch until the packet's preferred net debt/EBITDAre basis is verified or soundly reconciled.

Debt structure must also be characterized: secured vs unsecured mix (heavily secured books pledge the best assets and narrow refinancing options) · fixed vs floating mix and hedge maturities (a "fixed" book whose swaps expire next year is floating-in-waiting) · **debt maturity wall** — list maturities for the next 24 months against available liquidity (cash + revolver capacity + free cash after dividends). A wall larger than liquidity without a stated refinancing plan is a Severe-flag candidate.

## Dividend safety rules

Dividend coverage is rated on AFFO payout, with the trend and the funding source: **Positive** — payout < 80% on AFFO, stable or falling · **Watch** — 80–90%, or rising toward 90%, or payout quoted only on FFO with AFFO unavailable · **Negative** — > 90% on AFFO, or dividend funded by debt, asset sales, or equity issuance. A recent dividend cut resets the history: rate the new dividend's coverage, but flag the cut. Verified does not mean safe — a verified 95% AFFO payout is Negative, full stop.

## Valuation logic

Do not use net income, EPS, or standard P/E — depreciation distorts all of them. Do not read a high dividend yield alone as cheap — **a very high yield usually signals an expected cut, not a bargain.** Use: P/FFO and P/AFFO (state which, and whose definition) · NAV premium/discount · implied cap rate vs private-market cap rates · AFFO dividend coverage. A deep NAV discount is only meaningful if the NAV inputs (cap rate, NOI) are stated; a discount to a stale NAV is Estimated at best.

## Default first-pass dashboard for REITs

Header must show: company / ticker · sector classification · property type · analysis date and data freshness · provisional score.

Then six to eight key metrics — use a table, not a long paragraph:

| Metric | Value | Rating | Provenance | Comment |
|---|---|---|---|---|
| FFO or AFFO per share (state which) | | | | |
| FFO/AFFO per-share growth | | | | |
| Dividend & payout ratio (state denominator) | | | | |
| Same-property NOI growth | | | | |
| Occupancy (state basis) | | | | |
| Net debt/EBITDAre (state definition status) | | | | |
| Interest coverage | | | | |
| Debt maturity wall / liquidity | | | | |

Then: red flags by severity (each with provenance status) · missing or unverified data, listed explicitly · neutral research conclusion.

The first-pass REIT score is always provisional unless: the AFFO definition and payout are resolved, the leverage definition is resolved, occupancy basis is stated, valuation data is current, and at least partial peer comparison is performed.

## REIT-specific "Verify missing data" action

When the user picks Verify missing data, prioritize in this order: 1. AFFO definition and payout ratio (from the supplemental reconciliation) · 2. net debt/EBITDAre definition (gross/net, -re basis, JV treatment, preferreds) · 3. debt maturity schedule next 24 months vs liquidity · 4. fixed/floating mix and hedge expiries · 5. same-property NOI definition and growth · 6. occupancy basis · 7. cash lease spreads · 8. NAV inputs (cap rate assumptions).

Other follow-up actions: deeper analysis · compare vs peers · deep dive: valuation · deep dive: risks · deep dive: dividend coverage / debt maturities / NAV · full research memo. Priority logic: payout above 90% or quoted only on FFO → verify coverage first. Maturity wall in next 24 months → verify liquidity before rating balance sheet. Occupancy falling with negative same-property NOI → deep dive portfolio quality.

## Score-change audit trail

Whenever a follow-up action changes the score, show all nine items: 1. previous score · 2. updated score · 3. metric that changed · 4. old status · 5. new verified value · 6. source document · 7. exact quote showing label and value · 8. pillar affected · 9. reason for the change.

Rules: if the exact quote cannot be provided, do not change the score — keep the metric at its prior label. A score changes only when the newly verified metric changes a pillar's Positive/Watch/Negative rating; verification alone does not automatically change the score.

## REIT data confidence rules

**High:** recent 10-K / 10-Q / supplemental information package / earnings release with the exact table label and value quoted. **Medium:** investor presentation with a labeled table; reputable provider cross-checked against filings; user-provided filing excerpts; reported values pending direct verification. **Low:** aggregator-only data, search-summary data, payout ratios with unstated denominators, NAV estimates with unstated inputs, unlabeled numbers.

Rules: price, P/FFO, and yield from aggregators may be used as Estimated. AFFO and EBITDAre are never High confidence unless the reconciliation or labeled table was read. If a key metric is Low confidence or missing, state how it affects the pillar score.

## What NOT to use

Net income, EPS, and standard P/E — depreciation distorts all of them; use P/FFO or P/AFFO. Standard FCF (growth capex makes it look weak). Dividend yield alone. Net debt/EBITDA without the '-re' adjustment. FFO payout as a substitute for AFFO payout.

## Common mistakes to avoid

Comparing Core FFO to Nareit FFO across companies · quoting a payout ratio without its denominator · treating leased occupancy as physical occupancy · reading GAAP lease spreads as cash spreads · taking total NOI growth at face value when same-property NOI is negative · presenting an ambiguous leverage ratio as verified · ignoring the secured/unsecured and fixed/floating mix · ignoring JV pro-rata debt · calling a high yield cheap · upgrading a pillar because a metric was found, even though the metric is still in Watch range · trusting a NAV discount whose inputs were never stated.

## Red flags

**Severe** — AFFO payout above 100% — the dividend is being funded by debt or asset sales · large debt maturities in the next 18 months with no refinancing plan or liquidity to cover them · going-concern language, covenant breach, or distressed exchange.

**Moderate** — occupancy falling while same-property NOI turns negative · persistent deep NAV discount with management issuing equity anyway · payout 90%+ on AFFO or coverage quoted only on FFO · heavily secured debt book narrowing refinancing options · floating-rate or hedge-expiry exposure large vs EBITDAre · total NOI growth masking negative same-property NOI · tenant or operator concentration with credit stress.

**Minor** — WALT shortening modestly year over year · small fixed-to-floating drift · one-quarter occupancy dip without NOI deterioration.

Grade findings Minor / Moderate / Severe and attach a provenance status to each before applying any cap.

## Scoring weights

| Pillar | Weight |
|---|---|
| FFO/AFFO per-share growth | 25% |
| Balance sheet (debt/EBITDAre, coverage, maturities) | 25% |
| Portfolio quality (occupancy, same-property NOI) | 20% |
| Dividend safety (AFFO payout) | 15% |
| Valuation (P/FFO, NAV, implied cap rate) | 15% |

Score each pillar 2 (Positive), 1 (Watch), 0 (Negative) vs peers and own history; weighted total ÷ 2 = 0–100%. ~75%+ strong on current evidence; 50–75% mixed — investigate the weak pillar; <50% with sufficient evidence and no verified Severe flag = weak on current evidence. Any verified Severe red flag caps the score at 50% until resolved; two or more usually mean high-risk / special situation. Verify flags against primary sources before capping. The score is a research organizer, not a prediction engine.

## Conclusion template

End with exactly one of: **strong on current evidence** / **mixed, needs more evidence** (name the evidence) / **weak on current evidence** (score <50% with sufficient evidence and no verified Severe flag) / **high-risk, special situation** / **insufficient data** — plus data confidence (High/Medium/Low) and a two-sentence thesis including what would break it. No buy/sell/hold language.

## Final sector checklist

1. Sector confirmed: most operating profit fits Real Estate / REITs.
2. Property type identified and stated; thresholds read against type-appropriate peers.
3. Peer group built on property type, geography, tenant base, growth stage, leverage profile.
4. REIT metrics labeled with provenance; Verified only with exact quoted labels from primary sources.
5. Cash-flow measures disambiguated: FFO, Core FFO, AFFO, company-adjusted AFFO kept separate; payout denominator stated.
6. Operating metrics disambiguated: same-property vs total NOI; occupancy and lease-spread basis stated.
7. Debt definition resolved: gross/net, EBITDAre basis, JV treatment, preferreds; secured/unsecured, fixed/floating, maturity wall characterized.
8. Dividend safety rated on AFFO payout with funding source.
9. "What NOT to use" respected.
10. Quality-of-earnings and geographic/currency checks run (Core Framework).
11. Red flags graded, provenance-labeled, and verified before applying the Severe cap.
12. Valuation done with P/FFO or P/AFFO, NAV, implied cap rate — not P/E or yield alone.
13. Weighted score computed; weakest pillar identified.
14. Score-change audit trail shown if any follow-up action changed the score.
15. Neutral research conclusion written with data confidence and unresolved gaps.

*This is general information only and not financial advice. For personal guidance, please talk to a licensed professional.*
