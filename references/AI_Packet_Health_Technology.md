# AI Stock Review Packet: Health Technology

**Version 2.2.5 — Last updated 2026-09-22.** Supersedes v2.2.4. v2.2.5 adds one shared expectations-module sentence: where a sector packet defines an expectations adaptation, it governs the variables solved for and the value split (Banks and Insurers now define one). v2.2.4 adds the expectations-embedded valuation module: the universal expectations test (reverse-solve the price for required growth, margin, reinvestment and discount rate), the proven-vs-unproven enterprise-value split with its valuation-pillar caps, and the "Estimated — expectations-implied" sub-label. v2.2.3 corrections: runway denominator excludes marketable-securities flows; adds a packet-local evidentiary-authority tag for clinical/regulatory/patent claims; sub-routes diagnostics vs life-science tools and generics vs biosimilars with their own weights; adds mixed-company EV-weighted scoring; MAUDE signal-not-rate limitation; CRL/Class I recall as candidate (not automatic) Severe; "expected competitive entry" labeled an estimate; Medicare-negotiation materiality test. Supersedes v2.1: rebuilt as a strict execution file with mandatory branch routing (commercial biopharma / development-stage biotech / medical devices / diagnostics & tools / generics & biosimilars / mixed), each with its own metrics, red flags, and scoring weights; adds the v4 provenance standard, asset-level clinical evidence rules, forward catalyst-funded runway, patent-cliff verification beyond filings, EV-impact-based binary-event severity, accelerated-approval and manufacturing/quality/reimbursement risk, and the five-category conclusion. Educational framework — not investment advice. No buy/sell/hold language.

*Pharmaceuticals, biotech, medical devices, diagnostics, life-science tools, generics/biosimilars* — GICS: Health Care (Pharmaceuticals, Biotechnology & Life Sciences; Health Care Equipment & Services)

**Core principle: route to the business model before selecting any metric.** Pharma, pre-commercial biotech, and devices have different operating models, regulatory pathways, valuation methods, and financial metrics. Applying earnings multiples to a pre-commercial biotech, or drug pipeline logic to a device maker, is the sector's defining analytical mistake. Verified does not mean Positive.

## Prompt

> Analyze [company name / ticker] using the uploaded Core Framework and this Health Technology guide.
> Do not use buy/sell/hold language.
> Provide: 1. Business model summary · 2. Sector and branch classification · 3. Peer group with rationale · 4. Key branch metrics with provenance labels · 5. Values vs peers and 5-year history · 6. Positive/Watch/Negative assessment · 7. Severe red flags, if any · 8. Valuation method appropriate for the branch · 9. Data confidence: High/Medium/Low · 10. Neutral research conclusion: strong on current evidence / mixed, needs more evidence / weak on current evidence / high-risk, special situation / insufficient data.
> Use primary sources (10-K, 10-Q, 20-F, 6-K, earnings releases, FDA/EMA databases, ClinicalTrials.gov, Orange/Purple Book, CMS records). Do not rely only on screeners, press releases, or summaries.

## Branch routing

Classify into exactly one primary branch before loading metrics or scoring weights:

1. **Commercial biopharma** — approved products generate most revenue; driven by product sales, loss of exclusivity, pipeline replacement, pricing, manufacturing quality.
2. **Development-stage / pre-commercial biotech** — little or no product revenue; driven by clinical evidence, trial design, probability of success, runway, financing, asset concentration.
3. **Medical devices** — driven by procedure volume, installed base, recurring consumables, device regulatory pathway, reimbursement, recalls, physician adoption.
4. **Diagnostics & life-science tools** — instrument + consumable razor/blade models, test menu, reimbursement, sample volume; margin and reimbursement profile differ from both drugs and therapeutic devices.
5. **Generics & biosimilars** — commodity or semi-commodity economics; price erosion, manufacturing scale and quality, first-to-file/settlement dynamics; low margins are normal.
6. **Mixed health technology** — no branch clearly dominates.

For mixed companies, classify by normalized segment operating profit, then revenue, invested capital, management reporting, and estimated enterprise-value contribution; analyze each other material segment separately and state which branch covers which segment. Do not apply pharma thresholds to devices or device metrics to biotech.

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

**Clinical/regulatory/patent claims are Verified only when the review reads the exact primary record.** Acceptable primary records: company regulatory filings · FDA approval/decision documents · Orange Book (small-molecule patents/exclusivity) · Purple Book (biologics/biosimilars) · ClinicalTrials.gov and WHO ICTRP · EMA/CTIS records · peer-reviewed published trial results · CMS coverage/coding/payment records · FDA device clearance/approval/recall/MAUDE databases · USPTO patent-term-extension records. A company press release verifies only what management *reported* — never clinical efficacy, regulatory acceptance, or patent enforceability. A "met its endpoint" press line without the endpoint definition, effect size, confidence interval/p-value, safety data, and trial design stays **Reported, pending direct verification**.

**Evidentiary authority (clinical/regulatory/patent/reimbursement claims only).** Provenance says whether the review read the source; authority says how independently established the underlying claim is — the two are separate. Alongside the provenance label, tag such claims with one of: **regulatory-confirmed** (an agency decision, approval, enforcement action, or final legal/coverage record) · **registry-reported** (sponsor/investigator-submitted trial-registry data — registries apply only limited quality review and do not endorse the content) · **peer-reviewed** (published trial results) · **company-reported** (a filing, presentation, call, or press release). Reading a ClinicalTrials.gov record directly is *directly read · registry-reported* — it verifies what the sponsor entered, not that enrollment is on track or the therapy works. Only *regulatory-confirmed* or *peer-reviewed* authority can carry a Positive rating for an efficacy or approval claim; registry- and company-reported claims cap the relevant clinical pillar at Watch until corroborated. This tag is local to this packet and does not change the shared v4 provenance labels.

## Shared rules

**Conflicting figures rule (universal):** when two figures for the same metric appear to conflict, do not choose one immediately. First classify the difference: 1. different scope — group vs segment, consolidated vs ex-subsidiary · 2. different basis — gross vs net, reported vs adjusted · 3. different period — quarterly, annualized, LTM, fiscal year · 4. different currency · 5. different definition — company-defined vs packet-defined. Show both figures with provenance labels, then rate the pillar based on the figure that best matches the packet definition. If neither figure matches the packet definition, keep the pillar at Watch or Needs verification.

**Estimated proxy:** when a metric is calculated from available inputs but does not match the company's exact disclosed definition, label it **"Estimated proxy"** and state the inputs used. Examples: an AFFO payout proxy estimated above 100% when AFFO itself is not disclosed; an interest coverage proxy estimated from verified income-statement inputs but not company-disclosed; a net debt/EBITDAre proxy estimated when EBITDAre is not disclosed or JV/pro-rata treatment is unresolved. Never imply the proxy is the same as the company's official metric: a proxy is a sub-type of Estimated, is never Verified, never High confidence, and any rating that rests on it must say so.

**Guidance is not achievement:** guidance, targets, and management plans can support a Watch or directional comment, but they should not receive full Positive credit unless supported by achieved results, binding regulatory approval, or directly verified realized performance. This applies especially to: utilities rate-base growth guidance · REIT rent ramp / stabilized rent targets · energy production or capex targets · SaaS margin expansion targets · bank medium-term ROE targets · biotech pipeline readouts and expedited-program designations.

**Expectations are not results (universal):** a price already contains a forecast, and a review that only compares multiples never states what that forecast is. Run this test whenever the valuation pillar would otherwise rest on a multiple above the company's own 5-year range, or whenever the market or management thesis rests on segments with no achieved results; otherwise record "expectations test not triggered" and move on. Invert the valuation — hold the current price fixed and solve for what it requires: revenue CAGR over a stated horizon, steady-state operating or FCF margin, reinvestment (sales-to-capital or reinvestment rate), the discount rate with its components, and a terminal growth rate no higher than the long-run risk-free rate. Convert the requirement into absolute end-of-horizon revenue and test it three ways: against the company's own achieved 5-year record, against the best verified peer analog at comparable scale, and against the current size of the market being addressed. **TAM × assumed share is not a valuation output — it is the assumption under test.** Where a sector packet defines an expectations adaptation, the adaptation governs the variables solved for and the value split; the triggers, caps and labels of this module still apply.

**Proven vs unproven enterprise value:** split EV into the part the proven business supports under the sector packet's normal valuation method and the residual the market is paying for optionality. A segment counts as proven only when the company discloses its revenue AND either its operating profit or a company-defined unit economic; anything else is unproven, is valued separately and labeled, and is never blended into the base multiple. Report the residual as a share of total EV. Rules: required inputs that exceed anything the company has achieved — or anything a verified peer has achieved at comparable scale — cap the valuation pillar at Watch unless the review names the specific verified evidence supporting the higher requirement · residual EV above ~50% of total EV caps the valuation pillar at Watch and obliges the conclusion to state the residual share, whatever the operating pillars show · disclosure too thin to build the test (no segment detail, no margin path) makes valuation **Needs verification**, never a favorable default · do not penalize the same optimism twice by both discounting the required growth and inflating the discount rate — pick one and say which.

**Estimated — expectations-implied:** every output of this test carries that label, a sub-type of Estimated. It is never Verified and never High confidence, because the solution depends on assumptions the review itself chose; only the inputs (price, period-end share count, net debt, disclosed segment figures) carry labels of their own. **Avoid:** analyst price targets as evidence of value · forward multiples built on margins the company has never achieved · "cheap versus its own history" when that history sits entirely inside one expansion regime · peer multiples where the peers are themselves priced on expectations.

## Quality of earnings & geography

Profits converting into cash? Over 3–5 years FCF should roughly track net income. Watch: 'adjusted' EPS that excludes amortization of acquired intangibles, IPR&D write-offs, milestone and contingent-consideration charges year after year; acquisitions masking weak organic growth and building goodwill; capitalized development under IFRS inflating margins vs US-GAAP peers; receivables outgrowing revenue. Rule: high-quality earnings are recurring, cash-backed, not dependent on repeated adjustments. Geography/currency: where revenue and profit are generated (often different tax jurisdictions — IP domiciles distort both), FX debt vs local revenue, and exposure to tariffs, sanctions, or national pricing regimes.

## Expedited-program & designation rules (all drug branches)

Record expedited programs separately and never treat a designation as approval or as evidence of efficacy: Fast Track · Breakthrough Therapy · Priority Review · Accelerated Approval · Orphan designation · RMAT. A designation speeds development or review; it does not guarantee approval (guidance-is-not-achievement applies).

**Accelerated Approval requires its own risk test.** When a product is on Accelerated Approval, record: surrogate endpoint used · confirmatory-trial requirement and status · enrollment progress · required completion date · conversion-to-traditional status · withdrawal or label-restriction risk. Unconfirmed accelerated approvals carry ongoing regulatory risk that a traditional approval does not.

## Binary-event severity rule (all branches)

A pending clinical result or regulatory decision is **Severe only when failure would probably**: eliminate roughly half or more of estimated gross asset value (use a valuation *range*, not one market-price snapshot — market cap can be near-zero, negative-EV, or cash-heavy for biotech, which breaks a simple "half of EV" test) · threaten the ability to continue the funded development plan · invalidate the central platform/mechanism thesis · or leave no independently financeable program. Otherwise it is **Moderate** (material but not existential). A diversified company does not get an automatic Severe flag merely for having a Phase 3 or PDUFA date pending; a single-asset biotech's Phase 2 can be existential. Rate severity by EV/revenue dependence, remaining pipeline, post-failure cash, and how truly binary the event is.

---

## Branch 1 — Commercial biopharma

Driven by product-level sales, loss of exclusivity (LoE), and pipeline replacement. Metrics (judge vs subsector peers and own 5-year history, not fixed universal thresholds):

| Metric | Read it as |
|---|---|
| Organic / constant-currency revenue growth | Separate volume, price, mix; separate acquired from organic |
| Revenue by major product; top-product concentration | One product > 30–50% of sales is a structural risk to size and durability |
| 5-year LoE exposure | % of revenue from products losing exclusivity within 5 years — see patent rules |
| Pipeline assets by stage & indication | Replacement capacity for LoE — see asset-level rules |
| Adjusted R&D intensity | (expensed + capitalized development) ÷ revenue vs peers; productivity, not just level |
| Operating margin, packet FCF, ROIC | Cash quality; watch adjusted-EPS add-backs |
| Net debt & maturity profile; dividend/buyback coverage | Capital allocation and balance-sheet resilience |

**Valuation:** P/E and EV/FCF on earnings **after** expected patent erosion — never rate a low trailing multiple Positive when a material cliff is not yet reflected in normalized earnings. Add FCF yield, dividend coverage, and pipeline-adjusted (rNPV) contribution for late-stage assets. **Scoring weights:** Product growth & commercial durability 20% · Pipeline quality & replacement capacity 25% · Patent/exclusivity exposure 15% · Margins, FCF & ROIC 15% · Balance sheet & capital allocation 10% · Valuation vs normalized earnings 10% · Pricing/regulatory/manufacturing risk 5%.

**Severe (candidates — a CRL, warning letter, import alert, or Class I recall is Severe only when the affected product/site is material and remediation is uncertain, lengthy, costly, or likely to impair approval/supply/adoption):** patent/exclusivity erosion likely to remove a material share of normalized profit with no credible replacement · material manufacturing/quality issue preventing supply or approval · regulatory or safety action threatening a major product · financing or covenant distress. **Moderate:** single-drug dependence above half of revenue · thin late-stage pipeline into a cliff · rising gross-to-net erosion. **Medicare-negotiation exposure is not automatically Moderate** — test selected-product status, applicability year, Part B vs D, Medicare volume, and Maximum Fair Price vs actual *net* (not list) price plus commercial spillover; selected status can be Verified, but the earnings impact is usually Calculated or Estimated.

## Branch 2 — Development-stage / pre-commercial biotech

Revenue and earnings are largely irrelevant; value rides on clinical evidence, runway, and market size.

**Cash runway — trailing AND forward:** Liquidity = unrestricted cash + equivalents + liquid marketable securities (exclude restricted/pledged cash and uncommitted facilities; count an undrawn credit line only if committed, covenant-available, and economically usable). Normalized cash burn = cash operating loss + capex + capitalized clinical/development/manufacturing spend classified as investing + contractual milestone/development payments due under the current plan − recurring non-dilutive cash receipts. **Exclude marketable-securities purchases and maturities, financing flows, and acquisitions unless part of the forward plan** — buying Treasuries is not burn, and counting investing cash flow raw is the classic runway error. Base runway = liquidity ÷ normalized trailing monthly burn. Forward runway = liquidity ÷ expected monthly burn under the disclosed clinical/operating plan (pivotal enrollment, manufacturing scale-up, capex). Show base runway, forward runway, the next value-defining catalyst, expected liquidity at that catalyst, a ≥6-month delay sensitivity, post-catalyst buffer, likely financing requirement, and dilution sensitivity. **Runway > 24 months is not automatically Positive if it does not fund the next value-defining milestone.**

**Lead-asset clinical evidence (required for each material asset):** asset & indication · mechanism/modality (small molecule, antibody, cell, gene therapy) · trial identifier & development stage · design (randomized/blinded/controlled/single-arm) · comparator · primary endpoint (clinical / surrogate / biomarker) · effect size (absolute + relative) · statistical evidence (CI, p-value) · safety (discontinuations, serious events, imbalance) · enrollment (planned vs actual) · primary completion / expected readout · regulatory designations & agency feedback · competition · ownership economics (royalties, milestones) · program-specific probability reasoning · risk-adjusted valuation contribution. Do not assign probability from clinical phase alone — attrition varies by therapeutic area, modality, endpoint, and design. (The full multi-asset table is a follow-up deep dive; the first pass covers the lead asset(s) driving EV.)

**Valuation — rNPV discipline:** for each asset disclose eligible population, diagnosis/treatment rate, eligible share, price and gross-to-net, peak penetration, launch timing, exclusivity period, development + commercial costs, milestones/royalties, probability of technical success, probability of regulatory success, discount rate, residual value, and a sensitivity range. **Do not double-count clinical risk** through both a heavily risk-adjusted probability and an inflated "biotech discount rate" for the same uncertainty. **Scoring weights:** Lead-asset clinical evidence 25% · Cash runway & financing risk 20% · Trial design & regulatory pathway 15% · Pipeline diversification & platform validity 15% · Market opportunity & competition 10% · rNPV vs enterprise value 10% · Management execution 5%.

**Severe:** forward runway does not reach the next value-defining catalyst with an adequate buffer · clinical hold or material unexplained safety imbalance · lead-asset failure that invalidates the central platform thesis · regulatory feedback requiring a materially larger/longer program without funding · going-concern or covenant pressure. **Moderate:** single-asset concentration with a non-binary but important readout pending · reliance on one modality/mechanism · financing likely within 12 months at material dilution.

## Branch 3 — Medical devices

Driven by procedures, installed base, and recurring consumables — not drug pipelines.

Metrics (where relevant): organic revenue growth · procedure volume growth · new system placements & installed base · utilization per installed system · consumables/service mix & recurring-revenue % · ASP & new-product contribution · gross margin and service margin · adjusted R&D intensity · packet FCF margin & ROIC · inventory & obsolescence · capital-equipment backlog · warranty/field-service costs · supplier/manufacturing concentration. **Regulatory & access are separate hurdles:** FDA pathway (510(k) / De Novo / PMA — different evidence standards) is authorization only; coding, coverage, and payment (CMS) determine commercial access. For EU exposure: MDR/IVDR certification, notified-body availability, transition status. Track recalls and safety communications. **MAUDE is a signal-detection source, not an event-rate database** — never compute or compare adverse-event incidence from raw MAUDE counts (under-reporting, duplicates, no exposure denominator, no causation). Corroborate any signal with recalls, FDA safety communications, postmarket studies, registries, and company complaint-rate disclosures before rating.

**Valuation:** organic-growth-aware EV/EBIT, EV/Sales vs durable growth, P/E, FCF yield — vs own range and peers; device economics do not use drug rNPV. **Scoring weights:** Organic growth & procedure trends 20% · Product portfolio & installed-base quality 20% · Margins, FCF & ROIC 20% · Regulatory, reimbursement & safety 15% · Innovation & new-product productivity 10% · Valuation 10% · Balance sheet & capital allocation 5%.

**Severe (candidate — apply only when the affected product/site is material and remediation is uncertain, lengthy, costly, or likely to impair supply/approval/adoption; the classification alone does not quantify damage):** Class I recall or comparable safety action on a material product · loss/suspension of required authorization · material reimbursement loss · quality-system failure disrupting production · adverse-event pattern suggesting a systemic product issue. **Moderate:** reliance on one platform or procedure · reimbursement or coding under review · notified-body/MDR transition risk · single-source component dependence. **Do not treat FDA authorization as proof of reimbursement, adoption, or commercial success.**

## Branch 4 — Diagnostics & life-science tools

Sub-route first — these two are economically different: **4A clinical diagnostics / lab services** vs **4B life-science tools & research instruments**. Do not score a sequencing-instrument maker mainly on reimbursement-per-test, or a reference lab mainly on instrument placements.

**4A clinical diagnostics:** test volume · revenue per test · payer mix & reimbursement/denial rate · clinical validity and utility · sample-collection network & lab capacity · test-menu concentration · CLIA certification and proficiency testing · **US LDT oversight as of the analysis date** — state current FDA policy, CLIA status, applicable state requirements, and payer evidence standards (do NOT assume any previously proposed or vacated FDA LDT framework is in effect; the 2024 LDT final rule was vacated in 2025). *Weights:* test volume/reimbursement/payer quality 25% · clinical validity, utility & menu durability 20% · margins, FCF & ROIC 20% · regulatory & lab quality 15% · competitive position & innovation 10% · valuation 10%.

**4B life-science tools:** instrument placements & installed base · consumables pull-through & recurring revenue · service revenue · academic/government/biopharma research budgets & funding cycles · China exposure · capital-equipment order trends · installed-instrument utilization · customer destocking. *Weights:* instrument demand & installed-base growth 20% · consumables pull-through & recurring revenue 20% · margins, FCF & ROIC 20% · end-market & funding-cycle exposure 15% · innovation & competitive position 15% · valuation 10%.

Margins sit between devices and tools; use device-style growth/FCF valuation. For EU diagnostics, check IVDR transition deadlines by device class rather than describing generic "transition risk." Borrow the device red-flag list plus reimbursement-loss and test-menu-obsolescence risks.

## Branch 5 — Generics & biosimilars

Sub-route first — different legal and commercial systems: **5A conventional generics** (Hatch-Waxman ANDA) vs **5B biosimilars** (BPCIA §351(k)). Low gross margin is normal in both, not Negative.

**5A generics:** price erosion rate · ANDA approvals & pipeline · Paragraph IV status · 180-day first-applicant exclusivity eligibility and trigger · portfolio breadth · controlled-substance exposure · customer concentration · manufacturing quality (483s/warning letters are existential here) · shortage opportunities & discontinuations · gross margin by product cohort. *Weights:* portfolio growth & price erosion 25% · manufacturing quality & supply reliability 20% · pipeline/approvals/exclusivity 15% · margins & FCF 15% · balance sheet & litigation 15% · valuation 10%. Do NOT apply the 180-day/Paragraph IV framework to biosimilars.

**5B biosimilars:** reference-product market size · patent litigation & settlements · earliest permitted launch date · approved competitors · interchangeability status · formulary/payer access · provider economics · rebate/contracting strategy · manufacturing capacity · market-share ramp · price discount & net-price erosion. The Purple Book identifies licensed biosimilar/interchangeable products but does NOT establish future share or actual launch date. *Weights:* approved & launch-ready portfolio 20% · market access & commercial uptake 20% · patent/settlement/launch timing 15% · manufacturing & regulatory execution 15% · margins, FCF & capital 15% · valuation 15%.

Valuation on P/E and EV/FCF with an explicit price-erosion assumption. Severe: major-site quality action · concentrated portfolio facing a price-erosion cliff.

---

## Patent & exclusivity analysis (drug branches)

Company filings are necessary but not sufficient. For US products also consult: FDA Orange Book (small-molecule patents & exclusivities) · Purple Book (biologics & biosimilar status) · USPTO patent-term-extension records · litigation/settlement disclosures · filed/launched generic or biosimilar applications. Build a product-level table:

| Product | Revenue share | Patent protection | Regulatory exclusivity | Expected competitive entry | Competition type | Estimated erosion |
|---|---:|---|---|---|---|---:|

Distinguish composition-of-matter vs formulation vs method-of-use patents, regulatory exclusivity, pediatric extension, patent-term extension (USPTO restores term lost to regulatory review — original expiry is not always the economic date), litigation/settlement dates, authorized-generic plans, and generic vs biosimilar competition. **Patent expiration, exclusivity expiration, and actual competitor launch are different dates.** Label "expected competitive entry" an **Estimate** unless a launch has actually occurred or a legally binding, publicly disclosed settlement fixes the date — do not describe an LoE date as certain otherwise.

## Manufacturing, quality & pricing risk (drug branches)

Assess separately from clinical efficacy: FDA Form 483 observations · warning letters · import alerts · Complete Response Letters (a CRL ends the review cycle without approval) · site concentration & third-party manufacturing dependency · comparability after process changes · cold-chain and capacity constraints · batch failures. Pricing/reimbursement: gross-to-net deductions & rebates · government-payer exposure · formulary position & prior authorization · international reference pricing · **Medicare negotiation exposure (negotiated prices took effect Jan 1, 2026 — an operating issue now, not hypothetical, for affected products)** · Medicaid/340B. For devices, walk the full chain: FDA authorization → coding → coverage → payment level → hospital economics → physician incentives.

## Default first-pass dashboard

Use the six cards for the routed branch (see each branch above). Each card shows: value · Positive/Watch/Negative rating · provenance label (per the v4 standard) · one-line explanation. Use concise tables. The first-pass score is always provisional unless: the branch is confirmed; core branch metrics verified from filings/registries; lead clinical/regulatory claims verified against primary records; and at least partial peer comparison performed.

## Follow-up actions

Offer: 1. Verify branch classification and segment split · 2. Deep dive: full asset-by-asset clinical evidence table · 3. Deep dive: patent/exclusivity product table (Orange/Purple Book) · 4. Deep dive: cash runway & financing (biotech) · 5. Deep dive: reimbursement & pricing exposure · 6. Deep dive: manufacturing/quality (483s, CRLs, recalls) · 7. Compare vs branch peers · 8. Deep dive: rNPV build for the lead asset.

Priority logic: runway short or near a catalyst → 4. Material LoE approaching → 3. On Accelerated Approval or pending PDUFA → 2. Device with authorization but unclear coverage → 5. Recent 483/warning letter/recall → 6.

## Score-change audit trail

Whenever a follow-up action changes the score, show all nine items: 1. previous score · 2. updated score · 3. metric that changed · 4. old status · 5. new verified value · 6. source document · 7. exact quote showing label and value · 8. pillar affected · 9. reason for the change. If the exact quote cannot be provided, do not change the score — keep the metric at Needs verification. Verification alone does not change the score; only a changed pillar rating does.

## Data confidence rules

**High:** recent 10-K/10-Q/20-F/6-K/audited statements, or a primary regulatory/registry record (FDA decision, Orange/Purple Book, ClinicalTrials.gov results, CMS record), with the exact label/value quoted. **Medium:** earnings release or investor presentation with a labeled table; a company press release for what management reported (never for efficacy/approval/enforceability). **Low:** aggregator-only data, analyst pipeline models, unlabeled numbers, phase-only probability guesses. If a key metric is Low confidence, state how it affects the pillar score.

## What NOT to use

Revenue and earnings multiples for pre-commercial biotech. P/E across pharma without adjusting for pipeline maturity and looming cliffs. One universal threshold table across branches. A single phase-based probability for rNPV. Press-release efficacy claims as verified. FDA authorization as proof of reimbursement or adoption. "Adjusted" EPS that permanently excludes amortization, IPR&D, and milestone charges without scrutiny.

## Common mistakes to avoid

Scoring a biotech on P/E or EV/EBITDA · treating runway as Positive when it doesn't fund the next catalyst · assigning rNPV probability from phase alone · double-counting clinical risk in both probability and discount rate · calling a low pharma P/E "cheap" ahead of an unmodeled patent cliff · treating a Phase 3 as automatically Severe regardless of diversification · treating a designation (Breakthrough/Fast Track) as approval · applying drug pipeline logic to a device maker · assuming FDA clearance means reimbursement · ignoring 483s/CRLs/recalls · using diluted weighted-average shares as the primary dilution measure (use period-end, split-adjusted) · upgrading a pillar because a metric was found while it is still in Watch range.

## Scoring mechanics (all branches)

Rate each pillar vs peers and own history: Positive = 2, Watch = 1, Negative = 0. Pillar contribution = pillar weight × rating ÷ 2 (branch weights total 100%); score = sum of contributions, 0–100%. **Mixed companies:** score each material segment on its own branch weights first, then consolidate only when segment enterprise-value contributions can be estimated with reasonable confidence: consolidated score = Σ (segment score × estimated segment EV share). Do NOT weight by revenue — a low-revenue pipeline or platform segment can carry most of the EV. If segment EV shares cannot be estimated reliably, report the separate segment scores and conclude "mixed, needs more evidence" without a consolidated number. ~75%+ strong on current evidence; 50–75% mixed; <50% with sufficient evidence and no verified Severe flag = weak on current evidence. Any verified Severe flag caps the score at 50% — always show the uncapped score, the cap applied, and the displayed score. A flag activates the cap only when its evidence is Verified or Calculated — verified inputs; a flag resting on press releases, user excerpts, or relayed values stays a provisional warning. Two or more verified Severe flags usually mean high-risk / special situation. The score is a research organizer, not a prediction engine.

## Conclusion template

End with exactly one of: **strong on current evidence** / **mixed, needs more evidence** (name the evidence) / **weak on current evidence** (score <50% with sufficient evidence and no verified Severe flag) / **high-risk, special situation** / **insufficient data** — plus data confidence (High/Medium/Low), the branch used, and a two-sentence thesis including what would break it. No buy/sell/hold language.

## Final sector checklist

1. Branch classified before metrics loaded; mixed businesses split by segment.
2. Peer group built within the branch on business model, stage, and modality — never a bare sector label.
3. Core branch metrics verified with exact labels from filings/registries where possible.
4. Clinical/regulatory/patent claims verified against primary records, not press releases.
5. (Biotech) base AND forward runway computed; next catalyst funding tested.
6. (Biotech) lead-asset clinical evidence recorded with effect size, statistics, safety, and design.
7. (Pharma) product-level patent/exclusivity table built from Orange/Purple Book + filings.
8. (Devices) regulatory pathway, reimbursement chain, and recall/adverse-event trends reviewed.
9. Expedited programs and any Accelerated Approval risk-tested; designation ≠ approval.
10. Manufacturing/quality and pricing/reimbursement risks assessed separately from efficacy.
11. Binary-event severity rated by EV impact, not phase alone.
12. "What NOT to use" respected; quality-of-earnings and geography/currency checks run.
13. Red flags graded with provenance labels and verified before applying the Severe cap.
14. Valuation done with the branch-appropriate method (normalized P/E for pharma; rNPV + runway for biotech; growth/FCF multiples for devices).
15. Weighted score computed on the branch weights; uncapped and capped scores shown when a cap applies; neutral research conclusion written with data confidence, branch, and unresolved gaps.

*This is general information only and not financial advice. For personal guidance, please talk to a licensed professional.*
