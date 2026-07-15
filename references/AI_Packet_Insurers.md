# AI Stock Review Packet: Insurers

**Version 2.2.3 — Last updated 2026-07-13.** v2.2.3 corrections: capital jurisdiction router (no cross-framework threshold translation), RBC ACL/CAL basis rule, GAAP vs statutory combined-ratio separation, written/earned lag softened, favorable-development nuance (emergence ≠ current underwriting), four-view book-value rule replacing universal ex-AOCI, "Estimated insurance-float proxy" labeling, life economic-model routing, reinsurance scoring weights, impact-based rating-downgrade severity. Supersedes v2.1: upgraded from a general sector guide to a strict execution file (v4 verification and provenance standard, combined-ratio and premium disambiguation, reserve-quality rules, capital disambiguation, book-value rules, float and investment rules, subsector adjustments including life/reinsurance/broker overrides, scoring and audit-trail rules, five-category conclusion). Educational framework — not investment advice. No buy/sell/hold language.

*Property & casualty, life & annuities, reinsurance, insurance brokers, specialty lines* — GICS: Financials (Insurance). Health insurers (medical-loss-ratio businesses) route to the Health Services packet.

**Core principle: reserves are estimates, so insurer earnings are opinions.** Current-year profit can be manufactured by releasing yesterday's reserves or under-providing for today's claims — the truth surfaces years later. And premium growth is not strength: growing fast in a soft market usually means underpricing risk. A verified combined ratio of 97% is still Watch. Verified does not mean Positive.

## Prompt

> Analyze [company name / ticker] using the uploaded Core Framework and this Insurers guide.
> Do not use buy/sell/hold language.
> Provide: 1. Business model summary · 2. Sector and subsector classification · 3. Peer group with rationale · 4. Key insurance metrics with provenance labels · 5. Values vs peers and 5-year history · 6. Positive/Watch/Negative assessment · 7. Severe red flags, if any · 8. Valuation (P/B vs ROE; subsector-appropriate) · 9. Data confidence: High/Medium/Low · 10. Neutral research conclusion: strong on current evidence / mixed, needs more evidence / weak on current evidence / high-risk, special situation / insufficient data.
> Use primary sources (10-K, 10-Q, 20-F, 6-K, statutory filings, Solvency II SFCR, annual reports, earnings releases). Do not rely only on screeners or summaries.

## Key metrics & rule-of-thumb ranges (P&C base — see subsector overrides)

| Metric | Positive | Watch | Negative | How to read it |
|---|---|---|---|---|
| **Combined ratio** | < 95% | 95–100% | > 100% | Below 100% = underwriting profit before investment income. State the basis — see disambiguation |
| **Accident-year combined ratio ex-cat** | Better than peers, stable | Middling | Deteriorating | The cleanest underwriting read — strips reserve releases and cat noise |
| **Prior-year development (PYD)** | Consistently favorable | Neutral / mixed | Adverse | Adverse = past business was underpriced. See reserve rules |
| **Operating ROE** | > 12% | 8–12% | < 8% | Read with P/B and cost of equity, as with banks |
| **BVPS growth (+ dividends)** | > 8%/yr | 4–8% | < 4% | The long-run compounding engine; use ex-AOCI basis — see book-value rules |
| **Capital adequacy** | Well above own framework's intervention level and management target, stable | Adequate but declining, or basis unresolved | Near intervention levels or falling fast | Framework- and basis-specific — see capital router and scoring |
| **Investment yield & quality** | Rising without reaching | Stable | Stretching into credit/illiquidity | Chasing yield with credit, duration, or alt-asset risk is the classic pre-loss behavior |
| **Premium growth (NPW)** | Rate-driven, in hard market | Market-level | Far above market in soft pricing | Growth ≠ strength — see reserve rules |
| **Net share dilution / yr** | < 2% (or shrinking) | 2–4% | > 4% | Period-end shares outstanding (split-adjusted); buybacks below fair value compound BVPS |
| **P/B with ROE** | See valuation rules | — | — | Never rate P/B in isolation |

**Formulas:** Combined ratio = loss ratio + expense ratio. Loss ratio = incurred losses ÷ net earned premiums. Expense ratio = underwriting expenses ÷ net earned premiums (or net written — state which). Estimated insurance-float proxy ≈ loss reserves + unearned premiums − premiums receivable (a simplification — see float rules; always labeled Estimated proxy with components listed). BVPS growth = (ending BVPS + dividends per share) ÷ beginning BVPS − 1, on the equity basis chosen per the book-value rules. Operating ROE = operating income ÷ average common equity ex-AOCI (with GAAP shown alongside). RBC ratio = total adjusted capital ÷ RBC capital at a STATED basis — ACL (authorized control level) or CAL (company action level = 2 × ACL); never quote an RBC ratio without its basis. Solvency II ratio = eligible own funds ÷ solvency capital requirement (EU). Investment leverage = investments ÷ equity. Net dilution = change in period-end common shares outstanding (split-adjusted) ÷ prior-year count.

## Insurance metric verification standard

An insurance metric is not "verified" unless the output includes all seven evidence items:

1. Metric name
2. Exact value
3. Source document
4. Exact table, note, or section
5. Short quote showing the metric label next to the value
6. Definition match to this Insurers guide (or the company definition, stated)
7. Score impact

Rules: search summaries, aggregator snippets, and unlabeled extracted numbers cannot verify insurance metrics. Do not treat a number as verified because a search result or third-party summary claims it came from a filing. Never reuse a percentage from a nearby table unless the label exactly matches the intended metric. If the label is not visible next to the value, the metric is not verified. If the metric cannot be verified, mark it "Needs verification."

**Known traps:** insurance disclosures are dense with similar percentages — loss ratio, expense ratio, combined ratio, RBC ratio, Solvency II ratio, and investment yield can all appear on one page; the label controls the meaning. A "combined ratio" without a stated basis (calendar vs accident year, with or without catastrophes and development, gross vs net of reinsurance) is not yet a usable number. "Premiums" without written/earned and gross/net qualifiers is not yet a usable number.

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

**Guidance is not achievement:** guidance, targets, and management plans can support a Watch or directional comment, but they should not receive full Positive credit unless supported by achieved results, binding regulatory approval, or directly verified realized performance. This applies especially to: utilities rate-base growth guidance · REIT rent ramp / stabilized rent targets · energy production or capex targets · SaaS margin expansion targets · bank medium-term ROE targets · insurer combined-ratio and ROE targets.

## Combined-ratio & premium disambiguation

Never mix these bases — state which one every figure uses:

| Term | What it is |
|---|---|
| Calendar-year combined ratio | This period's booked losses ÷ premiums — INCLUDES prior-year reserve development, so releases flatter it |
| Accident-year combined ratio | Losses assigned to this year's business only — the honest read on current pricing |
| Accident-year ex-cat | Also strips catastrophe losses — the cleanest underlying trend |
| Loss ratio / expense ratio | The two components; check whether expense ratio uses earned or written premiums |
| GWP / NWP | Gross vs net written premiums — before/after reinsurance ceded; sales activity |
| GEP / NEP | Gross vs net earned premiums — the revenue actually recognized; the ratio denominator |
| GAAP combined ratio | Both components ÷ net EARNED premiums |
| Statutory ("trade") combined ratio | Loss ratio on net earned + expense ratio on net WRITTEN (+ policyholder dividends where applicable) — a statutory 94% and a GAAP 94% are not automatically the same evidence |

Rules: every combined ratio states its full construction — GAAP or statutory · gross or net · calendar or accident year · catastrophes in or out · PYD in or out · policyholder dividends in or out · reinstatement premiums in or out · company-reported or packet-calculated. Do not compare GAAP and statutory ratios without reconciliation. A calendar-year combined ratio below 95% built on large reserve releases is NOT Positive underwriting evidence — rate the accident-year figure. Gross vs net matters: heavy reinsurance purchase can mask gross underwriting problems (and creates counterparty risk). Written premiums are recorded before they are fully earned; the lag depends on policy duration, inception distribution, and risk pattern — reconcile written-premium growth to earned-premium growth rather than assuming a fixed one-year lag. If only a calendar-year figure is disclosed, show it with its PYD component separated; if PYD is not separable, the underwriting pillar caps at Watch.

## Reserve-quality rules

Reserves are the biggest number on the balance sheet and the least knowable. Measure: one-year development as % of beginning reserves · 3- and 5-year cumulative development · development by line and accident year (loss triangles / Schedule P) · development as % of pretax operating income · IBNR % and trend · paid vs incurred triangle consistency · methodology, discounting, or assumption changes · loss-portfolio transfers, adverse-development covers, commutations (these transfer or mask development) · reinsurance recoverables and counterparty quality.

Scoring: **Positive** — consistently favorable, broad-based PYD that is modest relative to reserves and earnings · **Watch** — neutral/mixed development, favorable development concentrated in one line or driven by methodology change, or releases large relative to earnings · **Negative** — adverse development, especially repeated or accelerating. Favorable development is a revision of *prior-period* estimates: it may reflect genuine favorable emergence or conservative reserving, but it is NOT evidence of current accident-year underwriting quality, and it can itself be a smoothing device.

**Rule: rapid premium growth can hide underpricing** (new business hasn't developed; reserves on it are guesses; soft-market growth is bought with price). If NPW growth is far above market — roughly > 15%/yr in a soft market — require pricing/rate evidence and accident-year ratios before rating underwriting Positive. This is the insurance twin of the Banks rapid-loan-growth rule.

**Rule: favorable development is a prior-estimate revision, not current earnings power.** Quantify what % of pre-tax income came from favorable development; when it contributes materially (roughly >25%) for consecutive years, flag earnings quality and rate profitability on the accident-year basis — even if reserve adequacy itself still rates Positive.

## Capital disambiguation & scoring

Six different things — never substitute one for another:

| Term | What it is |
|---|---|
| RBC ratio (US) | Total adjusted capital ÷ authorized control level — statutory, regulator-defined |
| Solvency II ratio (EU/UK) | Eligible own funds ÷ SCR — from the SFCR |
| Statutory surplus | Dollar capital in the regulated entities — not a ratio |
| Rating-agency capital | S&P/AM Best model capital — drives ratings, not regulation |
| GAAP/IFRS shareholders' equity | Accounting book value — moves with AOCI; not regulatory capital |
| Holding-company liquidity | Cash at the holdco — dividends from subsidiaries are regulator-gated |

**Jurisdiction router — identify the framework before applying any threshold.** Frameworks in use: US RBC · EU Solvency II · UK Solvency UK · Bermuda BSCR/ECR · Canada LICAT/MCT/MICAT · Swiss SST · Australia PCA/LAGIC · Lloyd's member/central capital · IAIS ICS (internationally active groups). These use different valuation bases, risk measures, and intervention levels — **never translate a ratio from one framework into another's thresholds.** For every capital ratio report: framework and ratio name · numerator/denominator basis · solo entity or consolidated group · regulatory intervention level · management target · trend. Rate the ratio against its OWN framework's intervention level, the management target, the trend, and framework peers; fixed numeric thresholds are preliminary heuristics only.

**US RBC basis rule:** RBC is quoted on two conventions that differ by 2x — TAC ÷ ACL (authorized control level) or TAC ÷ CAL (company action level = 2 × ACL). A "400%" ratio means opposite things on the two bases. Never rate an RBC figure until the basis is identified; state both the quoted ratio and its ACL-equivalent. As ACL-basis heuristics only: **Positive** > 400%, stable · **Watch** 250–400% or declining materially · **Negative** approaching intervention levels. Solvency II heuristics: **Positive** > 180% and above management target · **Watch** 130–180% or below target · **Negative** approaching 100% SCR (note transitional measures and internal-model effects).

Rules: RBC ≠ Solvency II ≠ GAAP equity. "Comfortably capitalized" is not a disclosed ratio. A financial-strength rating (A, A+) supports context but is not a capital ratio. Holdco/opco structure matters: statutory entities pay dividends up only with regulatory headroom — holdco debt service depends on it. If no ratio is disclosed (common for US subsidiaries of groups): "Capital ratio not directly disclosed / needs verification." Verified does not mean Positive — a verified SII of 155% is Watch.

## Book value & ROE rules — the AOCI trap

GAAP equity swings with unrealized bond marks in AOCI: rising rates crush reported book value and falling rates inflate it, often without changing ultimate cash flows *when assets can be held to maturity* — but unrealized losses become economically real under surrender or liquidity stress, so never dismiss them outright. Rules: report four equity views where relevant — GAAP/IFRS common equity · common equity ex-AOCI · tangible common equity · company-disclosed adjusted/economic equity — and choose the valuation basis that best fits the economics, stating why. For P&C insurers ex-AOCI operating ROE is usually the right primary basis; for life insurers, removing AOCI can strip a legitimate asset-liability offset (LDTI and IFRS 17 place liability discount-rate effects in OCI), so check duration matching, hedge assets, and surrender-stress liquidity before preferring any single view. A P/B that looks cheap only because AOCI destroyed the denominator is not cheap; a life insurer that looks fine ex-AOCI but faces surrender risk against underwater bonds is not fine. BVPS growth + dividends over 5 years is the compounding engine — for life insurers, cross-check against embedded-value or CSM growth where disclosed. Buyback quality: repurchases below fair/book value compound BVPS; buybacks funded by weakening capital ratios do not earn Positive.

## Float & investment rules

Float = policyholder money held before claims are paid — the second profit engine. Float is not a standardized accounting measure: any calculation is labeled **"Estimated insurance-float proxy"** with included/excluded components listed (loss reserves, unearned premiums, premiums receivable; where material also reinsurance recoverables, funds withheld, DAC, policyholder account balances). Do not compare float leverage across accounting regimes (IFRS 17 vs US GAAP/statutory) without reconciliation. Assess: investment leverage (investments ÷ equity — amplifies both yield and losses) · asset quality mix (govvies/IG credit vs high-yield, CRE, alts, affiliated assets) · duration vs liability profile (life insurers: disintermediation risk if rates spike and surrenders rise) · unrealized loss positions vs equity · new-money yield vs portfolio yield. **Reaching for yield is the classic pre-loss behavior:** a rising yield achieved through credit descent, illiquidity, or affiliated/related-party assets rates Negative even while reported income improves. Alt-heavy or affiliated-asset-heavy portfolios (private credit, sidecars) get a transparency caveat and generally cap the investment pillar at Watch unless look-through disclosure is strong.

## Subsector adjustments

**P&C — personal lines** (auto/home): frequency/severity trends, rate adequacy vs loss-cost inflation, cat exposure (state the modeled cat load), direct vs agency distribution economics.

**P&C — commercial & specialty**: pricing-cycle position (hard vs soft market — state it, with rate-change evidence), reservation of long-tail lines (casualty, D&O, workers' comp — where under-reserving hides longest), E&S growth quality.

**Reinsurance** — its own scoring model, not a P&C adjustment. Add: gross and net PML (probable maximum loss — 1-in-100 and 1-in-250 event loss as % of capital) · cat budget vs actual over multiple years · rate-on-line changes · retrocession purchased and reinstatement premiums · attachment points/limits drift · third-party capital and sidecars · recoverable concentration and collateral/trust arrangements · casualty-tail reserve development · exposure growth vs premium growth. Combined ratios are volatile by design — judge across a full cat cycle; a benign-cat-year 85% is not repeatable evidence. Recoverables are counterparty-credit exposures: collateral, disputes, and recoverability matter independently of the counterparty's headline rating. *Weights override:* underwriting & pricing-cycle position 20% · catastrophe & aggregate exposure 20% · capital & liquidity 20% · reserve & retrocession quality 15% · investments & third-party capital 10% · valuation 15%.

**Life & annuities** — override the P&C table: combined ratio does not apply. Route again by economic model before choosing emphasis: fixed/indexed annuities (spread, surrender behavior, hedging) · variable annuities (fees, guarantees, hedge effectiveness, market risk) · protection life (mortality, lapse, assumption changes) · group benefits (incidence, recovery, pricing) · runoff/long-term care (reserve adequacy, rate increases, morbidity) · participating/unit-linked IFRS business (CSM, new-business value). Use: new-business value / embedded value (where disclosed, mostly non-US) · CSM balance, new-business CSM, and CSM release under IFRS 17 · spread-based vs fee-based earnings mix · net investment spread and new-money yield vs guaranteed crediting rates · surrender/lapse trends, surrender-charge and MVA protection, liquidity under surrender stress · LDTI annual assumption-review effects (repeated favorable unlocking = earnings-quality flag) · hedge effectiveness · captive/affiliated reinsurance · statutory earnings and subsidiary remittances vs GAAP earnings. *Weights override:* profitability & spread/fee quality 25% · capital adequacy 25% · reserve/assumption quality (assumption reviews, LDTI/IFRS 17 unlocking) 20% · investment quality & ALM 15% · valuation (P/B ex-AOCI vs operating ROE; EV multiple where available) 15%.

**Insurance brokers** (no underwriting risk — fee businesses): normal-company economics apply. Use organic revenue growth, EBITDA/operating margin, FCF conversion, net debt/EBITDA, M&A discipline; value on P/E, EV/EBITDA, FCF yield. *Weights override:* organic growth 25% · margins & FCF 25% · capital allocation/M&A 15% · balance sheet 15% · valuation 20%. The insurance capital, reserve, and float sections do not apply.

**Financial guaranty / title / mortgage insurance:** monoline tail-risk models — judge on exposure-to-capital, vintage quality, and stress losses, not the headline combined ratio.

**Health insurers** (MLR businesses): route to the Health Services packet — medical-loss-ratio economics, not float economics.

**IFRS 17 vs US GAAP:** results are not directly comparable across regimes. Under IFRS 17 note the CSM (contractual service margin — deferred unearned profit) and risk adjustment; under US GAAP life, LDTI assumption unlocking. Cross-regime peer comparisons need a basis caveat.

## Valuation rules

Connect P/B (ex-AOCI) to operating ROE and cost of equity — the Banks logic: high P/B with durably high ROE and clean reserves can be fair; low P/B with weak ROE or dirty reserves is usually deserved. Cross-checks: BVPS + dividend compounding over 5–10 years · P/E only on multi-year normalized earnings (single-year P/E is distorted by cat losses and reserve moves — never headline it) · embedded value or CSM-based multiples for life where disclosed · P/E, EV/EBITDA, FCF yield for brokers. Rules: a "cheap" P/B is at best Watch until reserve quality and capital adequacy are verified — under-reserved book value is fiction. State the pricing-cycle position for P&C/reinsurance valuations; paying peak-multiple for peak-cycle underwriting earns Watch.

## Default first-pass dashboard for insurers

Six cards: 1. Underwriting (combined ratio with basis stated, accident-year trend) · 2. Reserve quality (PYD trend, releases vs earnings) · 3. Profitability & compounding (operating ROE, BVPS + dividends growth) · 4. Capital (RBC / Solvency II with trend, holdco liquidity) · 5. Float & investments (yield, quality, leverage, AOCI position) · 6. Valuation (P/B ex-AOCI vs operating ROE vs peers).

Each card shows: value · Positive/Watch/Negative rating · provenance label (per the v4 standard) · one-line explanation. Use concise tables, not long paragraphs.

The first-pass score is always provisional unless: the combined-ratio basis is resolved, reserve development verified from filings, a capital ratio verified or explicitly Not disclosed, and at least partial peer comparison performed.

## Follow-up actions

Offer: 1. Verify reserve development (loss triangles) · 2. Verify capital ratio (statutory/SFCR) · 3. Deep dive: underwriting by segment and accident year · 4. Deep dive: investment portfolio and AOCI · 5. Deep dive: valuation vs ROE and peers · 6. Deep dive: life assumptions/CSM (life only) · 7. Compare vs subsector peers · 8. Deep dive: pricing-cycle position and rate adequacy.

Priority logic: PYD adverse or unlabeled → 1. Capital ratio missing or declining → 2. Calendar/accident-year gap large → 3. Yield rising while quality falls, or big AOCI swing → 4. P/B far from peers either way → 5. Premium growth far above market → 8.

## Score-change audit trail

Whenever a follow-up action changes the score, show all nine items: 1. previous score · 2. updated score · 3. metric that changed · 4. old status · 5. new verified value · 6. source document · 7. exact quote showing label and value · 8. pillar affected · 9. reason for the change.

Rules: if the exact quote cannot be provided, do not change the score — keep the metric at Needs verification. A score changes only when the newly verified metric changes a pillar's Positive/Watch/Negative rating; verification alone does not automatically change the score.

## Data confidence rules

**High:** recent 10-K/10-Q/20-F/6-K, statutory filings, or Solvency II SFCR with the exact table label and value quoted — covers combined-ratio components, loss triangles, RBC/SII, investment schedules. **Medium:** earnings release or investor presentation with a labeled table (accident-year and ex-cat splits often live only here); rating-agency reports cross-checked against filings. **Low:** aggregator-only data, unlabeled ratios, estimated development, single-source rate commentary.

Rules: price and P/B from aggregators may be used as Estimated. Capital ratios are never High confidence unless the filing or regulator source clearly labels the ratio. If a key metric is Low confidence, state how it affects the pillar score.

## What NOT to use

EV/EBITDA, gross margin, operating margin, net debt/EBITDA (holdco leverage is judged differently), and FCF metrics — meaningless or misleading for underwriters (brokers excepted). Premium growth as a headline positive. Single-year P/E or net income (cat losses and reserve moves make them lumpy). Calendar-year combined ratios without the development component. GAAP book value without the AOCI check.

## Common mistakes to avoid

Treating premium growth as strength · rating a release-flattered calendar-year combined ratio as underwriting skill · ignoring adverse development because "it's one-time" (it rarely is) · using GAAP book value through an AOCI swing · confusing RBC with Solvency II or either with rating-agency capital · treating a compliance statement as a capital ratio · ignoring holdco/opco dividend gating · applying P&C metrics to a life insurer or any underwriting metric to a broker · comparing IFRS 17 results directly with US GAAP · calling low P/B "cheap" before reserve verification · extrapolating a benign-cat reinsurance year · upgrading a pillar because a metric was found while it is still in Watch range.

## Red flags

**Severe** — repeated or accelerating adverse reserve development · capital near its framework's intervention levels after losses, or a capital raise forced by losses · a rating downgrade (candidate flag — distinguish financial-strength vs issuer/holdco ratings; Severe only when reasonably likely to cause material lost business, cedent/broker restrictions, collateral requirements, termination rights, or financing distress) · going-concern language, covenant pressure, or blocked subsidiary dividends · evidence of under-reserving to manage earnings · large affiliated-asset or related-party investment exposure without look-through disclosure.

**Moderate** — combined ratio persistently above 100% with no pricing response · reserve releases funding a large share of earnings for consecutive years · reaching for yield (credit descent, illiquidity, duration bets) · premium growth far above market in soft pricing · concentrated cat exposure vs capital · surrender/lapse trend deterioration (life) · assumption unlocking that repeatedly boosts earnings (life) · heavy reliance on reinsurance with weak counterparties.

**Minor** — single-year cat losses within the stated cat budget · modest AOCI swings from rate moves · one soft quarter in a long-tail line · FX translation noise.

## Scoring weights (P&C base; life, reinsurance, and broker overrides in subsector section)

| Pillar | Weight |
|---|---|
| Underwriting (combined ratio, reserves) | 30% |
| ROE & book value growth | 25% |
| Capital adequacy | 20% |
| Investment results & quality | 10% |
| Valuation (P/B vs ROE) | 15% |

Sub-score note: the underwriting pillar weighs accident-year ratio quality 50% · reserve development 35% · growth quality (rate vs volume) 15%. If reserve development cannot be verified, the underwriting pillar cannot score above Watch.

Rate each pillar vs peers and own history: Positive = 2, Watch = 1, Negative = 0. Pillar contribution = pillar weight × rating ÷ 2 (weights total 100%; e.g., 30% × 2 ÷ 2 = 30 points); score = sum of contributions, 0–100%. ~75%+ strong on current evidence; 50–75% mixed; <50% with sufficient evidence and no verified Severe flag = weak on current evidence. Any verified Severe flag caps the score at 50% — always show the uncapped score, the cap applied, and the displayed score. A flag activates the cap only when its evidence is Verified or Calculated — verified inputs; a flag resting on user excerpts or relayed values stays a provisional warning. Two or more verified Severe flags usually mean high-risk / special situation. The score is a research organizer, not a prediction engine.

## Conclusion template

End with exactly one of: **strong on current evidence** / **mixed, needs more evidence** (name the evidence) / **weak on current evidence** (score <50% with sufficient evidence and no verified Severe flag) / **high-risk, special situation** / **insufficient data** — plus data confidence (High/Medium/Low), the subsector used, and a two-sentence thesis including what would break it. No buy/sell/hold language.

## Final sector checklist

1. Sector confirmed: most operating profit fits Insurance; health insurers routed to Health Services; brokers identified as fee businesses.
2. Subsector identified: personal P&C, commercial/specialty P&C, reinsurance, life & annuities, broker, monoline.
3. Peer group built within the subsector and accounting regime (IFRS 17 vs US GAAP caveat).
4. Combined-ratio basis resolved: calendar vs accident year, cat and PYD components separated, gross vs net stated.
5. Premium terms disambiguated: GWP/NWP/GEP/NEP kept separate; growth judged with pricing-cycle context.
6. Reserve development verified from loss triangles or development disclosures; releases vs earnings quantified.
7. Capital metrics disambiguated: RBC, Solvency II, statutory surplus, rating capital, GAAP equity, holdco liquidity kept separate.
8. Book value and ROE computed ex-AOCI with GAAP shown alongside.
9. Float and investment quality reviewed: leverage, credit quality, duration/ALM, affiliated assets.
10. Subsector overrides applied (life/broker weights; reinsurance cycle judgment).
11. "What NOT to use" respected; quality-of-earnings and geography/currency checks run (Core Framework).
12. Red flags graded with provenance labels and verified before applying the Severe cap.
13. Valuation done with P/B ex-AOCI vs operating ROE vs cost of equity, plus subsector-appropriate cross-checks.
14. Weighted score computed with sub-score rules; weakest pillar identified; uncapped and capped scores shown when a cap applies.
15. Score-change audit trail shown if any follow-up action changed the score; neutral research conclusion written with data confidence, subsector, and unresolved gaps.

*This is general information only and not financial advice. For personal guidance, please talk to a licensed professional.*
