# AI Stock Review Packet: Pre-Revenue Overlay

**Version 1.1 — Last updated 2026-10-08 (analysis as-of date: October 8, 2026).** New cross-sector packet for companies whose core commercial revenue is immaterial; routed BEFORE operating-profit sector classification. v1.1 (same day, after the Oklo test): splits the runway pillar into liquidity and dilution sub-ratings with a combination rule; replaces the 25% dilution cut-off with persistence and economic-impact tests; removes the overlapping Watch/Negative criteria in the commercialization pillar; defines the catalyst, the post-catalyst buffer, interest-income treatment, partial forward plans, slip measurement, missing-evidence scoring, and when binary outcomes "dominate". Pre-commercial biotech stays with Health Technology Branch 2. Educational framework — not investment advice. No buy/sell/hold language.

*Advanced nuclear / SMR, eVTOL and new aviation, space and launch, mining developers and explorers, pre-revenue deep tech and hardware, pre-commercial clean energy technology.*

**Core principle: a company with no operating profit cannot be routed by operating profit.** Development-stage companies are judged on gates, cash and dilution — not on the sector metrics they will only have after commercial operation. Applying utility, transportation, or producer-mining metrics to a company that has not started operating is this packet's defining mistake. Verified does not mean Positive.

## Prompt

> Analyze [company name / ticker] using the uploaded Core Framework and this Pre-Revenue Overlay. State the analysis as-of date.
> Do not use buy/sell/hold language.
> Provide: 1. Business model summary · 2. Core-revenue materiality test and route · 3. Sub-branch and critical gates · 4. Runway, financing and dilution · 5. Contract evidence · 6. Pillar ratings with provenance labels · 7. Severe red flags, if any · 8. Proven vs unproven EV and expectations test · 9. Data confidence · 10. Neutral research conclusion.
> Use primary sources (10-K, 10-Q, 20-F, 6-K, 8-K, prospectus supplements, regulator dockets and decisions). Do not rely only on press releases, screeners, or summaries.

## Inheritance rule

This overlay inherits every Core Framework mechanism and references it by name; it defines no parallel version. Load order: **Core Framework → this overlay → the sector packet's context metrics and red-flag list only** (mark sector red flags that cannot apply before operation "N/A — pre-operational").

| Mechanism | Where it lives | Used here as |
|---|---|---|
| Provenance labels (v4 standard) | Core | Every metric carries one label |
| Conflicting figures rule | Core | As written |
| Estimated proxy | Core | As written |
| Guidance is not achievement | Core | Covers target dates, deployment years, cost-down and capacity plans |
| Expectations are not results · Proven vs unproven enterprise value · Estimated — expectations-implied | Core | The valuation pillar |
| Red-flag severity & override rule | Core | Flags below plug into it; no second penalty mechanism |
| Neutral research conclusion language | Core | Five categories, with the Overlay-specific "binary outcomes dominate" test below |
| Scoring arithmetic (Positive 2 / Watch 1 / Negative 0; weight × rating ÷ 2) | SKILL.md Step 3 and the strict packets — Core does not define it | As written |
| Liquidity, normalized burn, base and forward runway, ≥6-month delay sensitivity, post-catalyst buffer, no double-counting of risk | Health Technology Branch 2 | Restated below with adaptations shown in brackets; Branch 2 governs if wording diverges |

Where Core and Branch 2 are silent, this overlay adds a rule marked **Overlay-specific**. Core has no general missing-evidence scoring rule and no "what NOT to use" table (its closest equivalent is the "Avoid" column of *Valuation methods by sector*); both gaps are handled below and in the pending Core diff.

## Core-revenue materiality test (trigger)

**Numerator — TTM core commercial revenue.** Exclude interest income and revenue from acquired businesses unrelated to the core thesis. Show grants, development/engineering fees, and pilot/demo revenue on separate lines. Count a line as core only when ALL apply: (a) earned from external customers, (b) under contract on commercial terms, (c) recurring or contracted to recur, (d) part of the company's intended commercial business model. Justify each classification in writing. **Overlay-specific:** legacy third-party revenue of businesses acquired for supply-chain or engineering capability is non-core unless that service is itself part of the intended commercial model; if criteria (a)–(d) cannot be confirmed from filings, the line is non-core and the reason is stated.

**Denominator — TTM cash operating costs** = cost of revenue + operating expenses − SBC − D&A − other identified noncash charges included in those lines. Reconcile each adjustment to the financial statements. Show exceptional cash costs separately and justify any exclusion. Capex and acquisitions are excluded but shown alongside. This routing denominator is distinct from the runway burn below.

**Threshold:** ratio < 25% → overlay applies. This is a routing heuristic, not an economic threshold. Ratios of 15–35% are borderline and require a written justification for the route chosen. TTM = most recent four reported quarters (FY − prior-year YTD + current YTD); state the period.

## Routing precedence, graduation and transition

Run the test BEFORE operating-profit sector classification.

- **Pre-commercial biotech** → Health Technology Branch 2 (authoritative; the overlay defers).
- **Everyone else** → this overlay scores the company. The sector packet supplies context metrics and its red-flag list only.
- **Graduation:** the rolling TTM ratio is ≥ 25% at four consecutive quarter-ends AND the sector packet's headline metrics can be applied meaningfully. Passing a gate or starting commercial operation alone is not enough.
- **Transition period** (from the first quarter-end at ≥ 25% until graduation): report both the overlay score and the sector-packet score; the conclusion names which one it rests on and why.
- **Multi-business developers** (e.g., power + fuel + isotopes): pick the sub-branch whose gates carry most of the estimated EV and say which other gate sets exist.

## Sub-branches and critical gates

The outstanding gates define the branch. For every gate, separate **company target dates** (guidance — never Verified) from **regulator-confirmed milestones** (docket entries, decisions, issued permits or certificates). A company filing that reports a regulator action is Verified as a disclosure; reading the regulator's own record gives the claim regulator-confirmed authority.

| Sub-branch | Critical gates (in order) | Next value-defining catalyst (default) | Regulator-confirmed evidence |
|---|---|---|---|
| **Advanced nuclear / SMR** | Design/topical approvals → construction authorization (NRC CP or COL, or DOE authorization) → binding fuel supply (HALEU, recycled, or government material) → construction complete → operating authorization / startup → first criticality → commercial operation | First-unit operating authorization plus first power, whichever is later | NRC docket and ADAMS records, NRC review schedules, DOE approvals (NSDA, PDSA, DSA, startup authorization) |
| **eVTOL / new aviation** | Certification basis (G-1) → means of compliance (G-2) → for-credit flight testing (TIA) → type certificate → production certificate → operating certificate (Part 135 or foreign equivalent) | Type certificate | FAA/EASA/CAAC publications, issued certificates |
| **Space / launch** | First successful orbital flight → repeat success / cadence → FAA launch license (Part 450) → reuse demonstration (if in the model) → binding manifest | Second consecutive successful flight of the commercial vehicle | FAA licenses, mission records, contract awards |
| **Mining developers / explorers** | Resource → reserve (S-K 1300 / NI 43-101) → PEA → PFS → DFS → key permits (EIS/ROD, water, mining lease) → binding offtake → project financing closed → construction decision | Project financing closed (DFS + permits in hand) | Technical report summaries, permit decisions, financing close notices |
| **Deep tech / pre-revenue hardware** | Pilot → paid pilot → binding commercial contract → manufacturing scale (yield, unit cost) | First binding volume contract at disclosed unit economics | Peer-reviewed results, third-party benchmarks, binding contracts |
| **Pre-commercial clean energy tech** | Demo plant → first commercial plant FID → financing closed (conditional loan commitments ≠ closed loans) → commercial operation | First commercial plant at nameplate | Financing close notices, permits, offtake contracts |

A different catalyst may be used when the review shows it moves more EV; state why.

## Runway

**Branch 2 method, restated (adaptations in brackets):** Liquidity = unrestricted cash + equivalents + liquid marketable securities (exclude restricted/pledged cash and uncommitted facilities; count an undrawn credit line only if committed, covenant-available, and economically usable). Normalized cash burn = cash operating loss + capex + capitalized [development/manufacturing] spend classified as investing + contractual milestone/development payments due under the current plan − recurring non-dilutive cash receipts. Exclude marketable-securities purchases and maturities, financing flows, and acquisitions unless part of the forward plan. Base runway = liquidity ÷ normalized trailing monthly burn. Forward runway = liquidity ÷ expected monthly burn under the disclosed [operating and construction] plan. Show base runway, forward runway, the next value-defining catalyst, expected liquidity at that catalyst, a ≥6-month delay sensitivity, post-catalyst buffer, likely financing requirement, and dilution sensitivity. Runway > 24 months is not automatically Positive if it does not fund the next value-defining milestone. [Branch 2's rNPV rule, generalized:] do not double-count the same risk (e.g., a delay case plus a discount-rate premium for the same delay).

**Overlay-specific clarifications:**
- **Interest income** on the liquidity being measured is NOT a recurring non-dilutive receipt — it shrinks as the cash is spent. Base case excludes it; show the with-interest figure as a sensitivity.
- **Post-catalyst buffer** (Branch 2 does not size it): ≥ 12 months of forward burn remaining after the catalyst in the ≥6-month delay case — consistent with Core's "<12-month runway" Severe example.
- **Forward plan shorter than the path to the catalyst:** compute forward runway on the disclosed horizon, then run two extrapolations to the catalyst — *flat* (last disclosed annual rate) and *step-up* (2× the disclosed rate from the next fiscal year, or the company's own disclosed project budget if larger). Label both Estimated. If no forward plan at all is disclosed, report **"forward runway not reliably estimable"** — an evidence limitation (Needs verification / Not disclosed), not a demonstrated shortfall.
- **Open equity programs** (ATM, shelf) are not liquidity until sold. Sales disclosed after the balance-sheet date (8-K, prospectus) may be added as Calculated pro forma; later undisclosed sales are Needs verification.

## Dilution

Use period-end shares outstanding: YoY, and since the first post-listing quarter-end. Split the change by source: financing/ATM, acquisitions, warrant exercises, convertibles, SBC (options and RSUs). Assess:
- **Persistence** — consecutive post-listing years above 15%, and open programs (state unused capacity ÷ shares at the current price as the forward overhang).
- **Economic impact** — average issue price vs book value per share before the raise, and whether runway already funded the catalyst (opportunistic raise) or the raise was forced (runway short, discount, warrants attached).

## Contract evidence hierarchy

Binding with take-or-pay or prepayment > binding with conditions > non-binding MOU / LOI / framework > announced "pipeline". Non-binding agreements never count as backlog and can never alone make the commercialization pillar Positive. A binding agreement whose amounts and conditions are not disclosed sits in "binding with conditions". Calling non-binding agreements an "order book" is a disclosure-quality point (Minor flag), not evidence.

## Pillars and thresholds

Numeric thresholds are defaults; any deviation requires a written reason.

| Pillar | Weight | Positive | Watch | Negative |
|---|---|---|---|---|
| **Cash runway, financing & dilution** | 25% | See sub-ratings | See sub-ratings | See sub-ratings |
| — *Liquidity sub-rating* | | Catalyst funded in the delay case with the buffer under BOTH flat and step-up extrapolations | Funded with buffer under flat only; or forward runway not reliably estimable while base runway ≥ 24 months | Not funded in the flat delay case (Severe candidate) |
| — *Dilution sub-rating* | | Period-end share growth ≤ 10% YoY | 10–30% YoY; or above 30% in one year when raised opportunistically at ≥ 2× prior book value per share | > 30% YoY when forced or below 2× book; or > 15% a year for 3+ consecutive post-listing years |
| **Critical gate progress** | 20% | Final construction and operating authorizations for the first unit in hand or regulator-scheduled; first-unit fuel/inputs binding; project funding committed | First-unit pathway active with ≥ 1 critical gate outstanding and no regulator-published date | Rejection, a gate stalled > 12 months, or no credible pathway |
| **Technical validation evidence** | 15% | Representative prototype of the commercial design operated at commercial conditions, or regulator-accepted performance data | Subscale, component, or test-unit validation; design based on operated predecessor technology | Failed demonstration or no physical validation |
| **Path to commercialization** | 15% | Binding take-or-pay or prepayment (cash received or amounts committed) covering the first units | Binding-with-conditions agreements | Non-binding agreements only |
| **Market opportunity & competition** | 10% | Third-party-evidenced demand and a verified lead over credible peers on gates or cost | Real demand, peers level or ahead, or peer gate table not yet built | Demand weakening or peers decisively ahead |
| **Valuation vs expectations** | 10% | Per Core: proven EV ≥ 50% and required inputs within achieved/peer evidence | Per Core cap: residual EV > 50%; or Needs verification | Scenario analysis shows success-case value after financing and dilution below current EV |
| **Management execution** | 5% | No slip > 1 quarter on the last 3+ guided milestones | One slip ≤ 12 months, or a disclosed pathway change | ≥ 2 slips > 6 months within 24 months, or one slip > 12 months |

**Runway pillar combination (Overlay-specific):** both sub-ratings equal → that rating; they differ by one level → the lower one; liquidity Positive with dilution Negative → Watch; **liquidity Negative → pillar Negative regardless of dilution** (a funding gap cannot be offset).

**Commercialization cap:** undisclosed unit economics (price, capex per unit, operating cost) cap this pillar at Watch; they do not by themselves make it Negative.

**Slip measurement:** compare the end of the earliest dated guided range in a filing with the end of the current range ("late 2027 or early 2028" → "2028" is end-Q1 2028 → end-Q4 2028 = three quarters). A switch of regulatory pathway is recorded as an event and counts as a slip only for the delay it causes.

**No double penalties:** assign each weakness primarily to one pillar. Related effects may be discussed elsewhere, but do not penalize the same underlying issue in multiple pillars without identifying distinct consequences. The runway pillar assesses corporate liquidity and dilution; the critical-gate pillar assesses project-financing readiness and current gate status; slip history belongs to management execution only. Moderate and Minor flags never move the score (Core's override uses Severe flags only), so a flag that mirrors a pillar weakness is not a second penalty.

**Missing-evidence scoring (Overlay-specific; Core has no general rule):** a pillar whose decisive evidence is Needs verification or Not disclosed scores Watch at most — never Positive, and Negative only when the available evidence is itself negative. (Consistent with the 2026-09-22 decision that a Needs-verification valuation pillar scores Watch at most.) If pillars carrying ≥ 40% of the weight rest on Needs verification, the conclusion is **insufficient data**.

## Valuation

Use Core's proven vs unproven EV split and expectations module. Always show market cap, cash, debt, restricted cash, and the share-count basis (basic vs fully diluted, treasury method for options). For a company with immaterial revenue the residual is usually close to 100% of EV, so Core's cap holds the pillar at Watch and the conclusion must state the residual share. If unit economics are not disclosed, the expectations test cannot be built honestly and valuation is **Needs verification** (Core). Scenario valuation (a follow-up action) must state, for each case, the success outcome, timing, financing need, and dilution. Never present a single "implied success probability" without those assumptions.

## Red flags (plug into Core's override rule)

**Severe** — supported calculations or disclosures demonstrate that forward runway does not reach the next value-defining catalyst with the buffer above · going-concern language · regulatory rejection or a materially longer pathway without funding · loss of a critical input with no alternative. Core's "<12-month runway" example and the catalyst-funding test describe the same underlying risk: count one flag, not two.
**Moderate** — repeated slipping of guided timelines · heavy reliance on non-binding agreements · persistent financing dilution well above development-stage peers (peer data required; otherwise Needs verification) · single-site / single-design concentration.
**Minor** — unquantified promotional disclosures · frequent management turnover.

## When binary outcomes "dominate" (Overlay-specific)

Core assigns **high-risk, special situation** when "binary outcomes dominate". Every development-stage company has binary gates, so the overlay applies a test: a verified Severe flag, OR a single gate expected within 12 months decides more than half of EV AND the liquidity sub-rating is Negative or Watch-on-flat-only for the failure/delay case. Otherwise use the score bands and name the gates in the thesis.

## What NOT to use

P/E · EV/EBITDA · P/S on immaterial revenue · dividend metrics · utility allowed-ROE logic · transportation operating ratio · AISC or reserve life before production · management TAM figures as evidence · non-binding agreements as backlog · weighted-average shares as the dilution measure.

## Default first-pass dashboard

Six cards: 1. Weighted score (with cap status) · 2. Liquidity and runway (base, forward, catalyst-delay buffer) · 3. Dilution (YoY by source, overhang) · 4. Gate status (completed vs outstanding, regulator-confirmed vs target) · 5. Contract tier (best agreement in the hierarchy) · 6. Valuation (EV, residual share, test status). Each card: value · rating · provenance label · one-line explanation.

## Follow-up actions

Offer: 1. Runway & dilution deep dive · 2. Critical-gate timeline map · 3. Contract quality audit · 4. Scenario valuation · 5. Compare vs development-stage peers · 6. Full research memo. Score changes follow the nine-item score-change audit trail used in every strict packet.

## Verification checklist

1. As-of date stated. 2. Materiality test shown: numerator lines with core/non-core reasons, denominator reconciliation, TTM period, route. 3. Sub-branch, catalyst, and gates listed; company targets separated from regulator-confirmed milestones. 4. Liquidity, burn (ex- and with interest), base and forward runway, flat and step-up cases, delay buffer — formulas and inputs shown. 5. Dilution by source, persistence, issue price vs book, overhang. 6. Every agreement placed in the hierarchy. 7. Valuation inputs with share-count basis and residual share. 8. Each figure carries a Core provenance label; calculations show formula and inputs; guidance and assumptions are never labeled Verified. 9. Red flags graded before applying Core's cap; no flag counted twice. 10. Conclusion in Core's five categories with data confidence, the binary-outcome test result, and what would break the thesis.

*This is general information only and not financial advice. For personal guidance, please talk to a licensed professional.*
