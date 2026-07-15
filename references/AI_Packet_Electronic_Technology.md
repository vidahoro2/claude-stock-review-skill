# AI Stock Review Packet: Electronic Technology

**Version 2.2.2 — Last updated 2026-07-13.** v2.2.2 corrections: DIO period basis, ROIC invested-capital definition, cycle sub-score de-duplication (margin informs phase, not points), undetermined-cycle conclusion cap, adjusted R&D intensity, mid-cycle revenue caveat, impact-based export-control severity, staged subsidy credit, defense funding-cycle labels, fifth conclusion category. Supersedes v2.1: upgraded from a general sector guide to a strict execution file (v4 verification and provenance standard, cycle-position rules, inventory and book-to-bill rules, concentration and export-control rules, capital-intensity rules, subsector adjustments, scoring and audit-trail rules). Introduced in v2.2.1 with the extended v4 provenance labels and corrected scoring/display rules of 2026-07-13. Educational framework — not investment advice. No buy/sell/hold language.

*Semiconductors, semicap equipment, hardware, computers, networking, EMS/ODM, components, defense electronics* — GICS: Information Technology (Semiconductors & Semi Equipment; Technology Hardware) — defense electronics sit in Industrials (Aerospace & Defense)

**Core principle: establish cycle position before rating anything.** The classic trap in this sector is a low P/E on peak-cycle earnings — cyclicals look cheapest at the top and most expensive at the bottom. A verified 12x trailing P/E means nothing until the review states where margins sit versus their own 5–10 year range. Verified does not mean Positive.

## Prompt

> Analyze [company name / ticker] using the uploaded Core Framework and this Electronic Technology guide.
> Do not use buy/sell/hold language.
> Provide: 1. Business model summary · 2. Sector and subsector classification · 3. Peer group with rationale · 4. Key sector metrics with provenance labels · 5. Values vs peers and 5-year history · 6. Positive/Watch/Negative assessment with stated cycle position · 7. Severe red flags, if any · 8. Valuation (mid-cycle multiples) · 9. Data confidence: High/Medium/Low · 10. Neutral research conclusion: strong on current evidence / mixed, needs more evidence / high-risk, special situation / insufficient data.
> Use primary sources (10-K, 10-Q, 20-F, 6-K, annual reports, earnings releases, order/backlog disclosures). Do not rely only on screeners or summaries.

## Key metrics & rule-of-thumb ranges

| Metric | Positive | Watch | Negative | How to read it |
|---|---|---|---|---|
| **Revenue growth** | > 10% multi-year | 0–10% | Declining trend | Very cyclical — rate the multi-year trend and cycle position, never one quarter |
| **Gross margin** | Subsector top-half & stable/rising | Middling or drifting | Bottom-quartile or falling fast | Thresholds are subsector-specific — see subsector adjustments; never compare across models |
| **Adjusted R&D intensity** | In subsector band & productive | Drifting vs own history | Below subsector norm while peers accelerate | (Expensed + capitalized development) ÷ revenue; rough designer band 8–20% — always judge vs subsector and own 5-year range, see R&D rules |
| **Inventory days** | Stable/falling vs own history | Rising slowly | Rising fast while revenue slows | See inventory rules — the sector's best early-warning signal |
| **Book-to-bill / backlog** | > 1.0 and rising | ~1.0 | < 1.0 for 2+ quarters | Orders vs shipments; verify definition — see order-signal rules |
| **Capex % of revenue** | In subsector band | Above band with plan | Above band, no returns evidence | Foundry/memory 25–50% is normal; fabless < 5%; see capital-intensity rules |
| **ROIC (through cycle)** | > WACC across the cycle | Positive but peak-dependent | Below WACC at mid-cycle | Average 5 years, not the best year |
| **Customer concentration** | No customer > 10% | One 10–20% | > 20% or top-2 > 30% | 10-K discloses > 10% customers; see concentration rules |
| **Net debt/EBITDA** | < 1.5x (or net cash) | 1.5–3x | > 3x | Cyclicals need low leverage to survive downturns; use mid-cycle EBITDA |
| **Net share dilution / yr** | < 2% | 2–4% | > 4% | Period-end shares outstanding trend (split-adjusted); buybacks that merely offset SBC are not return of capital |
| **P/E vs cycle** | See valuation rules | — | — | Never rate the multiple without stating cycle position |

**Formulas:** Gross margin = gross profit ÷ revenue. Adjusted R&D intensity = (expensed R&D + capitalized development expenditure) ÷ revenue — the adjustment neutralizes the GAAP (expense) vs IFRS (capitalize qualifying development) gap. Inventory days (DIO) = average inventory ÷ COGS for the measurement period × days in that period — 365 only with annual/LTM COGS; ~91 for a quarter; COGS basis, never revenue basis; state the averaging method. Book-to-bill = company-defined accepted-order measure ÷ consistently scoped shipment/billings/revenue measure. Capex intensity = purchases of property and equipment ÷ revenue. ROIC = NOPAT ÷ average invested capital, where invested capital = operating working capital + net PP&E + operating lease assets + capitalized development assets + other material operating assets — state whether goodwill and acquired intangibles are included. Through-cycle ROIC = multi-year NOPAT ÷ corresponding average invested capital, not an average of annual ratios. Net debt/EBITDA = (total debt − cash and equivalents) ÷ EBITDA (state whether EBITDA is trailing or mid-cycle). Net dilution = change in period-end common shares outstanding (split-adjusted) ÷ prior-year count; diluted weighted-average shares are a supporting measure only. Packet FCF = operating cash flow − purchases of property and equipment − separately reported capitalized development costs not already included in that line.

## Electronic Technology metric verification standard

A sector metric is not "verified" unless the output includes all seven evidence items:

1. Metric name
2. Exact value
3. Source document
4. Exact table, note, or section
5. Short quote showing the metric label next to the value
6. Definition match to this guide (or the company definition, stated)
7. Score impact

Rules: search summaries, aggregator snippets, and unlabeled extracted numbers cannot verify sector metrics. Do not treat a number as verified because a search result or third-party summary claims it came from a filing. Never reuse a percentage from a nearby table unless the label exactly matches the intended metric. If the label is not visible next to the value, the metric is not verified. If the metric cannot be verified, mark it "Needs verification."

**Known traps:** "inventory days" appears on both COGS and revenue bases — the label and denominator control the meaning. "Backlog" may be total, funded, unfunded, or RPO — never mix definitions across periods. Segment gross margin ≠ consolidated gross margin. Non-GAAP gross margin in semis often excludes amortization of acquired intangibles — state which basis is used. Book-to-bill is frequently disclosed only in earnings calls or presentations, not filings.

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

## Shared rules

**Conflicting figures rule (universal):** when two figures for the same metric appear to conflict, do not choose one immediately. First classify the difference: 1. different scope — group vs segment, consolidated vs ex-subsidiary · 2. different basis — gross vs net, reported vs adjusted · 3. different period — quarterly, annualized, LTM, fiscal year · 4. different currency · 5. different definition — company-defined vs packet-defined. Show both figures with provenance labels, then rate the pillar based on the figure that best matches the packet definition. If neither figure matches the packet definition, keep the pillar at Watch or Needs verification.

**Estimated proxy:** when a metric is calculated from available inputs but does not match the company's exact disclosed definition, label it **"Estimated proxy"** and state the inputs used. Examples: an AFFO payout proxy estimated above 100% when AFFO itself is not disclosed; an interest coverage proxy estimated from verified income-statement inputs but not company-disclosed; a net debt/EBITDAre proxy estimated when EBITDAre is not disclosed or JV/pro-rata treatment is unresolved. Never imply the proxy is the same as the company's official metric: a proxy is a sub-type of Estimated, is never Verified, never High confidence, and any rating that rests on it must say so.

**Guidance is not achievement:** guidance, targets, and management plans can support a Watch or directional comment, but they should not receive full Positive credit unless supported by achieved results, binding regulatory approval, or directly verified realized performance. This applies especially to: utilities rate-base growth guidance · REIT rent ramp / stabilized rent targets · energy production or capex targets · SaaS margin expansion targets · bank medium-term ROE targets.

## Cycle-position rules

Every review must state an explicit cycle-position estimate — **early upturn / mid-cycle / late cycle-peak / downturn** — with the evidence behind it. Evidence sources, in order of usefulness: own inventory days trend · customer and channel inventory commentary · book-to-bill and order/backlog trend · gross margin vs own 5–10 year range · industry utilization and lead-time data (Estimated at best) · memory/component pricing where relevant.

Rules: margins at or near a 5–10 year high are peak evidence, not quality evidence — do not extrapolate them. Margin-vs-own-range informs the STATED cycle phase but earns no points in the cycle pillar — the cycle score is driven by inventory, orders, and utilization/pricing/channel evidence (prevents one gross-margin print from scoring in two pillars). A low trailing P/E combined with peak-range margins rates the valuation pillar Watch at best, never Positive on cheapness alone. A high trailing P/E at trough margins is not automatically Negative. If cycle position cannot be estimated from evidence, state "cycle position: undetermined", cap BOTH the cycle pillar and the valuation pillar at Watch, and cap the overall conclusion at "mixed, needs more evidence" regardless of the numerical score. Rate growth on the multi-year trend through the cycle; annualizing a single peak or trough quarter is never acceptable. Defense electronics uses its own phase labels — see the subsector adjustment.

## Inventory & order-signal rules

Inventory: compute DIO on the COGS basis and rate the trend vs own history, not a universal threshold. Inventory growing materially faster than forward revenue for 2+ quarters is a Moderate flag; combined with falling revenue and cut guidance it is Severe (demand miss plus writedown risk). Distinguish deliberate strategic builds (announced buffer stock, new product ramp, supply-security purchases) from involuntary builds — a strategic build claimed by management without disclosure of sell-through evidence stays Watch (guidance is not achievement). Check purchase obligations and prepayments to suppliers in the commitments note — off-balance-sheet demand risk.

Orders: book-to-bill above 1.0 supports Positive only with the company's definition verified (accepted orders vs nonbinding indications; billings vs revenue; segment vs group) — never compute it when numerator and denominator differ in scope, product, currency, or period. For lumpy semicap and defense businesses prefer a trailing-four-quarter measure, and check cancellations and pushouts before crediting order strength. Backlog must be labeled by type: total vs funded vs RPO. Book-to-bill below 1.0 for 2+ quarters is a Moderate flag. If order metrics are not disclosed (**Not disclosed**), rely on inventory, deferred revenue, and customer commentary — and say so; do not silently substitute an aggregator's estimate.

## Concentration & export-control rules

Customer concentration: 10-K/20-F risk factors and segment notes disclose customers above 10% of revenue — a disclosure trigger, not automatically a quality judgment. One customer > 20%, or top-2 > 30%, caps the relevant pillar at Watch even with strong current results; whether it stays Watch or worsens depends on context: distributor vs end customer, contract duration and cancellation rights, switching/qualification costs, customer financial strength, program diversity within one corporate customer, and time to replace the revenue. Semicap concentration is structural (few buyers) — default Watch, judged on relationship durability. Loss or major order cut from a >10% customer is a Severe flag when verified.

Supply concentration: single-source fab dependence (one foundry, one packaging/test provider, one EUV supplier) is a structural risk — state it; it justifies Watch when combined with geopolitical exposure.

Export controls & geopolitics: state China (and other restricted-market) revenue % where disclosed — and whether that figure is customer location, billing destination, shipping destination, or end use. Check the applicable rules as of the analysis date (they change often, and licensing pathways, thresholds, and transition periods exist). A verified restriction is Severe only when it is reasonably likely to cause a material, insufficiently mitigated effect on revenue, profit, inventory, or strategic capacity — keep three provenance strands separate: regulatory scope (verifiable from the regulator), company exposure (verifiable from the company), and financial effect (usually Estimated until management evidence exists).

Subsidies (CHIPS-type grants, government prepayments) get staged credit: announced or preliminary → no financial credit · finalized award with enforceable terms → limited Watch-level credit, adjusted for conditions · milestone earned or cash received → realized credit. Never include the full face value of a conditional award in liquidity, FCF, or valuation.

## Capital-intensity & R&D rules

Capex bands by subsector: foundry/memory/IDM 25–50% of revenue · semicap equipment 5–15% · fabless/design < 5% · hardware/devices 2–8% · EMS/ODM 1–4%. Capex above band needs evidence of returns (utilization commitments, prepaid customer agreements, binding subsidies) — otherwise Watch. Depreciation-life extensions that flatter margins are a quality-of-earnings flag. Use adjusted R&D intensity (expensed + capitalized development) and judge it against the subsector peer group and the company's own 5-year range, alongside absolute R&D growth and evidence of productive output (product cadence, design wins). A declining R&D ratio is not automatically Negative when revenue grows faster and absolute spend stays strong; adjusted intensity below subsector norm while competitors accelerate is a slow-burning Negative; R&D cut during a downturn to protect margins is Watch with a note. SBC follows the corrected standard: read from the cash-flow statement; rate dilution primarily on period-end shares outstanding (split-adjusted) over 3–5 years; buybacks earn capital-allocation credit only when the period-end count actually falls after SBC and acquisition issuance.

## Subsector adjustments

Classify the subsector first; the main table assumes IP-rich semis.

**Fabless / design & IP** — gross margin 50–70%+ normal; capex minimal; the risks are customer concentration, single-foundry dependence, and design-win cycles. Watch: R&D intensity vs peers, licensing vs product mix.

**Foundry / IDM / memory** — capital-intensity rules dominate; gross margin swings violently with utilization and pricing (memory especially). Use mid-cycle margins and through-cycle ROIC; book value and replacement cost are relevant valuation cross-checks. Memory: pricing trend is the cycle signal.

**Semicap equipment** — order-driven: book-to-bill, backlog, and customer capex plans lead revenue by 2–4 quarters. Service/installed-base revenue is the stabilizer — separate it. Customer concentration is structural (few buyers).

**Hardware / devices / networking** — ASP and unit trends matter as much as revenue; separate hardware margin from services/attach margin; channel inventory is the hidden risk. Gross margin 30–45% typical; premium brands higher.

**EMS / ODM contract manufacturers** — override the main table: gross margin 5–10% and operating margin 2–5% are normal, not Negative. Judge on ROIC, cash conversion cycle, customer concentration, and net debt. Valuation on P/E or EV/EBIT, never EV/Sales.

**Defense electronics** — backlog-driven, not chip-cycle-driven. Replace the semiconductor phase labels with: **funding/awards expansion / stable funded demand / program normalization / funding contraction / undetermined**. Assess execution separately: funded vs unfunded backlog, book-to-bill, program concentration, cost-plus vs fixed-price mix (fixed-price development transfers substantial cost and execution risk to the contractor — watch estimate-at-completion changes and loss provisions, not the contract type alone). GICS puts these in Industrials — peers are defense primes and suppliers, not semis.

**Hybrid routing:** majority-software/services operating profit (platforms, subscription-attached devices) → Software & SaaS packet with a hardware note. Distribution-heavy models → Distribution Services. Auto/industrial component makers with commodity economics → Producer Manufacturing may fit better. Classify by where most normalized operating profit comes from; if no segment clearly dominates, treat as mixed and state which packets cover which segments.

## Valuation rules

State the assumed cycle position in every valuation rating; if undetermined, the valuation pillar caps at Watch. Use: mid-cycle P/E — normalized margin on normalized revenue; current revenue is acceptable only when evidence shows volumes and pricing are already near normal cycle levels, otherwise state the revenue assumption and label the result Estimated proxy (a mid-cycle estimate on verified inputs is at best Calculated — verified inputs) · EV/EBITDA vs own 5–10 year range and peer median/interquartile range · FCF yield through the cycle (packet FCF) · P/B or replacement-cost cross-check for foundry/memory · PEG only for structurally growing, less-cyclical names. Adjust EV for net cash — many semis carry large net cash that flatters P/E.

Rules: never rate valuation Positive on a trailing multiple computed from peak-range margins. EV/Sales is acceptable only for high-growth names with verified structural (not cyclical) growth — and requires the same durability evidence as in the Software & SaaS packet. **Avoid:** trailing P/E at cycle extremes without stating cycle position · annualized single-quarter earnings · cross-model margin or multiple comparisons (fabless vs foundry vs EMS) · TAM-based valuation narratives (guidance is not achievement).

## Default first-pass dashboard for Electronic Technology

Six cards: 1. Growth & cycle position (multi-year revenue trend, stated cycle phase) · 2. Margins & pricing (gross margin vs own range and subsector, ASP/mix) · 3. Inventory & orders (DIO trend, book-to-bill/backlog) · 4. Investment & returns (capex intensity, R&D intensity, through-cycle ROIC) · 5. Balance sheet & dilution (net debt/EBITDA, net cash, period-end share count) · 6. Valuation (mid-cycle multiple vs own history and peers, net-cash adjusted).

Each card shows: value · Positive/Watch/Negative rating · provenance label (per the v4 standard) · one-line explanation. Use concise tables, not long paragraphs.

The first-pass score is always provisional unless: revenue, gross margin, inventory, and share count verified from filings; cycle position stated with evidence; and at least partial peer comparison performed.

## Follow-up actions

Offer: 1. Verify cycle position (inventory, orders, margin range) · 2. Deep dive: customer/supply concentration and export controls · 3. Deep dive: capital intensity and subsidy dependence · 4. Deep dive: valuation vs mid-cycle · 5. Compare vs subsector peers · 6. Deep dive: quality of earnings (depreciation lives, capitalized costs, purchase obligations) · 7. Deep dive: defense backlog and program mix (defense electronics only).

Priority logic: margins near multi-year highs with a low trailing P/E → recommend 1 then 4. Inventory rising while revenue slows → recommend 1. Customer > 10% or China revenue material → recommend 2. Capex above band or subsidy-dependent plans → recommend 3. EMS/ODM or defense subsector → recommend 5 with the right peer set.

## Score-change audit trail

Whenever a follow-up action changes the score, show all nine items: 1. previous score · 2. updated score · 3. metric that changed · 4. old status · 5. new verified value · 6. source document · 7. exact quote showing label and value · 8. pillar affected · 9. reason for the change.

Rules: if the exact quote cannot be provided, do not change the score — keep the metric at Needs verification. A score changes only when the newly verified metric changes a pillar's Positive/Watch/Negative rating; verification alone does not automatically change the score.

## Data confidence rules

**High:** recent 10-K / 10-Q / 20-F / 6-K / audited annual report with the exact table label and value quoted — covers revenue, gross margin, inventory, capex, R&D, share count, customer-concentration disclosures. **Medium:** earnings release or investor presentation with a labeled table — often the only home of book-to-bill, backlog, ASP commentary, and utilization; these can never be High confidence unless labeled in a filing. **Low:** aggregator-only data, industry-association estimates, channel checks, third-party utilization or pricing data, unlabeled numbers.

Rules: price and EV from aggregators may be used as Estimated. Industry cycle data (WSTS-type forecasts, third-party pricing) is context, never verification. If a key metric is Low confidence, state how it affects the pillar score.

## What NOT to use

Trailing P/E near a cycle peak without stating cycle position. Single-quarter growth rates or annualized single quarters. Margin or multiple comparisons across business models (fabless vs foundry vs EMS vs defense). EV/Sales for mature cyclicals. TAM projections as achievement. "Adjusted" gross margin without stating what is excluded. Inventory days computed on revenue instead of COGS.

## Common mistakes to avoid

Calling a cyclical "cheap" at peak margins · extrapolating AI-driven or shortage-driven demand as permanent · treating a strategic inventory build and a demand miss as the same signal · mixing backlog definitions across quarters · ignoring purchase obligations and supplier prepayments · comparing EMS margins to semiconductor margins · crediting announced subsidies or fab plans before they are binding and funded · using diluted weighted-average shares as the primary dilution measure · ignoring net cash when comparing P/E across companies · upgrading a pillar because a metric was found, even though the metric is still in Watch range.

## Red flags

**Severe** — inventory rising sharply while revenue falls and guidance is cut (demand and writedown double hit) · verified loss or major order cut from a customer above 10% of revenue · export-control restriction with verified scope reasonably likely to cause a material, insufficiently mitigated financial effect · covenant pressure, going-concern language, or refinancing risk into a downturn · verified accounting irregularities in revenue or inventory.

**Moderate** — book-to-bill below 1.0 for two or more quarters · customer concentration: one buyer > 20% or top-2 > 30% · capex far above subsector band without binding return evidence · single-source fab or supplier dependence combined with geopolitical exposure · depreciation-life extension or capitalization change that flatters margins · ASP erosion outpacing cost reductions · fixed-price development contracts driving losses (defense).

**Minor** — R&D ratio drifting down year over year · single-quarter inventory build ahead of a verified product ramp · seasonal book-to-bill dip · FX-driven revenue optics.

## Scoring weights

| Pillar | Weight |
|---|---|
| Margins & ROIC trend | 25% |
| Cycle position (inventory, book-to-bill) | 25% |
| Revenue growth (multi-year) | 20% |
| Balance sheet & dilution | 15% |
| Valuation vs own history & peers | 15% |

Sub-score notes: the cycle pillar weighs inventory trend 50% · order signals (book-to-bill/backlog) 30% · utilization/pricing/channel evidence 20% — margin-vs-own-range informs the stated phase but earns no cycle points (it already scores in the margins pillar). If order signals are Not disclosed, redistribute their sub-weight to inventory and the remaining evidence and say so. The balance-sheet pillar includes net share dilution per the period-end standard. If cycle position is undetermined, the cycle AND valuation pillars cap at Watch and the conclusion caps at "mixed, needs more evidence" regardless of the numerical score.

Rate each pillar vs peers and own history: Positive = 2, Watch = 1, Negative = 0. Pillar contribution = pillar weight × rating ÷ 2 (weights total 100%; e.g., 25% × 2 ÷ 2 = 25 points); score = sum of contributions, 0–100%. ~75%+ strong on current evidence; 50–75% mixed; <50% with sufficient evidence and no verified Severe flag = weak on current evidence. Any verified Severe flag caps the score at 50% — always show the uncapped score, the cap applied, and the displayed score. A flag activates the cap only when its evidence is Verified or Calculated — verified inputs; a flag resting on user excerpts or relayed values stays a provisional warning. Two or more verified Severe flags usually mean high-risk / special situation. The score is a research organizer, not a prediction engine.

## Conclusion template

End with exactly one of: **strong on current evidence** / **mixed, needs more evidence** (name the evidence) / **weak on current evidence** (score <50% with sufficient evidence and no verified Severe flag) / **high-risk, special situation** / **insufficient data** — plus data confidence (High/Medium/Low), the stated cycle position, and a two-sentence thesis including what would break it. If cycle position is undetermined, the conclusion cannot exceed "mixed, needs more evidence." No buy/sell/hold language.

## Final sector checklist

1. Sector confirmed: most normalized operating profit fits Electronic Technology (check hybrid routing).
2. Subsector identified: fabless, foundry/IDM/memory, semicap, hardware/devices, EMS/ODM, or defense electronics.
3. Peer group built on business model, capital intensity, customer type, cyclicality — never a bare sector label.
4. Revenue, gross margin, inventory, capex, R&D, and share count verified with exact labels from filings where possible.
5. Cycle position stated explicitly with evidence, or declared undetermined with pillar caps applied.
6. Inventory days computed on COGS basis; strategic vs involuntary builds distinguished.
7. Order signals labeled by definition (book-to-bill basis, backlog type) or marked Not disclosed.
8. Customer, supplier, and export-control concentration reviewed.
9. Capex and R&D judged against subsector bands; subsidies credited only when binding and received.
10. "What NOT to use" respected.
11. Quality-of-earnings and geographic/currency checks run (Core Framework) — depreciation lives and purchase obligations included.
12. Red flags graded with provenance labels and verified before applying the Severe cap.
13. Valuation done on mid-cycle basis, net-cash adjusted, vs own range and peers.
14. Weighted score computed with sub-score rules; weakest pillar identified; uncapped and capped scores shown when a cap applies.
15. Score-change audit trail shown if any follow-up action changed the score; neutral research conclusion written with data confidence, cycle position, and unresolved gaps.

*This is general information only and not financial advice. For personal guidance, please talk to a licensed professional.*
