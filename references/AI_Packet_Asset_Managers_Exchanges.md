# AI Stock Review Packet: Asset Managers & Exchanges

**Version 2.1.1 — Last updated 2026-10-08.** Supersedes v2.1. Consistency update: five conclusion labels, Core provenance and evidence rules, Severe-cap eligibility, and required first-pass Core loading for the expectations test. Sector metrics, thresholds, red flags, and pillar weights are unchanged. Educational framework — not investment advice. No buy/sell/hold language.

*Asset managers, brokers, stock exchanges, data providers* — GICS: Financials (Financial Services / Capital Markets)

## Prompt

> Analyze [company name / ticker] using the uploaded Core Framework and the uploaded Asset Managers & Exchanges guide.
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

## Sector: Asset Managers & Exchanges

Asset-light toll collectors on markets. Asset managers live and die by net flows and fee rates; exchanges and data providers are near-monopolies with very high margins and recurring revenue. Market downturns hit assets under management (AUM) and revenue automatically.

| Metric | Positive | Watch | Negative | How to read it |
|---|---|---|---|---|
| **AUM growth & net flows** | Positive organic flows | Flat | Persistent outflows | Market gains can mask outflows — separate the two. |
| **Fee rate trend** | Stable | Slow decline | Rapid decline | Fee compression is the structural headwind for active managers. |
| **Operating margin** | > 30% | 20–30% | < 20% | Exchanges/data: often 40–60%; active managers lower. |
| **Recurring revenue %** | > 70% | 40–70% | < 40% | Subscriptions and listing fees beat transaction-driven revenue. |
| **ROIC** | > 15% | 10–15% | < 10% | Asset-light models should earn high returns. |
| **Net debt/EBITDA** | < 2x | 2–3x | > 3x | Normal corporate leverage rules apply here (unlike banks). |

**Formulas:** Organic flow rate = net new client money ÷ beginning AUM. Average fee rate = management fee revenue ÷ average AUM. Recurring revenue % = subscription + listing + asset-based fees ÷ total revenue.

**What NOT to use:** Book value multiples (these are asset-light businesses — P/B is uninformative); net interest margin; single-year AUM growth during a bull market (it is mostly the market, not the manager).

**Valuation — use:** P/E versus organic flow growth; EV/EBITDA; FCF yield. Exchanges and data providers justify premium multiples via recurring revenue. **Avoid:** P/B (asset-light); AUM growth during bull markets without separating market effect from net flows.

**Red flags:**

- **Severe** — Sustained net outflows across multiple flagship products
- **Moderate** — Fee rate declining faster than costs can be cut
- **Moderate** — Revenue heavily dependent on trading volumes (cyclical)
- **Minor** — Key-person dependence in a star-manager firm

## Scoring template

| Pillar | Weight | Rating 0–2 | Notes |
|---|---|---|---|
| Net flows / AUM trend | 30% |  |  |
| Operating margin & leverage on scale | 25% |  |  |
| Fee-rate pressure / recurring mix | 15% |  |  |
| Balance sheet | 10% |  |  |
| Valuation | 20% |  |  |

Score each pillar 2 (Positive), 1 (Watch), 0 (Negative) vs peers and own history; weighted total ÷ 2 = 0–100%. ~75%+ strong on current evidence; 50–75% mixed — investigate the weak pillar; <50% with sufficient evidence and no qualifying Severe flag = weak on current evidence. The score is a research organizer, not a prediction engine.

**Override rule:** any Severe red flag supported by **Verified** or **Calculated — verified inputs** evidence caps the total score at 50% until resolved. Show the uncapped score, the cap applied, and the displayed score. Two or more qualifying Severe flags usually mean **high-risk, special situation**. Candidate Severe flags resting on user-provided excerpts, Reported, Estimated, or Needs verification evidence remain provisional warnings and do not activate the cap; state what would verify them.

## Conclusion template

End with exactly one of: **strong on current evidence** / **mixed, needs more evidence** (name it) / **weak on current evidence** (score <50% with sufficient evidence and no qualifying Severe flag) / **high-risk, special situation** / **insufficient data** — plus data confidence (High/Medium/Low) and a two-sentence thesis including what would break it. No buy/sell/hold language.
