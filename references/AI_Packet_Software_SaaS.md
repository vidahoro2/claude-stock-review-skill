# AI Stock Review Packet: Software & SaaS

**Version 2.2.5 — Last updated 2026-10-08.** Supersedes v2.2.4. v2.2.5 rewrites the shared evidence-for-ratings rule (first-pass ratings may use Reported evidence provisionally; follow-up rating changes need Verified inputs; model outputs stay Estimated; assumption, arithmetic, or framework changes go through the audit trail) and the matching score-change rule. v2.2.4 adds one shared expectations-module sentence: where a sector packet defines an expectations adaptation, it governs the variables solved for and the value split (Banks and Insurers now define one). v2.2.3 adds the expectations-embedded valuation module: the universal expectations test (reverse-solve the price for required growth, margin, reinvestment and discount rate), the proven-vs-unproven enterprise-value split with its valuation-pillar caps, and the "Estimated — expectations-implied" sub-label. v2.2.2 adds the weak-on-current-evidence conclusion category. Supersedes v2.2 (same day) with calculation corrections: packet-FCF double-count guard, period-end share count as primary dilution measure, calculated-billings-proxy labeling, explicit scoring arithmetic with uncapped/capped display, retention-nondisclosure handling, EV/Sales growth-divisor heuristic removed. v2.2 superseded v2.1: upgraded from a general sector guide to a strict execution file (verification and provenance standard, revenue/ARR disambiguation, retention-metric rules, SBC and dilution rules, capitalized-cost rules, subsector adjustments, scoring and audit-trail rules). Educational framework — not investment advice. No buy/sell/hold language.

*Software / SaaS, internet platforms, IT services, open-source/infrastructure software* — GICS: Information Technology (Software & Services); large internet platforms sit in Communication Services (Media & Entertainment) — see the relocation note below.

**Core principle: adjusted profitability that excludes stock-based compensation is not profitability.** Verification proves a number is real; the sector thresholds, the trend, and the dilution cost determine the rating. A verified 25% "non-GAAP operating margin" with SBC at 22% of revenue is still Watch at best. Verified does not mean Positive.

## Prompt

> Analyze [company name / ticker] using the uploaded Core Framework and this Software & SaaS guide.
> Do not use buy/sell/hold language.
> Provide: 1. Business model summary · 2. Sector and subsector classification · 3. Peer group with rationale · 4. Key SaaS metrics with verification status · 5. Values vs peers and 5-year history · 6. Positive/Watch/Negative assessment · 7. Severe red flags, if any · 8. Valuation (EV/Sales vs growth, Rule of 40, SBC-adjusted FCF) · 9. Data confidence: High/Medium/Low · 10. Neutral research conclusion: strong on current evidence / mixed, needs more evidence / high-risk, special situation / insufficient data.
> Use primary sources (10-K, 10-Q, 20-F, 6-K, annual reports, earnings releases, investor presentations, KPI tables). Do not rely only on screeners or summaries.

## Key metrics & rule-of-thumb ranges

| Metric | Positive | Watch | Negative | How to read it |
|---|---|---|---|---|
| **Revenue growth** | > 20% | 10–20% | < 10% | Organic, constant-currency where disclosed. Deceleration is the #1 thing the market punishes |
| **Gross margin** | > 70% | 50–70% | < 50% | True subscription software should be very high; below 50% questions the model. IT services excepted — see subsector adjustments |
| **Rule of 40** | > 40 | 30–40 | < 30 | Growth % + FCF margin %. See Rule of 40 rules for which inputs are allowed |
| **Net revenue retention (NRR)** | > 110% | 100–110% | < 100% | Above 100% means existing customers spend more each year. Company-defined — see retention rules |
| **Gross retention (GRR)** | > 90% | 85–90% | < 85% | Strips out upsell; shows whether customers actually stay |
| **CAC payback** | < 18 mo | 18–30 mo | > 30 mo | How fast sales & marketing spend is recovered |
| **FCF margin** | > 15% | 0–15% | Persistently neg. | OCF − capex − capitalized software not already in capex; see capitalized-cost rules |
| **SBC % of revenue** | < 10% | 10–20% | > 20% | Stock comp is a real expense paid by dilution |
| **Net share dilution / yr** | < 2% | 2–4% | > 4% | Period-end shares outstanding trend (split-adjusted) over 3–5 years; buybacks that merely offset SBC are not return of capital |
| **cRPO / billings growth** | ≥ revenue growth | Slightly below | Well below | Leading indicators; sharp slowdowns show up here before revenue |
| **EV/Sales** | See valuation rules | — | — | Never rate the multiple in isolation — connect to growth + margin |

**Formulas:** Rule of 40 = organic revenue growth % + FCF margin %. NRR = revenue from existing customers this period ÷ revenue from those same customers in the prior-year period (company definitions vary — record the definition). GRR = (starting recurring revenue − churn − downgrades) ÷ starting recurring revenue. CAC payback (months) = sales & marketing spend ÷ (net-new ARR × gross margin) × 12. Packet FCF margin = (operating cash flow − purchases of property and equipment − capitalized software costs not already included in that capex line) ÷ revenue. SBC ratio = stock-based compensation (cash-flow statement) ÷ revenue. Net dilution = change in period-end common shares outstanding (split-adjusted) ÷ prior-year count; diluted weighted-average shares are a supporting measure only — anti-dilution in loss periods, convertibles, and issuance timing distort them. Calculated billings proxy = revenue + change in deferred revenue. RPO = total contracted revenue not yet recognized; cRPO = the portion expected within 12 months.

## SaaS metric verification standard

A SaaS metric is not "verified" unless the output includes all seven evidence items:

1. Metric name
2. Exact value
3. Source document
4. Exact table, note, or section
5. Short quote showing the metric label next to the value
6. Definition match to this Software & SaaS guide (or the company definition, stated)
7. Score impact

Rules: search summaries, aggregator snippets, and unlabeled extracted numbers cannot verify SaaS metrics. Do not treat a number as verified because a search result or third-party summary claims it came from a filing. Never reuse a percentage from a nearby table unless the label exactly matches the intended metric. If the label is not visible next to the value, the metric is not verified. If the metric cannot be verified, mark it "Needs verification."

**Known trap:** SaaS disclosures are full of similar-looking percentages — revenue growth, ARR growth, cRPO growth, NRR, GRR, gross margin, non-GAAP operating margin, FCF margin, and SBC ratio are all percentages, often on the same slide. The label controls the meaning. The value alone is never enough. A second trap: GAAP metrics live in filings, but ARR, NRR, and CAC usually live only in earnings releases and investor presentations — different documents, different reliability tiers (see data confidence rules).

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

## Shared rules

**Conflicting figures rule (universal):** when two figures for the same metric appear to conflict, do not choose one immediately. First classify the difference: 1. different scope — group vs segment, consolidated vs ex-subsidiary · 2. different basis — gross vs net, reported vs adjusted · 3. different period — quarterly, annualized, LTM, fiscal year · 4. different currency · 5. different definition — company-defined vs packet-defined. Show both figures with provenance labels, then rate the pillar based on the figure that best matches the packet definition. If neither figure matches the packet definition, keep the pillar at Watch or Needs verification.

**Estimated proxy:** when a metric is calculated from available inputs but does not match the company's exact disclosed definition, label it **"Estimated proxy"** and state the inputs used. Examples: an AFFO payout proxy estimated above 100% when AFFO itself is not disclosed; an interest coverage proxy estimated from verified income-statement inputs but not company-disclosed; a net debt/EBITDAre proxy estimated when EBITDAre is not disclosed or JV/pro-rata treatment is unresolved. Never imply the proxy is the same as the company's official metric: a proxy is a sub-type of Estimated, is never Verified, never High confidence, and any rating that rests on it must say so.

**Guidance is not achievement:** guidance, targets, and management plans can support a Watch or directional comment, but they should not receive full Positive credit unless supported by achieved results, binding regulatory approval, or directly verified realized performance. This applies especially to: utilities rate-base growth guidance · REIT rent ramp / stabilized rent targets · energy production or capex targets · SaaS margin expansion targets · bank medium-term ROE targets.

**Expectations are not results (universal):** a price already contains a forecast, and a review that only compares multiples never states what that forecast is. Run this test whenever the valuation pillar would otherwise rest on a multiple above the company's own 5-year range, or whenever the market or management thesis rests on segments with no achieved results; otherwise record "expectations test not triggered" and move on. Invert the valuation — hold the current price fixed and solve for what it requires: revenue CAGR over a stated horizon, steady-state operating or FCF margin, reinvestment (sales-to-capital or reinvestment rate), the discount rate with its components, and a terminal growth rate no higher than the long-run risk-free rate. Convert the requirement into absolute end-of-horizon revenue and test it three ways: against the company's own achieved 5-year record, against the best verified peer analog at comparable scale, and against the current size of the market being addressed. **TAM × assumed share is not a valuation output — it is the assumption under test.** Where a sector packet defines an expectations adaptation, the adaptation governs the variables solved for and the value split; the triggers, caps and labels of this module still apply.

**Proven vs unproven enterprise value:** split EV into the part the proven business supports under the sector packet's normal valuation method and the residual the market is paying for optionality. A segment counts as proven only when the company discloses its revenue AND either its operating profit or a company-defined unit economic; anything else is unproven, is valued separately and labeled, and is never blended into the base multiple. Report the residual as a share of total EV. Rules: required inputs that exceed anything the company has achieved — or anything a verified peer has achieved at comparable scale — cap the valuation pillar at Watch unless the review names the specific verified evidence supporting the higher requirement · residual EV above ~50% of total EV caps the valuation pillar at Watch and obliges the conclusion to state the residual share, whatever the operating pillars show · disclosure too thin to build the test (no segment detail, no margin path) makes valuation **Needs verification**, never a favorable default · do not penalize the same optimism twice by both discounting the required growth and inflating the discount rate — pick one and say which.

**Estimated — expectations-implied:** every output of this test carries that label, a sub-type of Estimated. It is never Verified and never High confidence, because the solution depends on assumptions the review itself chose; only the inputs (price, period-end share count, net debt, disclosed segment figures) carry labels of their own. **Avoid:** analyst price targets as evidence of value · forward multiples built on margins the company has never achieved · "cheap versus its own history" when that history sits entirely inside one expansion regime · peer multiples where the peers are themselves priced on expectations.

## Revenue & ARR disambiguation

Seven different things — never substitute one for another:

| Term | What it is |
|---|---|
| Revenue (GAAP) | Recognized revenue under ASC 606 / IFRS 15 — the only audited growth number |
| ARR | Company-defined non-GAAP annualization of recurring revenue or contracts — definitions vary |
| Annualized run-rate | Latest quarter (or month) × 4 (or 12) — not ARR, not contracted |
| Billings | Only a company-disclosed metric is "billings"; revenue + Δdeferred revenue is a **calculated billings proxy** — distorted by contract assets, unbilled receivables, acquired deferred revenue, FX, duration changes |
| Bookings | New contract value signed — sales activity, not revenue |
| RPO / cRPO | Contracted revenue not yet recognized (total / next 12 months) — audited, in filings |
| Deferred revenue | Balance-sheet liability for cash collected before recognition |

Rules: ARR ≠ revenue — ARR growth can exceed revenue growth for mechanical reasons (annualization of a strong exit month, acquired ARR, definition changes). A company that changes its ARR or NRR definition without restating history gets an automatic Moderate flag. Run-rate annualization is never Verified ARR. Billings can be manipulated by invoice timing and contract duration — never rate growth Positive on billings alone. RPO growth includes multi-year deal length changes; prefer cRPO for near-term momentum. If GAAP revenue growth and ARR growth diverge materially, show both with provenance labels and explain the gap; if unexplained, growth pillar caps at Watch.

## Retention metric rules

NRR, NDR, DBNRR, and DBNER are company-defined and NOT comparable across companies without checking definitions. Record for each company: measurement window (trailing 12 months vs quarterly annualized), cohort basis (all customers vs customers above a size threshold), and whether churned customers are included in the denominator.

Scoring: **Positive** — NRR > 110% with stable or improving trend and GRR > 90% · **Watch** — NRR 100–110%, OR NRR above 110% but declining fast, OR NRR disclosed only above a customer-size threshold · **Negative** — NRR < 100%, or GRR < 85%.

Rules: if NRR is not disclosed, mark retention **Not disclosed** and cap the pillar at **Watch** until evidence is available. Nondisclosure is a disclosure-quality issue, not evidence of deterioration — do not state or imply retention worsened without evidence. A previously consistent NRR disclosure that is discontinued, or redefined without restated history, is a Moderate flag. In usage-based models NRR is volatile through customer optimization cycles — rate the 4–6 quarter trend, not a single print.

## SBC, dilution & capitalized-cost rules

SBC is a real expense paid by shareholders through dilution. Rules: read SBC from the cash-flow statement, never from a non-GAAP reconciliation alone. Rate dilution primarily on period-end common shares outstanding (split-adjusted) over 3–5 years; diluted weighted-average shares are a supporting measure only — anti-dilution during loss periods understates dilution exactly when it matters most. **Buybacks that merely offset SBC issuance are an expense settlement, not a return of capital** — credit the dilution pillar for buybacks only when the period-end count actually falls after SBC and acquisition issuance. Any "adjusted operating margin" or "non-GAAP EPS" that excludes SBC while SBC exceeds 10% of revenue must be shown next to its GAAP counterpart.

**Capitalized-cost trap:** capitalized software development costs shift R&D expense from the income statement to capex — inflating gross margin, operating margin, and EBITDA while leaving FCF unchanged or worse. Rules: compute packet FCF as OCF − purchases of property and equipment − capitalized software costs **not already included** in that line. Inspect the cash-flow labels and the software-cost note before subtracting: many companies report capitalized software inside capex — never subtract the same expenditure twice. State OCF, the reported capex label, the capitalized-software amount, and whether it sits inside or outside capex. If capitalized development costs grow materially faster than revenue for 2+ years, apply a Moderate flag and re-check the margin story. Compare (R&D expense + capitalized software) ÷ revenue across peers, not R&D expense alone.

## Rule of 40 rules

Allowed inputs: organic revenue growth % (constant-currency where disclosed) + FCF margin % as defined above. Not allowed: ARR growth substituted for revenue growth · non-GAAP operating margin substituted for FCF margin (it excludes SBC and capitalized costs) · acquisition-inflated growth. A Rule of 40 above 40 built on a Watch-rated FCF definition or unverified growth is itself Watch. State the two inputs and their verification status whenever the Rule of 40 is scored.

## Growth quality rules

Separate organic from acquired growth using the acquisitions note and pro-forma disclosures; if the split is not disclosed and M&A is material, growth is at best Watch, Needs verification. Watch the deceleration curve: sequential net-new ARR (or sequential revenue adds) reveals slowdowns two to four quarters before year-over-year rates do. FX can add or hide several points — prefer constant-currency where disclosed. Verified high growth with decelerating cRPO and falling net-new ARR does not earn a full Positive growth score.

## Subsector adjustments

Classify the subsector first; the main table assumes subscription software.

**Per-seat / subscription SaaS** — the main table applies as written. Watch seat-count exposure to customer headcount cuts and AI-driven seat compression.

**Usage / consumption-based** (cloud data, infrastructure, API businesses) — NRR is volatile and seasonal; rate the multi-quarter trend. cRPO and net-new consumption commitments are the best leading indicators. Gross margin reflects compute costs — a dip from AI/GPU mix is Minor if the trend recovers.

**Open-source / infrastructure software** — check conversion of community usage to paid; sales efficiency is usually worse; CAC payback thresholds loosen one notch.

**IT services / consulting / outsourcing** — headcount-driven, not software economics. Override the main table: gross margin 25–35% is normal, not Negative; Rule of 40 does not apply. Use instead: utilization rate, revenue per employee, attrition, book-to-bill, backlog, pricing (rate cards), operating margin 10–20% band. Valuation on P/E or EV/EBIT, not EV/Sales.

**License-to-subscription transitions** — optical revenue decline can mask a healthy model shift (upfront license revenue trades for ratable subscription). Use ARR, cRPO, and remaining maintenance base; do not rate the transition-period growth Negative mechanically — but demand evidence the subscription base is actually building.

**Internet platforms / marketplaces (relocation note)** — if most operating profit comes from advertising, marketplace take rates, or consumer engagement, the company usually belongs in Communication Services or Consumer Discretionary under GICS. Metrics shift to DAU/MAU, ARPU, take rate, engagement. This packet may still be used on request, but state the relocation and adjust peers accordingly.

**Hybrid routing:** hardware + software mixes (devices, semis with software attach) → classify by where most operating profit comes from; majority-hardware profit → use the Electronic Technology packet. Payments/fintech platforms → Fintech & Payments packet. Video games with live-service recurring revenue may use this packet's retention logic but take Consumer Services / Communication peers.

## Valuation rules

Connect EV/Sales to growth AND margin — never rate the multiple alone: a 12x EV/Sales on 35% durable growth with 25% FCF margin can be more defensible than 5x on 8% growth. Reference checks: EV/Sales (LTM, and NTM where reliable consensus exists) vs the company's own 3–5 year range AND the peer median/interquartile range — there is no universal growth-to-multiple conversion rule · Rule of 40 vs peer multiples · EV/FCF using packet FCF (SBC-honest; cross-check against GAAP profit) · PEG once meaningfully GAAP-profitable.

Rules: high multiple + verified decelerating growth (falling net-new ARR, cRPO growth below revenue growth) → valuation pillar Watch or Negative regardless of business quality. Never justify a premium multiple with non-GAAP margins while SBC exceeds 15% of revenue. For IT services use P/E or EV/EBIT vs peers. **Avoid:** P/E for early-stage high-growth names · adjusted profit metrics that exclude SBC while dilution runs high · EV/ARR on company-defined ARR without a GAAP reconciliation.

## Default first-pass dashboard for Software & SaaS

Six cards: 1. Growth (revenue growth, net-new ARR, cRPO growth) · 2. Retention (NRR, GRR with definitions) · 3. Unit economics (gross margin, CAC payback) · 4. Profitability (FCF margin, Rule of 40, GAAP operating margin) · 5. Dilution (SBC ratio, net share count trend) · 6. Valuation (EV/Sales vs growth, EV/FCF, peer context).

Each card shows: value · Positive/Watch/Negative rating · provenance label (per the v4 standard) · one-line explanation. Use concise tables, not long paragraphs.

The first-pass score is always provisional unless: GAAP revenue and growth verified from filings, SBC and share count verified from filings, FCF computed per this packet, and at least partial peer comparison performed.

## Follow-up actions

Offer: 1. Verify KPI disclosures (ARR/NRR definitions and history) · 2. Deep dive: dilution and SBC · 3. Deep dive: growth quality (organic vs acquired, net-new ARR curve) · 4. Deep dive: valuation vs growth and peers · 5. Compare vs subsector peers · 6. Deep dive: quality of earnings (capitalized costs, billings terms) · 7. Deep dive: competitive/AI disruption exposure.

Priority logic: NRR missing or definition changed → recommend 1. SBC > 15% of revenue or share count rising > 3%/yr → recommend 2. M&A-heavy or net-new ARR falling → recommend 3. EV/Sales high vs growth band → recommend 4. Capitalized software growing faster than revenue or billings diverging from revenue → recommend 6.

## Score-change audit trail

Whenever a follow-up action changes the score, show all nine items: 1. previous score · 2. updated score · 3. metric that changed · 4. old status · 5. new verified value · 6. source document · 7. exact quote showing label and value · 8. pillar affected · 9. reason for the change.

Rules: if the exact quote for a new factual input cannot be provided, do not change the score on that input — keep the metric at Needs verification. A score changes only when a pillar's Positive/Watch/Negative rating changes — through a newly verified input, or through a disclosed change in assumption, judgment, arithmetic, or framework version (name the type in item 9; items 5–7 then read "not applicable"); verification alone does not automatically change the score.

## Data confidence rules

**High:** recent 10-K / 10-Q / 20-F / 6-K / audited annual report with the exact table label and value quoted — this covers GAAP revenue, deferred revenue, RPO/cRPO, SBC (cash-flow statement), and share counts. **Medium:** earnings release or investor presentation with a labeled table — this is usually the ONLY home of ARR, NRR, GRR, CAC, and customer counts; these metrics can never be High confidence unless they appear labeled in a filing. **Low:** aggregator-only data, search-summary data, incomplete disclosure, estimated ratios, unlabeled numbers.

Rules: price and EV from aggregators may be used as Estimated. Company-defined KPIs keep a definition caveat even when verified in a presentation. If a key metric is Low confidence, state how it affects the pillar score.

## What NOT to use

P/E for early-stage, high-growth names deliberately running at low GAAP profit. 'Adjusted' profit measures that exclude stock-based compensation while dilution runs high. Total revenue growth without separating organic from acquired. EV/ARR without a GAAP revenue reconciliation. Billings growth as a substitute for revenue growth. Rule of 40 built from non-GAAP operating margin.

## Common mistakes to avoid

Treating ARR as revenue · comparing NRR across companies with different definitions · crediting buybacks that merely offset SBC issuance · using non-GAAP margins that exclude SBC as the profitability anchor · missing capitalized development costs when judging margins · rating growth on billings or bookings alone · applying SaaS thresholds to IT services businesses · applying SaaS multiples to license-transition businesses mid-transition · rating a high EV/Sales "Negative" mechanically without the growth/margin context · rating a low EV/Sales "cheap" while growth decelerates and NRR sits below 100% · upgrading a pillar because a metric was found, even though the metric is still in Watch range.

## Red flags

**Severe** — growth slowing sharply while the valuation still prices hyper-growth · NRR below 100% and falling — the installed base is shrinking · going-concern language, covenant pressure, or a cash runway under ~18 months with negative FCF · evidence of round-tripping, channel stuffing, or receivables far outgrowing revenue · loss or churn of a customer accounting for >10% of revenue.

**Moderate** — SBC above 20% of revenue with a rising share count · cRPO/billings growth well below recognized revenue growth for 2+ quarters · ARR or NRR definition changed without restated history, or disclosure ceased · capitalized software development costs growing materially faster than revenue · acquisitions masking organic decline (no organic split disclosed) · top-3 customers > 20% of revenue · debt-funded buybacks that only offset SBC presented as shareholder returns.

**Minor** — gross margin dip from cloud-hosting or AI-compute mix shift (watch the trend) · FX-driven growth optics either direction · single-quarter NRR dip in a usage-based model during customer optimization cycles · seat-growth pause during customer headcount cuts if retention holds.

## Scoring weights

| Pillar | Weight |
|---|---|
| Revenue growth / NRR | 30% |
| Gross margin / Rule of 40 | 25% |
| FCF margin | 20% |
| Dilution / SBC | 15% |
| Valuation (EV/Sales vs growth) | 10% |

Sub-score notes: the growth/NRR pillar weighs organic revenue growth 50% · retention (NRR/GRR) 30% · leading indicators (net-new ARR, cRPO) 20%. If retention is Needs verification, the pillar cannot score above Watch. If growth is verified but ARR/revenue divergence is unexplained, the pillar caps at Watch.

Rate each pillar vs peers and own history: Positive = 2, Watch = 1, Negative = 0. Pillar contribution = pillar weight × rating ÷ 2 (weights total 100%; e.g., 30% × 2 ÷ 2 = 30 points); score = sum of contributions, 0–100%. ~75%+ strong on current evidence; 50–75% mixed; <50% with sufficient evidence and no verified Severe flag = weak on current evidence. Any verified Severe flag caps the score at 50% — always show the uncapped score, the cap applied, and the displayed score. A flag activates the cap only when its evidence is Verified or Calculated — verified inputs; a flag resting on user excerpts or relayed values stays a provisional warning. Two or more verified Severe flags usually mean high-risk / special situation. The score is a research organizer, not a prediction engine.

## Conclusion template

End with exactly one of: **strong on current evidence** / **mixed, needs more evidence** (name the evidence) / **weak on current evidence** (score <50% with sufficient evidence and no verified Severe flag) / **high-risk, special situation** / **insufficient data** — plus data confidence (High/Medium/Low) and a two-sentence thesis including what would break it. No buy/sell/hold language.

## Final sector checklist

1. Sector confirmed: most operating profit fits Software & SaaS (check the relocation and hybrid routing notes).
2. Subsector identified: per-seat SaaS, usage-based, open-source/infra, IT services, license-transition, or platform.
3. Peer group built on business model, growth stage, margin structure, go-to-market, customer type.
4. GAAP revenue, SBC, share count, and RPO verified with exact labels from filings where possible.
5. Revenue/ARR terms disambiguated: revenue, ARR, run-rate, billings, bookings, RPO/cRPO, deferred revenue kept separate.
6. Retention metrics recorded with company definitions; missing NRR handled per retention rules.
7. FCF computed per packet definition including capitalized software costs.
8. Rule of 40 built only from allowed inputs, with verification status stated.
9. Organic vs acquired growth separated; deceleration curve (net-new ARR, cRPO) reviewed.
10. "What NOT to use" respected.
11. Quality-of-earnings and geographic/currency checks run (Core Framework).
12. Red flags graded and verified before applying the Severe cap.
13. Valuation done with EV/Sales vs growth + margin context, SBC-honest FCF, and peer comparison.
14. Weighted score computed with sub-score rules; weakest pillar identified.
15. Score-change audit trail shown if any follow-up action changed the score; neutral research conclusion written with data confidence and unresolved gaps.

*This is general information only and not financial advice. For personal guidance, please talk to a licensed professional.*
