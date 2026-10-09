# AI Stock Review Packet: Distribution Services

**Version 2.1.2 — Last updated 2026-10-08.** Supersedes v2.1.1. Shared scoring update: delegates applicability, band precedence and Severe-cap conditions to Core v2.1.8; each Severe flag now states the company-specific condition that activates the cap. Pillar weights are unchanged. v2.1.1 aligned the five conclusion labels, evidence rules, Severe-cap provenance and first-pass Core loading. Educational framework — not investment advice. No buy/sell/hold language.

*Wholesale distributors of food, electronics, medical, industrial goods* — GICS: Industrials (Trading Companies & Distributors); food/drug wholesale in Consumer Staples (Distribution & Retail)

## Prompt

> Analyze [company name / ticker] using the uploaded Core Framework and the uploaded Distribution Services guide.
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

## Sector: Distribution Services

Razor-thin margins, high volume. The business is logistics and working-capital efficiency, not pricing power. Inventory turns, ROIC, and scale decide the winners — fast turns let a 3% margin business earn excellent returns on capital.

| Metric | Positive | Watch | Negative | How to read it |
|---|---|---|---|---|
| **Revenue growth** | > 6% | 2–6% | < 2% | Tied to end-market demand and share gains. |
| **Operating margin** | > 6% | 3–6% | < 3% | Structurally thin — efficiency is everything. |
| **Inventory turns** | High & stable | Slowing | Falling | The core efficiency metric for distributors. |
| **Cash conversion cycle** | Short / negative | Stable | Lengthening | Working capital is the business; watch it closely. |
| **ROIC** | > 12% | 8–12% | < 8% | Low margins can still earn high returns via fast turns. |
| **Net debt/EBITDA** | < 2.5x | 2.5–3.5x | > 3.5x | Watch working-capital swings on the balance sheet. |

**Formulas:** Inventory turns = COGS ÷ average inventory. Cash conversion cycle = inventory days + receivable days − payable days. ROIC = NOPAT ÷ invested capital.

**What NOT to use:** Gross or operating margin comparisons with other sectors (2–6% is normal here, not a weakness); revenue growth without margin and turns context; EV/Sales.

**Valuation — use:** P/E, EV/EBITDA, and FCF yield; ROIC and cash conversion cycle as the operational screens. **Avoid:** EV/Sales; margin comparisons with other sectors; revenue growth without turns and margin context.

**Red flags:**

- **Severe** — Large customers squeezing margins below cost of capital returns. *Condition:* the company attributes a margin decline to repricing, renewal on lower terms, or loss of one or more large customers (state their share of revenue), and the operating result of the affected segment or of the group turns negative as a result. Returns below an estimated cost of capital alone are Moderate — an estimate cannot activate the cap.
- **Moderate** — Inventory obsolescence in fast-moving categories (electronics)
- **Moderate** — Disintermediation — suppliers selling direct
- **Minor** — Temporary working-capital build ahead of a season

## Scoring template

**Shared scoring rules:** apply the Core Framework section "Shared scoring rules: applicability, bands, and Severe conditions" before rating pillars, computing the percentage, or applying a Severe cap.

| Pillar | Weight | Rating 0–2 | Notes |
|---|---|---|---|
| Inventory turns / working capital | 30% |  |  |
| ROIC | 25% |  |  |
| Margin trend | 15% |  |  |
| Balance sheet | 15% |  |  |
| Valuation | 15% |  |  |

Score each pillar 2 (Positive), 1 (Watch), 0 (Negative) vs peers and own history; weighted total ÷ 2 = 0–100%. ~75%+ strong on current evidence; 50–75% mixed — investigate the weak pillar; <50% with sufficient evidence and no qualifying Severe flag = weak on current evidence. The score is a research organizer, not a prediction engine.

**Override rule:** any Severe red flag whose written condition is met on **Verified** or **Calculated — verified inputs** evidence caps the total score at 50% until resolved. Show the uncapped score, the cap applied, and the displayed score. Two or more qualifying Severe flags usually mean **high-risk, special situation**. Candidate Severe flags resting on user-provided excerpts, Reported, Estimated, or Needs verification evidence remain provisional warnings and do not activate the cap; state what would verify them.

## Conclusion template

End with exactly one of: **strong on current evidence** / **mixed, needs more evidence** (name it) / **weak on current evidence** (score <50% with sufficient evidence and no qualifying Severe flag) / **high-risk, special situation** / **insufficient data** — plus data confidence (High/Medium/Low) and a two-sentence thesis including what would break it. No buy/sell/hold language.
