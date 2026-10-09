# AI Stock Review Packet: Retail

**Version 2.1.2 — Last updated 2026-10-08.** Supersedes v2.1.1. Shared scoring update: delegates applicability, band precedence and Severe-cap conditions to Core v2.1.8; each Severe flag now states the company-specific condition that activates the cap; the same-store-sales Watch band now covers 0–1% and Negative is defined as below 0%. Pillar weights are unchanged. v2.1.1 aligned the five conclusion labels, evidence rules, Severe-cap provenance and first-pass Core loading. Educational framework — not investment advice. No buy/sell/hold language.

*Stores, e-commerce, omnichannel retailers* — GICS: Consumer Discretionary (Consumer Discretionary Distribution & Retail); grocers/drugstores in Consumer Staples (Distribution & Retail)

## Prompt

> Analyze [company name / ticker] using the uploaded Core Framework and the uploaded Retail guide.
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
> 10. Neutral research conclusion: strong on current evidence / mixed, needs more evidence / weak on current evidence / high-risk, special situation / insufficient data
>
> Use primary sources where possible, such as 10-Ks, 10-Qs, annual reports, earnings releases, and regulatory filings. Do not rely only on screeners or summaries.

## Evidence and Core loading

Read the Core Framework alongside this packet before scoring: use `Stock_Analysis_Modular/Markdown/01_Core_Framework.md` with the maintained packets, or `references/01_Core_Framework.md` with the bundled packets. This packet inherits the Core expectations module; load it during the first pass and run the test whenever its triggers apply, without waiting for a requested deep dive. Apply its valuation-pillar caps and label test outputs **Estimated — expectations-implied**. If the Core cannot be read or a triggered test cannot be completed, valuation is **Needs verification** and scores no higher than Watch; state the missing evidence or access.

Every key metric carries exactly one of the seven Core provenance labels. Verified requires the review to directly read the intended label next to the exact value, identify the source document and date, locate the table or section, quote the source line, explain the definition match, and state the rating/score impact. Search summaries, model-generated summaries, and relayed figures cannot verify a metric. **Verified does not mean Positive.**

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

**Score-change audit trail:** show the previous and updated score, the metric or basis that changed, old status, new factual value and provenance, source document, exact label/value quote, pillar affected, and reason. For assumption, judgment, arithmetic, or framework changes, name the change type and explain the revised basis; mark factual value/source/quote not applicable only when no factual input changed. Verification alone does not improve a rating.

## Universal checklist

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

**Peer group:** 5–10 names sharing business model, geography, growth stage, margin structure, capital intensity, regulation, customer type, cyclicality. A sector label is not a peer group.

**Quality of earnings:** Profits converting into cash? Over 3–5 years FCF should roughly track net income. FCF consistently and materially below net income? Investigate the gap. 'Adjusted' earnings much higher than GAAP, year after year? Same 'one-time' add-backs recurring every year? Working capital temporarily flattering cash flow? Acquisitions masking weak organic growth? Watch goodwill build. Revenue recognized aggressively? Receivables outgrowing revenue is a warning. Margin gains from real operating leverage — or accounting changes?
Rule: high-quality earnings are recurring, cash-backed, not dependent on repeated adjustments.

**Geography/currency:** Where is revenue generated? Where are profits generated (often different)? Where are assets located? Can they be taken or stranded? What currencies are revenue and costs in? Any mismatch? What currency is the debt in? FX debt vs local revenue is the classic blow-up. Politically risky jurisdictions — expropriation, licenses, rule of law? Could tariffs, sanctions, capital controls, tax changes, or regulation hit the model?

## Sector: Retail

A thin-margin volume game. Same-store sales and inventory management are everything; a few points of margin swing is huge. Revenue growth means little without comps and inventory trends, and leases are real debt — adjust for them.

| Metric | Positive | Watch | Negative | How to read it |
|---|---|---|---|---|
| **Same-store sales growth** | > 4% | 0–4% | < 0% | The single most-watched retail metric; split traffic vs ticket. |
| **Gross margin trend** | Stable / rising | Slipping | Falling fast | Level varies widely by format; trend vs peers is what matters. |
| **Markdown & shrink trend** | Low & stable | Rising | Spiking | Markdowns = demand misjudged; shrink (theft/loss) eats thin margins. |
| **Inventory turns** | High & stable | Slowing | Falling | Slow turns = markdowns coming and cash tied up. |
| **Online penetration & economics** | Growing profitably | Growing at a loss | Stalling | E-commerce growth must come with acceptable fulfillment costs. |
| **Return rate (e-commerce)** | Low / falling | Stable | High / rising | Returns can quietly destroy online profitability. |
| **CAC (e-commerce)** | Falling, < LTV | Stable | Rising toward LTV | Paid-acquisition dependence is fragile. |
| **Lease-adjusted leverage** | < 3x | 3–4x | > 4x | Leases are debt; ignore them and retail balance sheets look deceptively clean. |

**Formulas:** Same-store (comparable) sales = sales growth from stores open 12+ months. Inventory turns = COGS ÷ average inventory. Shrink = inventory losses (theft, damage, error) ÷ sales. Lease-adjusted leverage = (net debt + capitalized operating leases) ÷ EBITDAR. CAC = sales & marketing spend ÷ new customers acquired. Online penetration = e-commerce revenue ÷ total revenue.

**What NOT to use:** Revenue growth without same-store sales (new stores can mask decaying ones); net debt/EBITDA that ignores leases; gross margin comparisons across formats (grocery vs luxury); single-quarter comps against an easy prior-year comparison.

**Valuation — use:** P/E and lease-adjusted EV/EBITDA; FCF yield; comps trend as the primary health gauge. **Avoid:** Revenue growth without comps and inventory; leverage metrics ignoring leases; cross-format margin comparisons.

**Red flags:**

- **Severe** — Negative comps plus rising inventory — the markdown spiral. *Condition:* comparable sales are negative and inventory grows faster than sales in at least two consecutive quarters on a matched scope (same store base, acquisitions excluded), with gross margin falling over the same periods. A build the company disclosed in advance is context to weigh, not an exemption. Negative comps with inventory in line is Moderate.
- **Moderate** — Markdowns and shrink rising together
- **Moderate** — Losing share to online/discount competitors
- **Minor** — One soft quarter against a tough prior-year comp

## Scoring template

**Shared scoring rules:** apply the Core Framework section "Shared scoring rules: applicability, bands, and Severe conditions" before rating pillars, computing the percentage, or applying a Severe cap.

| Pillar | Weight | Rating 0–2 | Notes |
|---|---|---|---|
| Comps / traffic | 30% |  |  |
| Margins & inventory discipline | 25% |  |  |
| Online & competitive position | 15% |  |  |
| Lease-adjusted balance sheet | 15% |  |  |
| Valuation | 15% |  |  |

Score each pillar 2 (Positive), 1 (Watch), 0 (Negative) vs peers and own history; weighted total ÷ 2 = 0–100%. ~75%+ strong on current evidence; 50–75% mixed — investigate the weak pillar; <50% with sufficient evidence and no qualifying Severe flag = weak on current evidence. The score is a research organizer, not a prediction engine.

**Override rule:** any Severe red flag whose written condition is met on **Verified** or **Calculated — verified inputs** evidence caps the total score at 50% until resolved. Show the uncapped score, the cap applied, and the displayed score. Two or more qualifying Severe flags usually mean **high-risk, special situation**. Candidate Severe flags resting on user-provided excerpts, Reported, Estimated, or Needs verification evidence remain provisional warnings and do not activate the cap; state what would verify them.

## Conclusion template

End with exactly one of: **strong on current evidence** / **mixed, needs more evidence** (name it) / **weak on current evidence** (score <50% with sufficient evidence and no qualifying Severe flag) / **high-risk, special situation** / **insufficient data** — plus data confidence (High/Medium/Low) and a two-sentence thesis including what would break it. No buy/sell/hold language.
