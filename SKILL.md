---
name: stock-review
description: Fast, sector-aware fundamental stock review using the user's Stock Analysis Guide (v2.x packets), with a progressive workflow — compact scorecard first, deep dives on demand. Use this skill whenever the user asks to analyze, review, evaluate, score, or "run the guide" on a stock, ticker, or public company — e.g. "review DKNG", "analyze JPMorgan", "what does the guide say about NVDA", "stock review O" — and also for the follow-up actions it offers — "make deeper analysis", "verify missing data", "compare vs peers", "deep dive valuation/risks", "create full research memo". It classifies the company into one of 23 sectors, loads only that sector's packet, researches primary sources, and produces a neutral research conclusion. Never produces buy/sell/hold advice.
---

# Stock Review (Progressive, Guide-Driven, Sector-Aware)

Analyze one public company using the Stock Analysis — Sector-by-Sector Guide (v2.x packets). Core principle: **the first response is a research dashboard, not an investment memo.** Its job is to show whether the company deserves deeper research and which areas need verification. Full analysis happens only when the user asks for it — this keeps token usage proportional to interest.

The guide's analytical insight still governs everything: every sector has its own metrics, its own "what NOT to use" list, and its own valuation toolkit. Importing another sector's metrics is the most common analytical mistake.

## Step 1 — Classify the company

Determine where the majority of **operating profit** (not revenue) comes from. For mixed businesses, pick the dominant segment's packet and note that other large segments deserve a separate pass.

File preference (most token-efficient first): (1) the user's maintained markdown packets at `Stock_Analysis_Modular/Markdown/AI_Packets/` if that folder is available; (2) the bundled copy in this skill's `references/`. Read ONLY the one sector packet needed. Read `references/01_Core_Framework.md` only when sector classification is unclear, the business is mixed, or a universal rule needs detail.

| Sector | Packet file |
|---|---|
| Banks | AI_Packet_Banks.md |
| Insurers | AI_Packet_Insurers.md |
| Asset managers, exchanges, data providers | AI_Packet_Asset_Managers_Exchanges.md |
| Fintech, card networks, processors | AI_Packet_Fintech_Payments.md |
| Software, SaaS, internet, IT services | AI_Packet_Software_SaaS.md |
| Semiconductors, hardware, defense electronics | AI_Packet_Electronic_Technology.md |
| Pharma, biotech, medical devices | AI_Packet_Health_Technology.md |
| Hospitals, health insurers, providers | AI_Packet_Health_Services.md |
| REITs and property companies | AI_Packet_REITs.md |
| Electric, gas, water utilities | AI_Packet_Utilities.md |
| Oil & gas | AI_Packet_Energy_Oil_Gas.md |
| Miners, steel, materials | AI_Packet_Mining_Metals.md |
| Chemicals, paper, packaging | AI_Packet_Process_Industries.md |
| Machinery, capital goods | AI_Packet_Producer_Manufacturing.md |
| Oilfield services, E&C, rental | AI_Packet_Industrial_Services.md |
| Rail, airlines, trucking, shipping | AI_Packet_Transportation.md |
| Food, beverage, household brands | AI_Packet_Consumer_Staples.md |
| Autos, appliances, homebuilders | AI_Packet_Consumer_Durables.md |
| Store/e-commerce retailers | AI_Packet_Retail.md |
| Restaurants, hotels, leisure, gaming | AI_Packet_Consumer_Services.md |
| Telecom carriers, satellite | AI_Packet_Communications_Telecom.md |
| Staffing, consulting, info services | AI_Packet_Commercial_Services.md |
| Wholesale distributors | AI_Packet_Distribution_Services.md |

Tower companies are REITs. Pre-commercial biotech follows Health Technology's cash-runway logic. A fintech with a banking charter gets the Banks packet for its lending book.

## Step 2 — Bounded first-pass research

Keep research proportional to a first pass: the latest earnings release / quarterly filing plus one or two targeted searches for the packet's headline metrics, current price/valuation, and anything matching the packet's red-flag list. Do NOT do exhaustive peer research yet — that belongs to the "Compare vs peers" action.

Source hierarchy: company filings (10-K, 10-Q, annual report, earnings release) first; investor presentations second; screeners/aggregators last, only to fill gaps. Record source and date for key figures. Never invent a number — not capital ratios, NRR, CAC payback, AFFO, reserve life, breakevens, NPLs, peer medians, or analyst targets. A metric that can't be verified is marked "needs verification" and costs confidence (and pillar credit, if it's important).

## Step 3 — First-pass scorecard (the default output)

Concise and dashboard-like. Short text + visual widget (see Step 5). Structure:

**A. Header** — company, ticker, sector packet used, analysis date, data-freshness note (e.g., "latest filing: Q1 10-Q, May 2026").

**B. Five to six key metric cards** — the weighted score plus the 4–5 most decision-relevant metrics *for that sector* (banks: ROE/ROTE, NIM, NPLs/charge-offs, CET1, P/B-with-ROE; SaaS: growth, Rule of 40, NRR, FCF margin, SBC/dilution, EV/Sales; REITs: FFO/AFFO growth, AFFO payout, occupancy, debt/EBITDAre, P/FFO or NAV; energy: FCF yield, corporate breakeven, net debt/EBITDA, reserve life, shareholder yield). Each with its Positive/Watch/Negative verdict.

**C. Pillar ratings** — the packet's weights; for each pillar: name, weight, rating (Positive=2 / Watch=1 / Negative=0), and a one-line reason. Weighted total ÷ 2 = 0–100% score. Label ratings **provisional** where peer comparison hasn't been done yet — a first pass can check ranges and own history, but the four-comparisons test is only complete after peer work. The score is a research organizer, not a prediction engine.

**D. Severe red-flag override** — any Severe flag supported by **Verified** or **Calculated — verified inputs** evidence caps the score at 50%; two or more usually mean high-risk / special situation. If a candidate Severe flag lacks that evidence in the first pass, label it "unverified — needs verification" and do NOT cap yet; say what would verify it.

**E. Expectations check** — run the Core Framework's expectations test when the valuation pillar would rest on a multiple above the company's own 5-year range, or when the thesis rests on segments with no achieved results. State what the current price requires (revenue CAGR over a stated horizon, steady-state margin, reinvestment, discount rate) and the residual — unproven — share of enterprise value; where the loaded packet defines an expectations adaptation, it replaces these variables and the split (Banks and Insurers: required ROE/ROTE solved from P/B or P/TBV and the cost of equity, residual share of market cap — insurance brokers keep the standard form), label the outputs "Estimated — expectations-implied", and apply the valuation-pillar caps. If the test is not triggered, say so in one line.

**F. Red flags** — each with severity (Severe/Moderate/Minor), what it is, why it matters, and its status: verified / estimated / needs verification.

**G. Data confidence** — High (recent filings/official disclosures) / Medium (presentations, calls, reputable providers) / Low (incomplete, stale, estimates). Name what's missing.

**H. Neutral research conclusion** — exactly one of: **strong on current evidence** / **mixed, needs more evidence** (name it) / **weak on current evidence** (score <50% with sufficient evidence and no verified Severe flag) / **high-risk, special situation** / **insufficient data**. One- or two-sentence thesis with what would break it.

End every review with: *"This is general information only and not financial advice. For personal guidance, please talk to a licensed professional."*

## Step 4 — Offer follow-up actions

After the scorecard, offer these actions — as widget buttons if a widget tool exists, otherwise a numbered list:

1. Make deeper analysis
2. Verify missing data
3. Compare vs peers
4. Deep dive: valuation
5. Deep dive: risks
6. Deep dive: [the company's weakest/sector-specific area — adapt: banks → credit quality / capital / deposits; SaaS → retention & Rule of 40 / SBC & dilution; REITs → dividend coverage / debt maturities / NAV; energy → breakevens / reserves / capital discipline]
7. Create full research memo

When the user selects an action (by button or words), read `references/deep_dives.md` and follow the matching section. Do not load it before then.

## Step 5 — Visual scorecard (when a widget tool is available)

Render the first-pass scorecard as a compact inline widget (call the visualization `read_me` setup first, silently): header with conclusion badge (teal = strong, amber = mixed, orange = weak, red = high-risk, gray = insufficient data); metric cards (score first, with "no Severe cap" / "capped at 50%" subtext); pillar bars filled 0/50/100% colored red #E24B4A / amber #EF9F27 / teal #1D9E75; red-flag severity pills (Severe red, Moderate amber, Minor gray) including verification status; action buttons from Step 4 wired to `sendPrompt`; footer disclaimer. Theme-aware CSS variables, flat design, round all numbers. The widget shows the same numbers as the text — never new claims. No widget tool → numbered action list in text instead.

## Verification standard (strict)

"Verified" is a protected word. A metric may be marked **verified** — and may change a pillar rating or the score — only when ALL of the following can be shown:

1. Metric name
2. Exact value
3. Exact source document (filing type and date)
4. Exact location: page, table name, or section heading
5. A short quote or extracted line showing the label next to the value
6. Why the label matches the sector guide's definition of the metric
7. Whether it updates a rating, and what the score becomes

Anything less is **estimated** or **needs verification** — usable context, never pillar-upgrade evidence. Search-engine summaries, AI overviews, and aggregator paraphrases are NEVER verification, even when they cite a filing: the score may only move on text actually read from the source document.

**Label-match rule:** never reuse a percentage from a nearby table unless the label exactly matches the intended metric. If the filing shows "Efficiency Ratio 16.6%," it cannot be used as CAR, CET1, capital adequacy, or any other capital metric. Identical values for different metrics in the same filing are a known trap — when two candidate numbers match, treat both as suspect until the labels are read.

**Bank capital disambiguation:** the Banks packet's seven-row disambiguation table is authoritative — CET1, Tier 1, CAR, regulatory requirement, excess capital, liquidity position, and efficiency ratio are different things; never substitute one for another. If the exact group-level capital ratio is not found in a readable source, write "Capital ratio not directly disclosed / needs verification" — and do NOT raise the capital pillar to Positive on compliance statements, dollar capital amounts alone, or computed estimates.

## Retrieval resilience for long filings

A truncated fetch is not a dead end. If a filing fetch cuts off before the needed table or note, do not immediately mark the metric unavailable. Important financial-statement notes — capital, credit quality, reserves, segment data, maturities, and risk disclosures — often appear near the end of long filings.

Run this fallback ladder in order:

1. **Search the saved or accessible filing text** for the target labels before anything else. A fetch may be truncated in the visible output but still searchable in saved text or page extraction.
2. **Run label-specific searches** within whatever filing text is readable. Adapt the labels to the metric being verified.
   For bank capital, search:
   - CET1
   - Common Equity Tier 1
   - Tier 1 ratio
   - CAR
   - capital adequacy
   - Capital management
   - minimum capital required
   - excess margin
   - regulatory capital
3. **Open the filing around the matched section or note.** Use browser page extraction when the normal fetch tool hits a size limit. Retry if the browser extension is temporarily disconnected.
4. **Try alternate versions of the same filing**, including:
   - same-day exhibits,
   - attached financial statements,
   - related 6-K, 10-Q, 20-F, or annual-report exhibits,
   - FilingSummary.xml,
   - XBRL or R-file note documents,
   - complete-submission text files only when the filing is small enough to load reliably.
5. **Try regulator or Pillar 3 disclosures** if the company filing does not expose the metric clearly. For banks, this may include central-bank filings, prudential disclosures, call reports, or local regulatory capital documents.
6. Only after these fallbacks fail, report the metric as:
   **"Capital ratio not directly disclosed / needs verification"**
   or the equivalent wording for the missing metric.

When reporting failure, name:

- the document checked,
- the section or note where the metric likely sits,
- what was readable,
- what was not accessible,
- and the best next source to verify it.

### Verification boundary

A metric may be marked **Verified** only when the skill itself has read the exact source label next to the value and can quote it.

Relayed tables, evaluator comments, search summaries, and aggregator snippets can improve context, but they cannot verify a metric.

If a value is supplied by another evaluator but the skill has not read it directly, label it:
**"Reported, pending direct verification."**
That status is Medium confidence at most, never High confidence, and never enough by itself to upgrade a pillar.

**Provenance labels** — the confidence label must reflect what the skill actually verified, not how plausible the number is:

| Label | Meaning |
|---|---|
| **Verified** | The skill itself directly read the source document and quotes the exact label next to the value |
| **Calculated — verified inputs** | Derived by a stated, reproducible formula whose inputs are each individually Verified; derived ratios are never plain "Verified" |
| **User-provided filing excerpt** | The user pasted verbatim filing text containing the label and value; the skill quotes it, but could not independently open the document. Usable for rating decisions with provenance stated; not "Verified" |
| **Reported, pending direct verification** | The value came from the user, another AI, an evaluator, a search summary, or a relayed table without verbatim source text |
| **Estimated** | Derived from market data, aggregators, or calculation |
| **Needs verification** | An important metric not found or not confirmed |
| **Not disclosed** | Relevant primary sources were checked and do not contain the metric; this is a disclosure fact, not a performance judgment |

External confirmation may inform the analysis, but it never upgrades the confidence label to Verified — only the skill independently reading the source does that. A derived ratio takes **Calculated — verified inputs** only when every input is Verified; otherwise it inherits the weakest input's label. A score can use reported data cautiously, but only Verified or Calculated — verified inputs evidence can activate a Severe-flag cap.

### Verification affects confidence, not rating

Verification proves that the number is real. It does not decide whether the number is good.

The rating still follows the relevant sector packet's thresholds, trend rules, and context.

Verified does not mean Positive.

Examples:

- A verified CET1 ratio of 11.3%, in the 10–12% Watch band and declining, is still **Watch**, not Positive.
- A verified AFFO payout ratio for a REIT still rates according to the REIT packet's payout thresholds. Verification does not automatically make the dividend safe.

## Hard rules

- No buy/sell/hold/accumulate/avoid language, no price targets (external analyst consensus may be quoted with source), no position sizing — educational research organization only.
- Respect the packet's "what NOT to use" list (no EV/EBITDA for banks, no standard P/E for REITs, no P/E for pre-commercial biotech, low P/E ≠ cheap for cyclicals at peak).
- Cite sources with dates for key figures; mark every estimate as an estimate; state clearly when data is missing, stale, or unverified.
- If the company can't be verified from primary sources at all, conclude "insufficient data" rather than leaning on screeners.
- Always end with the disclaimer line from Step 3G.
