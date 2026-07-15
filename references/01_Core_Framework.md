# Core Framework — Universal Stock Analysis Rules

**Version 2.1.2 — Last updated 2026-07-13.** v2.1.2 adds the weak-on-current-evidence conclusion category. v2.1.1 adds the v4 provenance-label table (Calculated — verified inputs, Not disclosed; Severe-flag caps require verified evidence). Educational framework — not investment advice. No buy/sell/hold language.

Part of the Stock Analysis Modular System. Upload (or paste) this with the relevant sector guide or AI packet when reviewing one company.

## How to use the modular system

- **Learning:** full Master Guide.
- **Analyzing one stock:** this Core Framework + the relevant Sector guide.
- **Most token-efficient AI analysis:** the relevant AI Packet only.
- **Updating:** update the Master Guide first, then regenerate Core, Sector files, and AI Packets.

## The four comparisons (always)

Every metric must be compared against:

- **Own 5-year history** — improving or deteriorating?
- **Direct peers** — same business model, not just the same sector label.
- **Sector cycle** — a 'cheap' cyclical at peak earnings is usually expensive.
- **Growth/return profile** — a 25x P/E can be cheap for a fast compounder, dear for a no-growth utility.

*Examples: 30x P/E can be fair if peers trade at 35x with worse ROIC/growth/leverage; 10x P/E can be expensive if earnings are at a cyclical peak and peers trade at 8x mid-cycle.*

## How to build a peer group

Good peers share most of: business model, geography, growth stage, margin structure, capital intensity, regulatory exposure, customer type, cyclicality. A sector label is not a peer group (Microsoft ≠ Snowflake ≠ Accenture ≠ Shopify; JPMorgan ≠ regional bank ≠ insurer ≠ Visa; grocer ≠ luxury retailer).

Method: start from the 10-K competition section → add the GICS sub-industry list → filter to 5–10 genuine peers. If fewer than 4–5 exist, lean on the company's own history and soften relative-valuation conclusions.

## The first 10 things to check

1. Identify the business model and sector page. For mixed businesses, classify by where most operating profit comes from.
2. Revenue trend over 5 years — growing, flat, shrinking? Organic or acquired?
3. Gross margin level and trend vs direct peers (skip for banks/insurers).
4. Free cash flow — positive, growing, converting from profits? (FFO/AFFO for REITs; skip for banks.)
5. Leverage — net debt/EBITDA generally; CET1 for banks; debt/EBITDAre for REITs; FFO/debt for utilities.
6. Share count over 5 years — dilution or buybacks?
7. Returns — ROIC vs cost of capital; ROE/ROTE vs cost of equity for banks and insurers.
8. Valuation vs own 5-year range AND vs peers, using the right multiple for the sector.
9. Run the sector red-flag list; grade findings Minor / Moderate / Severe.
10. Ask why the opportunity exists; write the thesis in two sentences.

## Red-flag severity & override rule

- **Minor** — note it; monitor 1–2 quarters.
- **Moderate** — needs a convincing explanation before a positive conclusion.
- **Severe** — usually disqualifying until resolved (uncovered dividend, <12-month runway, deposit flight, adverse reserve development, covenant/going-concern issues, restatements).

**Override rule:** any verified Severe red flag caps the total score at 50% until resolved. Two or more Severe red flags usually disqualify the company from normal fundamental analysis (special-situation territory). Verify flags against primary sources before applying the cap.

**False precision:** the score is a research organizer, not a prediction engine. A 78% company is not automatically better than a 72% one. The score shows which pillar needs more research; judgment and the written thesis matter more than the number.

## Universal core framework

| Metric | Positive | Watch | Negative | Notes |
|---|---|---|---|---|
| Revenue growth (YoY) | > 10% | 3–10% | < 0% | Multi-year direction beats one quarter |
| Gross / operating margin | Sector-relative | — | — | Only meaningful vs peers; N/A banks/insurers |
| Net margin | > 10% | 0–10% | Persistently neg. | Sector-dependent |
| ROIC | > 10–12% | 6–10% | Below cost of capital | NOT for banks/insurers — use ROE/ROTE |
| Free cash flow | Positive & growing | Break-even | Persistently neg. | Banks: N/A; REITs/utilities: FFO-based |
| Net debt/EBITDA | < 2x | 2–4x | > 4x | N/A banks/insurers |
| Share count | Flat/shrinking | Slowly rising | Rapidly rising | Dilution is universal |

Formulas: FCF = operating cash flow − capex. ROIC = NOPAT ÷ (debt + equity − cash). Net debt/EBITDA = (debt − cash) ÷ EBITDA. Rule of 40 = revenue growth % + FCF margin %.

## Quality of earnings checklist

- Profits converting into cash? Over 3–5 years FCF should roughly track net income.
- FCF consistently and materially below net income? Investigate the gap.
- 'Adjusted' earnings much higher than GAAP, year after year?
- Same 'one-time' add-backs recurring every year?
- Working capital temporarily flattering cash flow?
- Acquisitions masking weak organic growth? Watch goodwill build.
- Revenue recognized aggressively? Receivables outgrowing revenue is a warning.
- Margin gains from real operating leverage — or accounting changes?

**Rule: high-quality earnings are recurring, cash-backed, and not dependent on repeated adjustments.** Cash conversion = FCF ÷ net income (~80–100%+ over 3–5 years for mature firms); investigate persistent adjusted-vs-GAAP gaps above ~20%.

## Geographic, currency & political risk checklist

- Where is revenue generated? Where are profits generated (often different)?
- Where are assets located? Can they be taken or stranded?
- What currencies are revenue and costs in? Any mismatch?
- What currency is the debt in? FX debt vs local revenue is the classic blow-up.
- Politically risky jurisdictions — expropriation, licenses, rule of law?
- Could tariffs, sanctions, capital controls, tax changes, or regulation hit the model?

Matters most for mining, energy, banks, staples/multinationals, industrials, and emerging-market listings.

## Valuation methods by sector

| Sector | Primary valuation tools | Avoid / treat carefully |
|---|---|---|
| Banks | P/B & P/TBV with ROE/ROTE vs cost of equity; dividend yield | EV/EBITDA, net debt/EBITDA, gross margin, FCF, P/B without ROE |
| Insurers | P/B with ROE; BV growth + dividends; combined ratio trend | Premium growth alone; single-year P/E |
| Asset mgrs / exchanges | P/E vs flow growth; EV/EBITDA; FCF yield | P/B; bull-market AUM growth |
| Fintech / payments | EV/Sales or P/E vs volume growth; FCF yield | P/B; gross revenue; P/E for unprofitable fintechs |
| REITs | P/FFO, P/AFFO, NAV, implied cap rate, dividend coverage | Standard P/E, EPS, net income, unadjusted FCF |
| SaaS / software | EV/Sales vs growth, Rule of 40, FCF margin, NRR; PEG once profitable | P/E for early-stage; adjusted profits ignoring SBC |
| Energy (oil & gas) | FCF yield, EV/DACF, NAV of reserves, breakeven sensitivity | Low P/E at peak prices; field breakevens as corporate ones |
| Mining | NAV, through-cycle EV/EBITDA, cost-curve position, FCF yield | Single-year P/E; AISC outside precious metals |
| Utilities | P/E vs EPS growth, yield spread, FFO/debt, allowed ROE | FCF alone |
| Biotech (pre-commercial) | Cash runway, pipeline value, probability-adjusted NPV | P/E and revenue pre-approval |
| Pharma / devices | P/E vs pipeline, FCF yield, dividend coverage | P/E without patent-cliff adjustment |
| Retail | P/E, lease-adjusted EV/EBITDA, FCF yield, comps trend | Revenue growth without comps/inventory; leverage ignoring leases |
| Consumer staples | P/E, dividend yield, FCF yield, organic growth | Headline growth without volume/price split |
| Industrials | EV/EBITDA, mid-cycle P/E, FCF yield, ROIC, backlog | Peak-cycle P/E; one quarter of orders |
| Transportation | EV/EBITDA, P/E, FCF yield, operating ratio vs sub-mode peers | Cross-subsector margin comparisons |
| Telecom | EV/EBITDA, FCF yield, dividend coverage | EPS / P/E |

## Sources & update discipline

**Source hierarchy:** company filings and audited statements first; investor presentations are useful but promotional; third-party screeners must be checked against filings.

**Provenance labels (v4 standard):** every key metric carries exactly one label. The label reflects what the review itself verified, not how plausible the number is:

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

**Conflicting figures rule (universal):** when two figures for the same metric appear to conflict, do not choose one immediately. First classify the difference: 1. different scope — group vs segment, consolidated vs ex-subsidiary · 2. different basis — gross vs net, reported vs adjusted · 3. different period — quarterly, annualized, LTM, fiscal year · 4. different currency · 5. different definition — company-defined vs packet-defined. Show both figures with provenance labels, then rate the pillar based on the figure that best matches the packet definition. If neither figure matches the packet definition, keep the pillar at Watch or Needs verification.

**Estimated proxy:** when a metric is calculated from available inputs but does not match the company's exact disclosed definition, label it **"Estimated proxy"** and state the inputs used. Examples: an AFFO payout proxy estimated above 100% when AFFO itself is not disclosed; an interest coverage proxy estimated from verified income-statement inputs but not company-disclosed; a net debt/EBITDAre proxy estimated when EBITDAre is not disclosed or JV/pro-rata treatment is unresolved. Never imply the proxy is the same as the company's official metric: a proxy is a sub-type of Estimated, is never Verified, never High confidence, and any rating that rests on it must say so.

**Guidance is not achievement:** guidance, targets, and management plans can support a Watch or directional comment, but they should not receive full Positive credit unless supported by achieved results, binding regulatory approval, or directly verified realized performance. This applies especially to: utilities rate-base growth guidance · REIT rent ramp / stabilized rent targets · energy production or capex targets · SaaS margin expansion targets · bank medium-term ROE targets.

Ranges are rules of thumb calibrated June 2026 — refresh at least annually from current sector medians (e.g., Damodaran NYU datasets), rebuilt peer groups, and re-anchored cycle numbers.

## Neutral research conclusion language

| Conclusion | When to use |
|---|---|
| Strong on current evidence | Most pillars Positive, no Severe flags, valuation reasonable, data confidence High |
| Mixed / needs more evidence | Score ~50–75% or open questions; name the specific evidence needed |
| Weak on current evidence | Score <50% with sufficient evidence and no verified Severe flag — clearly weak, but not a special situation |
| High-risk / special situation | Verified Severe flag(s), or binary outcomes dominate |
| Insufficient data | Key metrics unverifiable from primary sources; state what is missing |

## Reusable AI stock-analysis prompt

> Analyze [company name / ticker] using the uploaded Core Framework and the uploaded [sector] guide.
> Do not use buy/sell/hold language.
> Please provide:
> 1. Business model summary
> 2. Correct sector classification
> 3. Peer group and why those peers are appropriate
> 4. Key sector metrics
> 5. Company values versus peers and 5-year history
> 6. Positive / Watch / Negative assessment
> 7. Severe red flags, if any
> 8. Valuation method appropriate for the sector
> 9. Data confidence level: High, Medium, or Low
> 10. Neutral research conclusion: strong on current evidence; mixed / needs more evidence; high-risk / special situation; or insufficient data
>
> Use primary sources where possible, such as 10-Ks, 10-Qs, annual reports, earnings releases, and regulatory filings. Do not rely only on screeners or summaries.
