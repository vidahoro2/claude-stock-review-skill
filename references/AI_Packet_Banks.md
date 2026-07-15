# AI Stock Review Packet: Banks

**Version 2.2.2 — Last updated 2026-07-13.** v2.2.2 adds the weak-on-current-evidence conclusion category. v2.2.1 adds the v4 provenance-label table (Calculated — verified inputs, Not disclosed; Severe-flag caps require verified evidence). Supersedes v2.1: upgraded from a general sector guide to a strict execution file (verification standard, capital disambiguation, scoring rules, audit trail, digital-bank adjustments). Educational framework — not investment advice. No buy/sell/hold language.

*Commercial banks, regional banks, money-center banks, digital banks and fintechs with banking charters* — GICS: Financials (Banks)

**Core principle: Verified does not mean Positive.** Verification proves the number is real; the sector thresholds, the trend, and the distance from regulatory minimums determine the rating. A verified CET1 of 11.3% is still Watch.

## Prompt

> Analyze [company name / ticker] using the uploaded Core Framework and this Banks guide.
> Do not use buy/sell/hold language.
> Provide: 1. Business model summary · 2. Sector classification · 3. Peer group with rationale · 4. Key bank metrics with verification status · 5. Values vs peers and 5-year history · 6. Positive/Watch/Negative assessment · 7. Severe red flags, if any · 8. Valuation (P/B or P/TBV with ROE/ROTE) · 9. Data confidence: High/Medium/Low · 10. Neutral research conclusion: strong on current evidence / mixed, needs more evidence / high-risk, special situation / insufficient data.
> Use primary sources (10-K, 10-Q, 20-F, 6-K, call reports, regulatory filings, earnings releases). Do not rely only on screeners or summaries.

## Key metrics & rule-of-thumb ranges

| Metric | Positive | Watch | Negative | How to read it |
|---|---|---|---|---|
| **ROE** | > 12% | 8–12% | < 8% | Headline profitability; compare to cost of equity |
| **ROTE** | > 14% | 10–14% | < 10% | Strips goodwill; the cleaner returns measure |
| **ROA** | > 1.2% | 0.8–1.2% | < 0.8% | Above ~1% is a well-run bank |
| **NIM** | > 3% | 2–3% | < 2% | Rate-environment dependent; for unsecured lenders read with risk-adjusted NIM |
| **Efficiency ratio** | < 55% | 55–65% | > 65% | Costs ÷ revenue — lower is better. A COST metric, never a capital metric |
| **CET1 ratio** | > 12%, stable/improving, comfortably above minimum | 10–12%, or declining materially even if compliant | < 10%, near minimum, or falling quickly | See Capital adequacy scoring rules |
| **Loan-to-deposit** | 70–90% | 90–100% | > 100% | Above 100% = wholesale-funded lending |
| **Deposit trend** | Growing, low-cost | Flat, mix shifting | Shrinking | Deposit flight is existential |
| **NPLs / net charge-offs** | Low & stable | Ticking up | Rising fast | See Credit quality rules |
| **P/B with ROE** | See Bank valuation logic | — | — | Never rate P/B in isolation |

**Formulas:** ROE = net income ÷ avg equity. ROTE = net income ÷ avg tangible common equity. ROA = net income ÷ avg assets. NIM = net interest income ÷ avg earning assets. Risk-adjusted NIM = NIM after credit-loss allowances. Efficiency ratio = non-interest expense ÷ (net interest income + non-interest income). CET1 ratio = common equity tier 1 capital ÷ RWA. Tier 1 ratio = tier 1 capital ÷ RWA. CAR = total regulatory capital ÷ RWA. LDR = loans ÷ deposits. NCO ratio = (charge-offs − recoveries) ÷ avg loans. Cost of risk = provision expense ÷ avg loans. P/B = market cap ÷ book equity; P/TBV = market cap ÷ tangible book.

## Bank metric verification standard

A bank metric is not "verified" unless the output includes all seven evidence items:

1. Metric name
2. Exact value
3. Source document
4. Exact table, note, or section
5. Short quote showing the metric label next to the value
6. Definition match to this Banks guide
7. Score impact

Rules: search summaries, aggregator snippets, and unlabeled extracted numbers cannot verify bank metrics. Do not treat a number as verified because a search result or third-party summary claims it came from a filing. Never reuse a percentage from a nearby table unless the label exactly matches the intended metric. If the label is not visible next to the value, the metric is not verified. If the metric cannot be verified, mark it "Needs verification."

**Known trap:** identical or similar percentages appear for different bank metrics in the same filing — efficiency ratio, CET1 ratio, CAR, ECL/stage ratios, and capital requirements are all percentages. The label controls the meaning. The value alone is never enough.

**Conflicting figures rule:** when two figures for the same metric appear to conflict, do not choose one immediately. First classify the difference: 1. different scope — group vs segment, consolidated vs ex-subsidiary · 2. different basis — gross vs net, reported vs adjusted · 3. different period — quarterly, annualized, LTM, fiscal year · 4. different currency · 5. different definition — company-defined vs packet-defined. Show both figures with provenance labels, then rate the pillar based on the figure that best matches the packet definition. If neither figure matches the packet definition, keep the pillar at Watch or Needs verification.

**Estimated proxy:** when a metric is calculated from available inputs but does not match the company's exact disclosed definition, label it **"Estimated proxy"** and state the inputs used. Examples: an AFFO payout proxy estimated above 100% when AFFO itself is not disclosed; an interest coverage proxy estimated from verified income-statement inputs but not company-disclosed; a net debt/EBITDAre proxy estimated when EBITDAre is not disclosed or JV/pro-rata treatment is unresolved. Never imply the proxy is the same as the company's official metric: a proxy is a sub-type of Estimated, is never Verified, never High confidence, and any rating that rests on it must say so.

**Guidance is not achievement:** guidance, targets, and management plans can support a Watch or directional comment, but they should not receive full Positive credit unless supported by achieved results, binding regulatory approval, or directly verified realized performance. This applies especially to: utilities rate-base growth guidance · REIT rent ramp / stabilized rent targets · energy production or capex targets · SaaS margin expansion targets · bank medium-term ROE targets.

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

## Bank capital disambiguation

Seven different things — never substitute one for another:

| Term | What it is |
|---|---|
| CET1 ratio | Common equity tier 1 capital ÷ RWA |
| Tier 1 capital ratio | Tier 1 capital ÷ RWA |
| Total capital ratio / CAR | Total regulatory capital ÷ RWA |
| Regulatory capital requirement | The minimum (varies by jurisdiction and bank) |
| Excess capital / surplus | Dollar capital held above the requirement — not a ratio |
| Liquidity position | LCR / liquid assets — not capital at all |
| Efficiency ratio | An operating-cost metric — nothing to do with capital |

Rules: CET1 ≠ CAR. Capital excess in dollars ≠ a capital ratio. "In compliance" ≠ a disclosed ratio. A value labeled "efficiency ratio" can never be used as any capital ratio. A value labeled "capital requirement" or "capital excess" cannot be used as CET1 or CAR unless the ratio itself is separately disclosed and labeled. If the exact ratio is not disclosed: **"Capital ratio not directly disclosed / needs verification."**

## Capital adequacy scoring rules

Use capital metrics in this order of preference: 1. CET1 ratio · 2. Tier 1 ratio · 3. CAR · 4. Regulatory requirement · 5. Excess capital · 6. Management compliance statement.

CET1 scoring: **Positive** > 12%, stable or improving, comfortably above the minimum · **Watch** 10–12%, OR declining materially even if compliant · **Negative** < 10%, near minimum, or declining quickly.

Rules: Verified does not mean Positive — a verified 11.3% is Watch. A verified CAR above requirements supports compliance but does NOT upgrade the capital pillar to Positive if CET1 is in Watch range or falling. Never upgrade the capital pillar to Positive using only: compliance statements, dollar capital amounts, excess-capital amounts, liquidity comments, or third-party summaries. Verification removes uncertainty; the rating must still follow thresholds, trend, and distance from minimums. Stale ratios (older than the latest credit data) keep a trend caveat and generally cannot support Positive if the trend is down.

## Capital / liquidity / deposits pillar sub-score

The 25% pillar weighs: capital adequacy 40% · deposit stability and cost 30% · liquidity and LDR 20% · securities losses / funding stress 10%.

Rules: if capital adequacy is Needs verification, the pillar cannot score above Watch. If CET1 is in Watch range, the pillar generally stays Watch even with strong deposits — strong deposits cannot fully offset weak or unverified capital. If CET1 is declining materially, state the trend. Verified rapid deposit outflows → pillar Negative and likely a Severe flag. CET1 near minimums + deteriorating credit → apply the Severe cap. Verified compliance alone is never enough for Positive.

## Credit quality rules

Use where available: NPL 15–90, NPL 90+, net charge-off ratio, provision expense, cost of risk, allowance/reserve coverage, IFRS Stage 2/Stage 3 loans, delinquency by vintage/cohort, loan growth by product, secured vs unsecured mix.

Scoring: **Positive** — NPLs/charge-offs low or improving, provisions adequate, loan growth not masking deterioration · **Watch** — NPLs elevated, provisions or cost of risk rising, or riskier mix increasing · **Negative** — NPLs/charge-offs rising fast, coverage weakening, or rapid growth into high-loss categories.

**Rule: rapid loan growth can temporarily hide credit problems** (new loans haven't seasoned; denominators inflate). If loan growth is very high (roughly >20%/yr), require cohort/vintage evidence before rating credit quality Positive.

## Bank valuation logic

Connect P/B or P/TBV to ROE/ROTE and the cost of equity — never rate the multiple alone. High P/B is not automatically expensive if ROE/ROTE is durably high with strong credit. Low P/B is not automatically cheap if ROE is below cost of equity or credit is deteriorating. High ROE with rising credit risk does not earn a full Positive valuation score. A premium P/B on a credit-cyclical loan book is at least Watch unless peer comparison and credit data support it. Use P/TBV where goodwill/intangibles distort book.

Valuation review includes: P/B or P/TBV · ROE/ROTE · cost-of-equity reference · credit-quality trend · peer P/B vs peer ROE · deposit franchise quality · growth durability · capital adequacy.

## Default first-pass dashboard for banks

Six cards: 1. Profitability (ROE, ROTE, ROA) · 2. Spread economics (NIM or risk-adjusted NIM) · 3. Efficiency (efficiency ratio) · 4. Credit quality (NPLs, NCOs, provisions, cost of risk) · 5. Capital and funding (CET1/CAR, deposits, LDR, liquidity) · 6. Valuation (P/B or P/TBV with ROE/ROTE and credit context).

Each card shows: value · Positive/Watch/Negative rating · provenance label (per the v4 standard) · one-line explanation. Use concise tables, not long paragraphs.

The first-pass bank score is always provisional unless: capital ratio verified, credit metrics verified, valuation data current, and at least partial peer comparison performed.

## Bank-specific follow-up actions

Offer: 1. Verify capital ratio · 2. Deep dive: credit quality · 3. Deep dive: deposits and funding · 4. Deep dive: valuation vs ROE/ROTE · 5. Compare vs bank peers · 6. Deep dive: securities portfolio and unrealized losses · 7. Deep dive: regulatory and country risk.

Priority logic: capital ratio missing → recommend 1. NPLs/NCOs/provisions/cost of risk rising → recommend 2. P/B or P/TBV high vs peers → recommend 4. Deposits shrinking, deposit costs rising, or wholesale funding growing → recommend 3. Unrealized securities losses large vs tangible equity → recommend 6.

## Digital bank and fintech-bank adjustments

Use this Banks framework whenever the business is mainly spread-driven, deposit-funded, or credit-risk-driven — regardless of "fintech" branding. Bank rules still apply in full to: deposits, capital adequacy, loan growth, credit losses, NPLs, provisions, cost of risk, LDR, liquidity, regulatory capital.

Add fintech-style checks: active customers / monthly actives, customer acquisition cost, revenue per active customer, deposits per customer, product cross-sell, activity rate, operating leverage, stock-based compensation, share dilution.

Do not compare digital banks mechanically with mature branch banks. Peer groups: similar digital banks + local incumbents (for credit cycle, regulation, and valuation context) + regional fintech lenders; payment/financial platforms only where the model genuinely overlaps.

A premium P/B for a digital bank is justified only if ALL hold: ROE/ROTE high and durable · credit losses controlled · capital comfortably above requirements · deposits stable and low-cost · customer growth converting into profitable products · dilution controlled. If credit quality is worsening while the valuation stays premium, rate valuation Watch or Negative even if current profitability is high.

## Score-change audit trail

Whenever a follow-up action changes the score, show all nine items: 1. previous score · 2. updated score · 3. metric that changed · 4. old status · 5. new verified value · 6. source document · 7. exact quote showing label and value · 8. pillar affected · 9. reason for the change.

Rules: if the exact quote cannot be provided, do not change the score — keep the metric at Needs verification. A score changes only when the newly verified metric changes a pillar's Positive/Watch/Negative rating; verification alone does not automatically change the score.

## Bank data confidence rules

**High:** recent 10-K / 10-Q / 20-F / 6-K / call report / regulatory filing / audited statements, with the exact table label and value quoted. **Medium:** company earnings release or investor presentation with a labeled table; reputable provider cross-checked against filings. **Low:** aggregator-only data, search-summary data, incomplete disclosure, estimated ratios, unlabeled numbers, ratios computed from partial data.

Rules: price and P/B from aggregators may be used as Estimated. Regulatory capital metrics are never High confidence unless the filing or regulator source clearly labels the ratio. If a key metric is Low confidence, state how it affects the pillar score.

## What NOT to use

EV/EBITDA, gross margin, operating margin, net debt/EBITDA, and FCF metrics — meaningless or misleading for banks. Deposits are not corporate debt. A low P/B alone is not cheap: a bank earning below its cost of equity deserves to trade below book.

## Common mistakes to avoid

Treating deposits as corporate debt · using EV/EBITDA · calling low P/B "cheap" without ROE and credit checks · calling high P/B "expensive" without ROE-durability checks · confusing efficiency ratio with capital ratio · confusing CAR with CET1 · treating compliance as a Positive capital score · ignoring deposit mix and costs · ignoring securities losses vs tangible equity · ignoring loan-book concentration · giving full profitability credit when credit costs are temporarily low · comparing digital banks directly with branch-heavy incumbents · upgrading a pillar because a metric was found, even though the metric is still in Watch range.

## Red flags

**Severe** — rapid deposit outflows or heavy wholesale/brokered funding reliance · NPLs and charge-offs rising while CET1 sits near minimums · CET1/Tier 1/CAR falling close to regulatory minimums · liquidity stress, emergency funding, or going-concern language · material regulatory enforcement affecting capital, liquidity, or lending · large unrealized securities losses vs tangible equity combined with deposit pressure.

**Moderate** — concentration in one loan book, geography, or segment · unrealized securities losses large vs tangible equity · rising deposit costs or mix shift to higher-cost funding · rising provisions, cost of risk, or early delinquencies · rapid growth into unsecured/higher-risk segments · premium valuation while credit quality weakens · capital ratios declining but still above minimums.

**Minor** — efficiency ratio drifting up 2–3 quarters · seasonal delinquency uptick without confirmed deterioration · temporary NIM compression from the rate environment · small deposit mix shift without outflows.

## Scoring weights

| Pillar | Weight |
|---|---|
| ROE / ROA / ROTE | 25% |
| Credit quality (NPLs, charge-offs) | 25% |
| CET1 / liquidity / deposits (see sub-score) | 25% |
| Efficiency ratio | 10% |
| Valuation vs book (P/B vs ROE) | 15% |

Score each pillar 2 (Positive), 1 (Watch), 0 (Negative) vs peers and own history; weighted total ÷ 2 = 0–100%. ~75%+ strong on current evidence; 50–75% mixed; <50% with sufficient evidence and no verified Severe flag = weak on current evidence. Any verified Severe flag caps the score at 50%; two or more usually mean high-risk / special situation. Verify flags against primary sources before capping. The score is a research organizer, not a prediction engine.

## Conclusion template

End with exactly one of: **strong on current evidence** / **mixed, needs more evidence** (name the evidence) / **weak on current evidence** (score <50% with sufficient evidence and no verified Severe flag) / **high-risk, special situation** / **insufficient data** — plus data confidence (High/Medium/Low) and a two-sentence thesis including what would break it. No buy/sell/hold language.

## Final sector checklist

1. Sector confirmed: most operating profit fits Banks.
2. Bank type identified: money-center, regional, digital bank, fintech-bank, emerging-market bank, or specialized lender.
3. Peer group built on business model, geography, regulation, growth stage, credit-risk profile.
4. Bank metrics verified with exact labels from primary sources where possible.
5. Capital metrics disambiguated: CET1, Tier 1, CAR, requirement, excess, liquidity, efficiency kept separate.
6. Credit quality reviewed: NPLs, charge-offs, provisions, cost of risk, reserves, loan growth.
7. Deposit and funding quality reviewed.
8. Securities losses and tangible-equity impact reviewed where relevant.
9. "What NOT to use" respected.
10. Quality-of-earnings and geographic/currency checks run (Core Framework).
11. Red flags graded and verified before applying the Severe cap.
12. Valuation done with P/B or P/TBV + ROE/ROTE + credit quality + cost of equity.
13. Weighted score computed; weakest pillar identified.
14. Score-change audit trail shown if any follow-up action changed the score.
15. Neutral research conclusion written with data confidence and unresolved gaps.

*This is general information only and not financial advice. For personal guidance, please talk to a licensed professional.*
