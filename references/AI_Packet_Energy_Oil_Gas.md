# AI Stock Review Packet: Energy (Oil & Gas)

**Version 2.2.3 — Last updated 2026-08-23.** v2.2.3 adds the expectations-embedded valuation module: the universal expectations test (reverse-solve the price for required growth, margin, reinvestment and discount rate), the proven-vs-unproven enterprise-value split with its valuation-pillar caps, and the "Estimated — expectations-implied" sub-label. v2.2.2 adds the weak-on-current-evidence conclusion category. v2.2.1 extends the v4 provenance labels (adds Calculated — verified inputs and Not disclosed; Severe-flag caps require verified evidence). Supersedes v2.1: upgraded from a general sector guide to a strict execution file (v4 verification and provenance standard, breakeven disambiguation, debt-definition rules, reserve verification rules, state-controlled-company checks, scoring and audit-trail rules). Educational framework — not investment advice. No buy/sell/hold language.

*Oil & gas exploration and production, integrated oil, midstream, refining* — GICS: Energy (Oil, Gas & Consumable Fuels)

**Core principle: Verified does not mean Positive.** Verification proves the number is real; the sector thresholds and the trend determine the rating. A verified net debt/EBITDA of 1.8x is still Watch. A verified reserve life of 7.8 years is still Watch.

## Prompt

> Analyze [company name / ticker] using the uploaded Core Framework and this Energy (Oil & Gas) guide.
> Do not use buy/sell/hold language.
> Provide: 1. Business model summary · 2. Sector classification and business type (E&P / integrated / midstream / refiner / mixed) · 3. Peer group with rationale · 4. Key energy metrics with provenance labels · 5. Values vs peers and 5-year history · 6. Positive/Watch/Negative assessment · 7. Severe red flags, if any · 8. Valuation (FCF yield, EV/DACF, NAV, breakeven sensitivity) · 9. Data confidence: High/Medium/Low · 10. Neutral research conclusion: strong on current evidence / mixed, needs more evidence / high-risk, special situation / insufficient data.
> Use primary sources (10-K, 10-Q, 20-F, 6-K, annual reports, reserve reports, earnings releases). Do not rely only on screeners or summaries.

## Business-type classification

Before scoring, state which the company is: **pure E&P**, **integrated oil**, **midstream**, **refiner**, or **mixed business**. Classify by where most **operating profit** (not revenue) comes from. For mixed businesses, run this packet on the dominant hydrocarbon segment and explicitly flag the other segments; in any deeper analysis, add a separate mini-pass or sum-of-the-parts note for the non-oil segment using its own sector logic (e.g., a transmission utility segment under the Utilities packet).

Sector context: profits ride a commodity price the company doesn't control. The best operators have low breakeven costs, strong free cash flow, and low debt so they survive crashes. Be precise about which 'breakeven' you mean — field-level, corporate, and dividend breakevens are different numbers.

## Key metrics & rule-of-thumb ranges

| Metric | Positive | Watch | Negative | How to read it |
|---|---|---|---|---|
| **FCF generation** | Strong & positive | Break-even | Negative | Capital discipline over drilling-for-growth is what gets rewarded. |
| **Corporate FCF breakeven** | < $45/bbl | $45–60 | > $60 | Oil price at which cash flow covers capex + interest. See breakeven disambiguation. |
| **Dividend breakeven** | < $50/bbl | $50–65 | > $65 | Price at which capex AND the base dividend are covered. |
| **Net debt/EBITDA** | < 1.5x | 1.5–2.5x | > 2.5x | Over-levered producers go bankrupt in price crashes. See debt definition rules. |
| **Reserve life (R/P)** | > 10 yrs | 7–10 yrs | < 7 yrs | Years of production left in proven reserves. |
| **Reserve replacement** | > 100% | 80–100% | < 80% | Below 100% the company is liquidating itself. |
| **Shareholder yield** | > 5% | 2–5% | Cut | Dividends + buybacks are now the main draw of the sector. |

**Formulas:** Field-level (half-cycle) breakeven = operating cost + sustaining capex per barrel for a specific field. Corporate FCF breakeven = the commodity price at which operating cash flow = total capex + interest, company-wide. Dividend breakeven = the price at which operating cash flow covers capex + the base dividend. Reserve life (R/P) = proven reserves ÷ annual production. Reserve replacement ratio = reserves added ÷ reserves produced. Shareholder yield = (dividends + net buybacks) ÷ market cap. Dividend coverage = FCF ÷ dividends paid.

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

## Energy metric verification standard

A metric is **Verified** only when the output includes all seven evidence items: 1. metric name · 2. exact value · 3. source document (filing type and date) · 4. exact table, note, or section · 5. short quote showing the metric label next to the value · 6. definition match to this guide · 7. score impact.

Search summaries, aggregator snippets, and unlabeled extracted numbers cannot verify energy metrics. Never reuse a number from a nearby table unless the label exactly matches the intended metric — production figures, sales volumes, throughput, and reserve figures are all "barrels" and are easily confused. The label controls the meaning.

**Conflicting figures rule:** when two figures for the same metric appear to conflict, do not choose one immediately. First classify the difference: 1. different scope — group vs segment, consolidated vs ex-subsidiary · 2. different basis — gross vs net, reported vs adjusted · 3. different period — quarterly, annualized, LTM, fiscal year · 4. different currency · 5. different definition — company-defined vs packet-defined. Show both figures with provenance labels, then rate the pillar based on the figure that best matches the packet definition. If neither figure matches the packet definition, keep the pillar at Watch or Needs verification.

**Estimated proxy:** when a metric is calculated from available inputs but does not match the company's exact disclosed definition, label it **"Estimated proxy"** and state the inputs used. Examples: an AFFO payout proxy estimated above 100% when AFFO itself is not disclosed; an interest coverage proxy estimated from verified income-statement inputs but not company-disclosed; a net debt/EBITDAre proxy estimated when EBITDAre is not disclosed or JV/pro-rata treatment is unresolved. Never imply the proxy is the same as the company's official metric: a proxy is a sub-type of Estimated, is never Verified, never High confidence, and any rating that rests on it must say so.

**Guidance is not achievement:** guidance, targets, and management plans can support a Watch or directional comment, but they should not receive full Positive credit unless supported by achieved results, binding regulatory approval, or directly verified realized performance. This applies especially to: utilities rate-base growth guidance · REIT rent ramp / stabilized rent targets · energy production or capex targets · SaaS margin expansion targets · bank medium-term ROE targets.

**Expectations are not results (universal):** a price already contains a forecast, and a review that only compares multiples never states what that forecast is. Run this test whenever the valuation pillar would otherwise rest on a multiple above the company's own 5-year range, or whenever the market or management thesis rests on segments with no achieved results; otherwise record "expectations test not triggered" and move on. Invert the valuation — hold the current price fixed and solve for what it requires: revenue CAGR over a stated horizon, steady-state operating or FCF margin, reinvestment (sales-to-capital or reinvestment rate), the discount rate with its components, and a terminal growth rate no higher than the long-run risk-free rate. Convert the requirement into absolute end-of-horizon revenue and test it three ways: against the company's own achieved 5-year record, against the best verified peer analog at comparable scale, and against the current size of the market being addressed. **TAM × assumed share is not a valuation output — it is the assumption under test.**

**Proven vs unproven enterprise value:** split EV into the part the proven business supports under the sector packet's normal valuation method and the residual the market is paying for optionality. A segment counts as proven only when the company discloses its revenue AND either its operating profit or a company-defined unit economic; anything else is unproven, is valued separately and labeled, and is never blended into the base multiple. Report the residual as a share of total EV. Rules: required inputs that exceed anything the company has achieved — or anything a verified peer has achieved at comparable scale — cap the valuation pillar at Watch unless the review names the specific verified evidence supporting the higher requirement · residual EV above ~50% of total EV caps the valuation pillar at Watch and obliges the conclusion to state the residual share, whatever the operating pillars show · disclosure too thin to build the test (no segment detail, no margin path) makes valuation **Needs verification**, never a favorable default · do not penalize the same optimism twice by both discounting the required growth and inflating the discount rate — pick one and say which.

**Estimated — expectations-implied:** every output of this test carries that label, a sub-type of Estimated. It is never Verified and never High confidence, because the solution depends on assumptions the review itself chose; only the inputs (price, period-end share count, net debt, disclosed segment figures) carry labels of their own. **Avoid:** analyst price targets as evidence of value · forward multiples built on margins the company has never achieved · "cheap versus its own history" when that history sits entirely inside one expansion regime · peer multiples where the peers are themselves priced on expectations.

## FCF definition rules

Management-defined or transcript FCF is not interchangeable with OCF minus organic investment. The two often differ through divestments, inorganic capex, working-capital effects, leases, or interest treatment. Report each separately with its own provenance label — e.g., "OCF − organic investments: Estimated" alongside "Management/transcript FCF: Reported, pending direct verification" — and flag the definition gap as needing reconciliation. Do not treat a management FCF figure as equivalent to OCF − capex unless the source definition is verified.

## Breakeven disambiguation

Three different things — never substitute one for another:

| Term | What it is |
|---|---|
| Field-level (half-cycle) breakeven | Operating cost + sustaining capex for one field — the lowest, most-marketed number; excludes overhead, interest, dividends |
| Corporate FCF breakeven | Company-wide price at which operating cash flow covers total capex + interest |
| Dividend breakeven | Company-wide price at which operating cash flow covers capex + the base dividend |

Rules: never treat a company-marketed field breakeven as a corporate breakeven. Corporate FCF breakeven is labeled **Verified** only if directly disclosed and quoted from the source; **Estimated** if calculated from assumptions (state them); **Needs verification** if not disclosed and not calculable from available data. If only a field breakeven is found, report it as such and keep corporate breakeven at Needs verification.

## Debt / EBITDA definition rules

A leverage figure is incomplete until the output specifies: 1. gross debt or net debt · 2. LTM or annualized EBITDA · 3. consolidated group or segment basis · 4. whether leases are included · 5. currency. If any of these is unclear, label the metric **"Reported, pending direct verification"** or **"Needs verification"** — do not present an ambiguous ratio as Verified, and say which definition element is missing. For groups with large non-recourse or subsidiary debt (e.g., a consolidated utility segment), note whether the ratio is distorted by consolidation.

**Scope-dependence rule:** leverage figures reported at different scopes (e.g., consolidated group vs excluding a consolidated segment) are scope-dependent rather than contradictory — report each figure with its scope stated. Standard wording: "Debt figures are scope-dependent rather than contradictory. Balance sheet remains Watch because the packet's preferred net debt/EBITDA basis is not directly verified." The balance-sheet pillar cannot rate above Watch until the preferred net basis is verified or soundly reconciled.

## Reserve metrics rules

Proven reserves, reserve life, and reserve replacement ratio must be verified from reserve filings, annual reports (20-F/10-K reserve tables), or official reserve releases — not from aggregators. Scoring: reserve life 7–10 years rates **Watch** even when verified. Reserve replacement above 100% rates **Positive** unless the additions are low quality or one-off — price-driven revisions, royalty/contract allocations, or purchases rather than drilling and recovery performance; in that case rate Watch and say why. State the as-of date; reserve data more than one annual cycle old carries a staleness caveat.

## Integrated and mixed-business rules

If the company owns material non-oil segments, classify by the dominant operating-profit driver but flag the other segment in the scorecard header and red-flag section.

**Ecopetrol-specific:** use this Energy (Oil & Gas) packet as the main packet. Flag ISA as a utilities/transmission segment. In any deeper analysis, include a separate mini-pass or sum-of-the-parts note for ISA under utilities logic (regulated returns, FFO/debt, concession duration), not oil & gas logic.

## State-controlled oil companies — governance / political-risk check

For any company with a government as controlling shareholder, add a required check covering: 1. state ownership percentage and control mechanics · 2. dividend policy influenced by government fiscal needs · 3. fuel-price controls or government receivables · 4. tax/royalty changes and exposure to fiscal-regime shifts · 5. capital allocation driven by policy rather than returns (mandated investments, social spending, forced acquisitions). Grade findings into the red-flag list; persistent policy-driven capital allocation is at least Moderate.

**Ecopetrol-specific — FEPC is a required item.** Every Ecopetrol review must report: 1. FEPC receivable balance · 2. whether it is rising or falling · 3. cash-flow impact · 4. government-payment timing · 5. provenance label. If the balance cannot be read from a primary source, report "FEPC balance — Needs verification" and name the best source to check (quarterly results report, 20-F related-party note).

## Valuation logic

Do not describe a low P/E as cheap by itself. **"Low P/E at high Brent prices can be a value trap if earnings are peak-cycle."**

Use: FCF yield at current or strip prices · EV/DACF · NAV of proved reserves · breakeven sensitivity across price scenarios · dividend coverage (FCF ÷ dividends). Avoid: low P/E at peak commodity prices · company-marketed field breakevens presented as corporate breakevens · cross-cycle EV/EBITDA comparisons.

Valuation review connects the multiple to the cycle: a low multiple on peak-cycle cash flow is at least Watch unless breakeven and balance-sheet strength support resilience at mid-cycle prices.

## Default first-pass dashboard for energy

Header must show: company / ticker · sector classification · business type (pure E&P / integrated / midstream / refiner / mixed, with non-oil segments flagged) · analysis date and data freshness · provisional score.

Then six to eight key metrics — use a table, not a long paragraph:

| Metric | Value | Rating | Provenance | Comment |
|---|---|---|---|---|
| Production | | | | |
| EBITDA or operating cash flow | | | | |
| FCF generation | | | | |
| Corporate FCF breakeven | | | | |
| Net debt/EBITDA | | | | |
| Reserve life | | | | |
| Reserve replacement | | | | |
| Shareholder yield or dividend coverage | | | | |

Then: red flags by severity (each with provenance status) · missing or unverified data, listed explicitly · neutral research conclusion.

The first-pass energy score is always provisional unless: breakeven verified or soundly estimated, leverage definition resolved, reserve data verified from reserve filings, valuation data current, and at least partial peer comparison performed.

## Energy-specific "Verify missing data" action

When the user picks Verify missing data, prioritize in this order: 1. corporate FCF breakeven · 2. dividend breakeven · 3. net debt/EBITDA definition (gross/net, LTM, basis, leases, currency) · 4. FEPC receivable or equivalent government receivable · 5. hedge position (volumes, prices, tenor, roll-off) · 6. reserve-life calculation (reserves ÷ current production, stated basis) · 7. dividend coverage (FCF vs dividends paid) · 8. Brent sensitivity (disclosed EBITDA/FCF impact per $1/bbl).

Other follow-up actions: deeper analysis · compare vs peers · deep dive: valuation · deep dive: risks · deep dive: breakevens & capital discipline · full research memo. Priority logic: breakeven missing → verify first. Leverage ambiguous → resolve definition before rating balance sheet above Watch. Reserve life under 10 years → check replacement quality. State-controlled → run the governance/political check before concluding.

## Score-change audit trail

Whenever a follow-up action changes the score, show all nine items: 1. previous score · 2. updated score · 3. metric that changed · 4. old status · 5. new verified value · 6. source document · 7. exact quote showing label and value · 8. pillar affected · 9. reason for the change.

Rules: if the exact quote cannot be provided, do not change the score — keep the metric at its prior label. A score changes only when the newly verified metric changes a pillar's Positive/Watch/Negative rating; verification alone does not automatically change the score.

## Energy data confidence rules

**High:** recent 10-K / 10-Q / 20-F / 6-K / reserve report / audited statements, with the exact table label and value quoted. **Medium:** company earnings release or investor presentation with a labeled table; reputable provider cross-checked against filings; user-provided filing excerpts; reported values pending direct verification. **Low:** aggregator-only data, search-summary data, incomplete disclosure, estimated breakevens without stated assumptions, unlabeled numbers.

Rules: price, market cap, and yield from aggregators may be used as Estimated. Breakevens and reserve metrics are never High confidence unless the source clearly labels them. If a key metric is Low confidence or missing, state how it affects the pillar score.

## What NOT to use

A low P/E at high commodity prices — peak-cycle earnings make expensive stocks look cheap (the classic trap). Company-marketed field breakevens as if they were corporate breakevens. EV/EBITDA comparisons across the cycle.

## Common mistakes to avoid

Treating field breakevens as corporate breakevens · calling low P/E "cheap" at peak Brent · presenting an ambiguous debt ratio as verified · taking reserve replacement at face value without checking addition quality · ignoring government receivables and price controls at state-controlled companies · rating the balance sheet on a ratio whose gross/net basis is unknown · upgrading a pillar because a metric was found, even though the metric is still in Watch range · ignoring hedge roll-off into weaker prices · ignoring FX mismatch between USD debt and local-currency costs or revenue.

## Red flags

**Severe** — high debt heading into a price downturn · liquidity stress, covenant pressure, or going-concern language · verified rapid, policy-driven cash drain (e.g., an uncollected government receivable large and growing vs operating cash flow).

**Moderate** — aggressive capex growth at cycle peaks (history rhymes) · reserve replacement persistently below 100% · state-driven capital allocation, fuel-price controls, or dividend policy set by government fiscal needs · leadership instability or governance turnover at state-controlled companies · low-quality reserve additions masking organic decline.

**Minor** — hedge book rolling off into a weaker price environment · FX mismatch between debt currency and revenue/cost currencies · single-quarter production misses from weather or maintenance.

Grade findings Minor / Moderate / Severe and attach a provenance status to each before applying any cap.

## Scoring weights

| Pillar | Weight |
|---|---|
| Cost position / breakevens | 30% |
| Capital discipline & FCF | 25% |
| Balance sheet | 20% |
| Reserves (life, replacement) | 10% |
| Valuation (FCF yield, EV/DACF) | 15% |

Score each pillar 2 (Positive), 1 (Watch), 0 (Negative) vs peers and own history; weighted total ÷ 2 = 0–100%. ~75%+ strong on current evidence; 50–75% mixed — investigate the weak pillar; <50% with sufficient evidence and no verified Severe flag = weak on current evidence. Any verified Severe red flag caps the score at 50% until resolved; two or more usually mean high-risk / special situation. Verify flags against primary sources before capping. The score is a research organizer, not a prediction engine.

## Conclusion template

End with exactly one of: **strong on current evidence** / **mixed, needs more evidence** (name the evidence) / **weak on current evidence** (score <50% with sufficient evidence and no verified Severe flag) / **high-risk, special situation** / **insufficient data** — plus data confidence (High/Medium/Low) and a two-sentence thesis including what would break it. No buy/sell/hold language.

## Final sector checklist

1. Sector confirmed: most operating profit fits Energy (Oil & Gas).
2. Business type identified: pure E&P, integrated, midstream, refiner, or mixed — non-oil segments flagged.
3. Peer group built on business model, geography, cost position, fiscal regime, growth stage.
4. Energy metrics labeled with provenance; Verified only with exact quoted labels from primary sources.
5. Breakevens disambiguated: field-level, corporate FCF, dividend kept separate.
6. Debt ratio definition resolved: gross/net, LTM, basis, leases, currency.
7. Reserve metrics verified from reserve filings; addition quality checked.
8. State-control governance/political check run where applicable (FEPC for Ecopetrol).
9. "What NOT to use" respected.
10. Quality-of-earnings and geographic/currency checks run (Core Framework).
11. Red flags graded, provenance-labeled, and verified before applying the Severe cap.
12. Valuation done with FCF yield, EV/DACF, NAV, breakeven sensitivity, dividend coverage — not standalone P/E.
13. Weighted score computed; weakest pillar identified.
14. Score-change audit trail shown if any follow-up action changed the score.
15. Neutral research conclusion written with data confidence and unresolved gaps.

*This is general information only and not financial advice. For personal guidance, please talk to a licensed professional.*
