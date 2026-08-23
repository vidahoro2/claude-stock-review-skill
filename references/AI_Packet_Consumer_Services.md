# AI Stock Review Packet: Consumer Services

**Version 2.2.3 — Last updated 2026-08-23.** v2.2.3 adds the expectations-embedded valuation module: the universal expectations test (reverse-solve the price for required growth, margin, reinvestment and discount rate), the proven-vs-unproven enterprise-value split with its valuation-pillar caps, and the "Estimated — expectations-implied" sub-label. v2.2.2 adds the weak-on-current-evidence conclusion category. v2.2.1 adds the v4 provenance-label table (Calculated — verified inputs, Not disclosed; Severe-flag caps require verified evidence). Supersedes v2.1: adds subsector routing (restaurants, hotels/lodging, leisure/theme parks, cruise lines, gaming/casinos/betting, education services), subsector-specific metrics, red flags, scoring weights and valuation methods, shared rules, and mixed-business handling. Educational framework — not investment advice. No buy/sell/hold language.

*Restaurants, hotels/lodging, leisure/theme parks, cruise lines, gaming/casinos/betting, education services, and other experience/discretionary service businesses* — GICS: Consumer Discretionary (Consumer Services). Media/streaming usually belongs in **Communication Services** — see the relocation note below.

**Core principle: classify the subsector first.** Consumer Services businesses share discretionary-spending exposure but have very different economics. Applying restaurant metrics to a cruise line, or hotel metrics to a casino, is the most common analytical mistake in this sector.

## Prompt

> Analyze [company name / ticker] using the uploaded Core Framework and this Consumer Services guide.
> Do not use buy/sell/hold language.
> Please provide:
> 1. Business model summary
> 2. Correct sector and subsector classification
> 3. Peer group and why those peers are appropriate
> 4. Key subsector metrics with verification status
> 5. Company values versus peers and 5-year history
> 6. Positive / Watch / Negative assessment
> 7. Severe red flags, if any
> 8. Valuation method appropriate for the subsector
> 9. Data confidence level: High, Medium, or Low
> 10. Neutral research conclusion: strong on current evidence; mixed / needs more evidence; high-risk / special situation; or insufficient data
>
> Use primary sources where possible: 10-Ks, 10-Qs, annual reports, earnings releases, investor presentations, segment tables, KPI tables, and regulatory filings. Do not rely only on screeners or summaries.

## Universal checklist

1. Identify the business model and subsector. For mixed businesses, classify by where most operating profit comes from.
2. Revenue trend over 5 years — growing, flat, shrinking? Organic, acquired, price-driven, capacity-driven, or subscriber-driven?
3. Unit economics — traffic, occupancy, utilization, yield, enrollment, or subscriber quality depending on subsector.
4. Margin level and trend versus direct peers **with the same operating model** (asset-light vs asset-heavy).
5. Free cash flow — positive, growing, converting from profits? For asset-heavy models, check FCF after growth capex.
6. Leverage — net debt/EBITDA, lease-adjusted leverage where leases are material, interest coverage, debt maturities, fixed-cost exposure.
7. Share count over 5 years — dilution or buybacks?
8. Returns — ROIC vs cost of capital where meaningful.
9. Valuation vs own 5-year range AND vs peers, using the right subsector method.
10. Run the subsector red-flag list; grade findings Minor / Moderate / Severe.
11. Ask why the opportunity exists; write the thesis in two sentences.

**Peer group:** 5–10 names sharing business model, geography, growth stage, margin structure, capital intensity, regulation, customer type, cyclicality. A sector label is not a peer group.

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

**Expectations are not results (universal):** a price already contains a forecast, and a review that only compares multiples never states what that forecast is. Run this test whenever the valuation pillar would otherwise rest on a multiple above the company's own 5-year range, or whenever the market or management thesis rests on segments with no achieved results; otherwise record "expectations test not triggered" and move on. Invert the valuation — hold the current price fixed and solve for what it requires: revenue CAGR over a stated horizon, steady-state operating or FCF margin, reinvestment (sales-to-capital or reinvestment rate), the discount rate with its components, and a terminal growth rate no higher than the long-run risk-free rate. Convert the requirement into absolute end-of-horizon revenue and test it three ways: against the company's own achieved 5-year record, against the best verified peer analog at comparable scale, and against the current size of the market being addressed. **TAM × assumed share is not a valuation output — it is the assumption under test.**

**Proven vs unproven enterprise value:** split EV into the part the proven business supports under the sector packet's normal valuation method and the residual the market is paying for optionality. A segment counts as proven only when the company discloses its revenue AND either its operating profit or a company-defined unit economic; anything else is unproven, is valued separately and labeled, and is never blended into the base multiple. Report the residual as a share of total EV. Rules: required inputs that exceed anything the company has achieved — or anything a verified peer has achieved at comparable scale — cap the valuation pillar at Watch unless the review names the specific verified evidence supporting the higher requirement · residual EV above ~50% of total EV caps the valuation pillar at Watch and obliges the conclusion to state the residual share, whatever the operating pillars show · disclosure too thin to build the test (no segment detail, no margin path) makes valuation **Needs verification**, never a favorable default · do not penalize the same optimism twice by both discounting the required growth and inflating the discount rate — pick one and say which.

**Estimated — expectations-implied:** every output of this test carries that label, a sub-type of Estimated. It is never Verified and never High confidence, because the solution depends on assumptions the review itself chose; only the inputs (price, period-end share count, net debt, disclosed segment figures) carry labels of their own. **Avoid:** analyst price targets as evidence of value · forward multiples built on margins the company has never achieved · "cheap versus its own history" when that history sits entirely inside one expansion regime · peer multiples where the peers are themselves priced on expectations.

## Quality of earnings

Profits converting into cash? Over 3–5 years FCF should roughly track net income. FCF consistently and materially below net income? Investigate the gap. 'Adjusted' earnings much higher than GAAP, year after year? Same 'one-time' add-backs recurring every year? Working capital temporarily flattering cash flow? Acquisitions masking weak organic growth? Watch goodwill build. Revenue recognized aggressively? Receivables outgrowing revenue is a warning. Margin gains from real operating leverage — or accounting changes? In this sector also check: capex, content, or ship/attraction investment excluded from the economic story.
Rule: high-quality earnings are recurring, cash-backed, not dependent on repeated adjustments.

## Geography/currency

Where is revenue generated? Where are profits generated (often different)? Where are assets located? Can they be taken or stranded? What currencies are revenue and costs in? Any mismatch? What currency is the debt in? FX debt vs local revenue is the classic blow-up. Politically risky jurisdictions — expropriation, licenses, rule of law? Could tariffs, sanctions, travel restrictions, capital controls, tax changes, or regulation hit the model?

## Subsector classification map

Classify by where most **operating profit** comes from, not revenue. Then use only that subsector's mini-packet.

| Subsector | Use when most profit comes from | First-pass metrics |
|---|---|---|
| Restaurants | Company-owned or franchised foodservice | Same-store sales, traffic vs price/mix, unit growth, restaurant-level margin, franchise mix, lease-adjusted leverage, FCF after growth capex |
| Hotels / lodging | Owned, managed, or franchised hotels; lodging platforms | RevPAR, ADR, occupancy, net rooms growth, owned vs managed/franchised mix, debt/EBITDA, FCF |
| Leisure / theme parks / experiences | Parks, attractions, live experiences, recreation venues | Attendance, per-capita spend, utilization, pass/membership trend, labor pressure, maintenance capex, fixed-cost leverage |
| Cruise lines | Ship-based vacation operations | Occupancy, net yield, passenger cruise days, booking curve, onboard spend, fuel sensitivity, FCF after ship capex |
| Gaming / casinos / betting | Land-based casinos, online betting, iGaming, gaming concessions | GGR/NGR, handle/hold, visitation, promo intensity, digital active users, license risk, debt/EBITDA |
| Education services | Schools, training, test prep, workforce education | Enrollment growth, starts, retention, outcomes, revenue per student, receivables/bad debt, cash conversion |
| Media / subscription | Consumer subscription services only if intentionally reviewed here | See relocation note — usually Communication Services |
| Mixed consumer services | Several material segments with different economics | Segment analysis or sum-of-the-parts |

Hotel REITs follow the REITs packet when real-estate economics dominate. A casino-hotel is Gaming, not Hotels. A fintech-like betting platform is still Gaming.

**Formulas:** RevPAR = ADR × occupancy. ADR = room revenue ÷ rooms sold. System-wide sales = sales across all locations incl. franchised — NOT company revenue. AUV = annual sales ÷ units. Per-capita spend = revenue ÷ attendance. Net yield = net revenue ÷ available passenger cruise days. Cruise occupancy = passenger cruise days ÷ available berth days (can exceed 100% by convention). Hold rate = gaming revenue ÷ handle. Lease-adjusted leverage = (net debt + lease liabilities) ÷ EBITDAR or per company definition. FCF = operating cash flow − capex.

## Restaurants

Company-operated stores carry food, labor, rent, and capex risk; franchise-heavy models report lower revenue but earn higher margins with better cash conversion. Identify the mix first — it drives every comparison.

| Metric | Positive | Watch | Negative | How to read it |
|---|---|---|---|---|
| **Same-store sales / comps** | > 5% | 2–5% | < 2% | Separate traffic from price/mix where disclosed |
| **Traffic / transactions** | Positive | Flat to slightly negative | Sustained decline | Often undisclosed → Needs verification if missing |
| **Price / mix** | Supports margin, traffic stable | Price-led growth | Price masking traffic decline | Price-only growth is fragile |
| **Unit growth** | Consistent net openings with solid new-unit returns (> 5% for growth concepts) | Slowing or acquisition-led | Net closures or weak new-unit returns | Judge mature systems vs own history, not a fixed % |
| **Restaurant-level margin** | Expanding / best-in-class | Flat, cost pressure | Falling materially | Compare only against similar ownership mix |
| **Franchise mix / royalties** | Royalty growth, healthy franchisees | Mixed model | Franchisee distress | System sales are not company revenue |
| **Lease-adjusted leverage** | < 3x | 3–4x | > 4x | Leases are real fixed obligations |
| **FCF after growth capex** | Positive & growing | Break-even | Negative | Expansion should fund itself over time |

**What NOT to use:** revenue growth without separating comps, traffic, price/mix, and unit growth; comparing franchise-heavy and company-owned margins without adjustment; system-wide sales as company revenue.

**Red flags:** **Severe** — traffic declining while price increases hide weak demand; franchisee distress, royalty disputes, or mass closures; negative comps plus high lease-adjusted leverage. **Moderate** — food/labor inflation without pricing power; negative comps for several quarters. **Minor** — one-quarter weather, calendar, or promotion timing issue.

**Weights:** comps & traffic 25% · unit economics & margins 25% · unit growth & franchise quality 20% · balance sheet & leases 15% · valuation 15%.

## Hotels / lodging

Asset-light franchisors and managers earn fees on hotel-level revenue with low capital intensity; owned-hotel operators bear real estate, labor, capex, and occupancy risk. The two models are not margin-comparable.

| Metric | Positive | Watch | Negative | How to read it |
|---|---|---|---|---|
| **RevPAR** | > 5% growth | 0–5% | Negative | Core lodging demand metric |
| **ADR** | Rising, occupancy stable | Price-led only | Falling | Rate power |
| **Occupancy** | > 75% | 65–75% | < 65% | Cyclical and market-specific |
| **Net rooms growth** | > 4% | 1–4% | < 1% or negative | Pipeline quality matters — not all pipeline converts |
| **Fee growth (managed/franchised)** | > 5% | 0–5% | Negative | Higher-quality revenue stream |
| **Owned vs asset-light mix** | Asset-light mix rising | Mixed | Heavy owned exposure into downturn | Drives margins and capital intensity |
| **Debt/EBITDA** | < 3x | 3–4x | > 4x | Most important for owned-heavy models |
| **FCF** | Positive & durable | Thin / capex-heavy | Negative | Check renovation and maintenance capex |

**What NOT to use:** comparing owned-hotel margins with asset-light franchisors; judging from one seasonally strong or weak quarter; treating pipeline rooms as guaranteed growth.

**Red flags:** **Severe** — debt maturity wall during weak RevPAR period; owned-heavy model with falling RevPAR and negative FCF. **Moderate** — occupancy falling while ADR is also cut; corporate or group travel weakness; pipeline cancellations. **Minor** — temporary renovation disruption.

**Weights:** RevPAR/ADR/occupancy 30% · asset-light mix & fee growth 20% · balance sheet 20% · FCF & capex 15% · valuation 15%.

## Leisure / theme parks / experiences

Admissions, passes, memberships, food and beverage, merchandise, lodging, and premium experiences against a high fixed-cost base — attendance and per-capita spend drive operating leverage in both directions.

| Metric | Positive | Watch | Negative | How to read it |
|---|---|---|---|---|
| **Attendance** | > 5% growth | 0–5% | Negative | Separate demand from pricing |
| **Per-capita spending** | Rising, attendance stable | Price-led | Falling, or damaging traffic | Revenue ÷ attendance |
| **Utilization / capacity** | High & stable | Mixed | Low | Capacity limits can cap growth |
| **Pass / membership trend** | Growing quality base | Flat or discount-driven | Declining / churn rising | Often only partially disclosed |
| **Operating margin** | Expanding | Labor/cost pressure | Falling materially | Fixed costs amplify swings |
| **Maintenance capex** | Funded & stable | Rising | Deferred / underfunded | Safety and asset-quality issue |
| **Weather exposure** | Geographically diversified | Seasonal | Highly concentrated | Never annualize a weather quarter |
| **Debt / fixed-cost leverage** | Manageable | Elevated | High with weak demand | Operating leverage cuts both ways |

**What NOT to use:** revenue growth without separating attendance from per-capita spend; ignoring maintenance capex; annualizing a weather-affected quarter.

**Red flags:** **Severe** — attendance decline plus high fixed-cost leverage; underinvestment in safety or maintenance. **Moderate** — per-capita growth driven only by price while attendance falls; labor cost pressure without pricing offset. **Minor** — weather or calendar disruption.

**Weights:** attendance & utilization 25% · per-capita spend & pricing power 20% · margins & labor 20% · maintenance capex & asset quality 15% · balance sheet 10% · valuation 10%.

## Cruise lines

Ticket revenue plus high-margin onboard spending against a capital-intensive base: ships, drydock, fuel, crew, port costs, and heavy debt financing. Capacity additions and leverage dominate the analysis.

| Metric | Positive | Watch | Negative | How to read it |
|---|---|---|---|---|
| **Occupancy** | > 100% (berth convention) | 95–100% | < 95% | Check company definition |
| **Net yield** | > 5% growth | 0–5% | Negative | Key pricing + onboard metric; definitions vary — check reconciliation |
| **Passenger cruise days** | Growing profitably | Capacity-led | Declining | Volume metric |
| **Booking curve** | Strong price and volume | Mixed | Late discounting | Usually qualitative, from earnings calls |
| **Onboard spending** | Growing | Flat | Falling | Higher-margin revenue source |
| **Fuel sensitivity** | Offset by pricing/hedging | Pressure | Margin shock | Check fuel expense and hedging disclosure |
| **Debt/EBITDA** | Improving toward < 4x | Elevated | > 5x or worsening | Subsector structurally debt-heavy |
| **FCF after ship capex** | Positive | Thin | Negative | Include orderbook timing |

**What NOT to use:** peak-cycle P/E without checking leverage, interest burden, and capacity additions; occupancy alone when yield is weak; ignoring ship capex and the orderbook.

**Red flags:** **Severe** — high leverage with negative FCF; new capacity arriving into weak bookings; refinancing pressure during weak demand. **Moderate** — fuel cost spike without pricing offset; discounting needed to fill ships; onboard spend weakening. **Minor** — itinerary or port disruption.

**Weights:** bookings/yield/occupancy 30% · balance sheet & interest burden 25% · FCF after ship capex 20% · cost & fuel sensitivity 10% · valuation 15%.

## Gaming / casinos / betting

Land-based casinos are license- and location-driven; online betting depends on handle, hold, promo intensity, CAC, gaming taxes, and regulation. Always separate land-based and digital economics — they are different businesses.

| Metric | Positive | Watch | Negative | How to read it |
|---|---|---|---|---|
| **GGR / NGR** | > 5% growth | 0–5% | Negative | Definitions vary by market — check which is reported |
| **Handle** | Growing with rational promos | Promo-led | Declining | Betting volume |
| **Hold / win rate** | Near normalized range | Volatile | Spike treated as recurring | Luck-driven short term — normalize |
| **Visitation** | Growing | Flat | Declining | Land-based demand |
| **Revenue per visitor** | Rising | Flat | Falling | Monetization |
| **Promotional intensity** | Stable / falling | Rising | Rising faster than revenue | Quality-of-growth test for digital |
| **Digital active users / CAC** | Growing with improving economics | CAC-heavy | Losses widening | Often inconsistently disclosed → Estimated |
| **Debt/EBITDA** | < 3x | 3–4x | > 4x | Adjust for OpCo/PropCo and lease structures |

**What NOT to use:** short-term hold-rate spikes as sustainable growth; comparing land-based casinos with online platforms without segment separation; ignoring license risk, gaming taxes, and market-access costs.

**Red flags:** **Severe** — license, regulatory, or suitability threat; high debt with declining visitation or gaming revenue; online betting losses widening despite revenue growth. **Moderate** — promo spend rising faster than revenue; VIP or single-jurisdiction concentration; hold-rate benefit mistaken for recurring growth. **Minor** — unlucky hold-rate quarter.

**Weights:** gaming revenue quality & visitation 25% · margins, promo intensity & unit economics 25% · regulatory/license position 20% · balance sheet 15% · valuation 15%.

## Education services

Tuition, program fees, testing, training, and employer-funded education. Growth quality depends on enrollment, retention, student outcomes, regulatory standing, and cash collection — outcomes and regulation can dominate valuation.

| Metric | Positive | Watch | Negative | How to read it |
|---|---|---|---|---|
| **Enrollment growth** | > 5% with good outcomes | 0–5% | Negative | Never separate from outcomes |
| **Starts** | Growing quality cohorts | Flat / volatile | Falling | Leading indicator |
| **Retention** | Improving | Flat | Declining | Quality signal |
| **Completion / outcomes** | Strong / improving | Mixed or limited disclosure | Weak / disputed | Regulatory- or company-reported; check source |
| **Revenue per student** | Stable / rising | Mix-driven | Falling | Pricing and program mix |
| **Marketing cost per start** | Efficient | Rising | Unsustainable | Often Estimated from S&M ÷ starts |
| **Bad debt / receivables** | Low & stable | Rising | Receivables outgrow revenue | Cash-quality warning |
| **Cash conversion** | FCF tracks earnings | Mixed | Weak | Key quality-of-earnings test |

**What NOT to use:** growth without student outcomes and regulatory risk; revenue growth while receivables, bad debt, refunds, or marketing costs deteriorate; comparisons with general consumer discretionary names.

**Red flags:** **Severe** — accreditation loss, probation, or regulatory investigation; poor outcomes causing enrollment collapse; revenue-recognition, refund, or student-financing concerns. **Moderate** — rising bad debt or receivables; marketing spend rising faster than starts; retention deterioration. **Minor** — short-term enrollment timing issue.

**Weights:** enrollment quality, starts & retention 25% · outcomes & regulatory position 30% · cash conversion & receivables 20% · margins & marketing efficiency 10% · valuation 15%.

## Media / subscription relocation note

Media, streaming, advertising networks, and content-heavy entertainment belong in **Communication Services** (AI_Packet_Communications_Telecom.md). Review here only when the business is primarily a consumer subscription service tied to experiences, fitness, or education-like content. If so, use this compact overlay: subscriber growth (> 10% Positive / 0–10% Watch / negative Negative) paired with churn (often undisclosed → Needs verification), ARPU trend, engagement, content/CAC efficiency, and FCF after content investment. **Never** judge on subscriber growth alone, and do not value as SaaS unless retention, gross margin, and CAC payback actually resemble SaaS. Valuation: EV/Sales for high-growth unprofitable names; EV/EBITDA, P/E, or FCF yield for mature ones. Weights: subscribers/churn/ARPU 30% · engagement & retention 20% · content/CAC efficiency 20% · FCF after content 15% · valuation 15%.

## Mixed businesses

Use segment analysis when several material Consumer Services models coexist: owned hotels + franchise fees → separate real estate from fee earnings; land-based casino + online betting → separate casino EBITDA from digital unit economics; parks + media → likely sum-of-the-parts; multi-brand restaurant groups → brand-level comps and margins where disclosed. If segment data is insufficient, lower data confidence and say so.

## Peer-group rules

Do not compare: franchise-heavy restaurants vs company-owned operators without adjustment · asset-light hotel franchisors vs hotel REITs or owned-hotel operators without adjustment · casinos vs online betting platforms without segment separation · cruise lines vs hotels just because both are travel · education companies vs broad consumer discretionary · subscription media vs SaaS by default · theme parks vs restaurants just because both serve consumers. For mixed businesses, build peer groups by segment.

## Valuation summary

| Subsector | Preferred methods | Avoid |
|---|---|---|
| Restaurants | P/E, EV/EBITDA, FCF yield, EV/unit where useful; value royalty streams separately from owned operations | System sales as company revenue |
| Hotels | EV/EBITDA, P/E, FCF yield; fee-based earnings multiple for asset-light; NAV for owned real-estate-heavy | Owned vs franchised margin comparisons |
| Leisure / theme parks | EV/EBITDA, FCF yield; asset/NAV context where assets are irreplaceable | Ignoring fixed-cost leverage and maintenance capex |
| Cruise | Through-cycle EV/EBITDA, FCF yield after ship capex, debt-adjusted valuation | Peak-cycle P/E |
| Gaming | EV/EBITDA, FCF yield, sum-of-the-parts (land-based / digital / real estate) | Treating hold-rate spikes as recurring |
| Education | P/E, EV/EBITDA, FCF yield with regulatory-risk discount | Revenue growth without outcomes |
| Media / subscription | EV/Sales (high-growth), EV/EBITDA / P/E / FCF after content (mature) | Subscriber growth alone |

## Data availability notes

If a metric is not disclosed, do not invent it — use a proxy only when labeled **Estimated** (or **Estimated proxy** per the shared rules), and mark important missing metrics **Needs verification**. Commonly undisclosed or inconsistent: restaurant traffic, AUV, and franchisee health (infer from closures, bad debt, royalty disputes); hotel RevPAR comparable-set definitions; casino hold normalization and promo detail; cruise net-yield definitions (check reconciliation); education outcomes (may be regulatory-source only); subscription churn and CAC.

## Scoring template

Score each pillar 2 (Positive), 1 (Watch), 0 (Negative) vs peers and own history, using the **subsector weights above**; weighted total ÷ 2 = 0–100%. ~75%+ strong on current evidence; 50–75% mixed — investigate the weak pillar; <50% with sufficient evidence and no verified Severe flag = weak on current evidence.

**Override rule:** any verified Severe red flag caps the total score at 50% until resolved. Two or more Severe red flags usually disqualify the company from normal fundamental analysis (special-situation territory). Verify flags against primary sources before applying the cap.

**Adaptive deep dives** (for the skill's follow-up action #6): Restaurants → traffic vs price / unit economics / franchisee health / lease-adjusted leverage. Hotels → RevPAR & occupancy / asset-light vs owned mix / debt maturities / pipeline quality. Leisure → attendance & per-capita spend / maintenance capex / fixed-cost leverage. Cruise → bookings & yields / leverage & ship capex / fuel sensitivity. Gaming → license risk / promo intensity / digital economics / hold normalization. Education → enrollment quality / accreditation risk / outcomes & receivables. Mixed → segment economics / sum-of-the-parts.

## Conclusion template

End with exactly one of: **strong on current evidence** / **mixed, needs more evidence** (name the evidence) / **weak on current evidence** (score <50% with sufficient evidence and no verified Severe flag) / **high-risk, special situation** / **insufficient data** — plus data confidence (High/Medium/Low), the subsector used, and a two-sentence thesis including what would break it. No buy/sell/hold language.
