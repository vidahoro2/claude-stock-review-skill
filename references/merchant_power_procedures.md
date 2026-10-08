# Merchant power procedures (Utilities packet, Branch B)

**Version 1.0 — Last updated 2026-10-08.** Companion to `AI_Packet_Utilities.md` v2.3.0. Educational framework — not investment advice. No buy/sell/hold language.

**When to load:** automatically, during the first pass, whenever a Branch B company (or the Branch B share of a mixed company) triggers the expectations test, or its valuation pillar would rate above Watch, or a blended score needs segment EV shares. This file is part of the first pass in those cases — it is not a deep dive and does not wait for a user request. If the procedures cannot be completed, valuation is **Needs verification** and scores no higher than Watch. Every output here is **Estimated** (model outputs: "Estimated — expectations-implied"); verified inputs never make a modeled result Verified.

## 1. Choose the horizon

Choose and justify a valuation horizon independently of hedge coverage — typically long enough to pass the main contract expiries and any announced retirements or license dates that matter to value. State the horizon and why.

## 2. Forward-curve case

A scenario built from current market prices, not evidence of mid-cycle earnings. Bridge, year by year over the horizon:

1. **Energy margin** — hedged volumes at hedged prices; open volumes at the current forward curve for their market, net of fuel and variable cost (state the fuel curve used).
2. **Capacity revenue** — cleared auction results where known; note caps, collars, and pending rule changes.
3. **Retail margin** — at the company's achieved unit margin unless a change is disclosed.
4. **Support payments** — e.g., nuclear production tax credit, computed against the price path (it declines as receipts rise) and stopping at its statutory end.
5. **Operating costs** — fixed O&M, SG&A.
6. **Maintenance capital and nuclear fuel.**
7. **Cash interest, cash taxes, working capital and collateral.**

Output: EBITDA and FCFE (or FCFF) per year. Label the result **Estimated**.

## 3. Normalized case

A separately justified case — never the forward curve relabeled. Acceptable bases, with the reason stated: realized margins averaged over a period that includes both tight and loose market conditions; or the long-run price at which new capacity would enter the market. Use the same bridge as section 2. Current curves do not establish mid-cycle conditions; say why the chosen basis is representative.

## 4. Reverse test and proven/unproven split

Hold the current price fixed and solve for what it requires: the margin or growth path, the reinvestment that growth requires (funded inside the model), contract expiries, and asset lives. Pair FCFE with market capitalization and cost of equity, or FCFF with enterprise value and WACC — never mix them. Terminal growth no higher than the long-run risk-free rate; its sign for an aging fleet comes from the modeled cash-flow path. The yield shortcut (FCF yield ≈ cost of equity − growth) is a steady-state cross-check only, with its assumptions stated.

**Split:** proven = operating fleet and achieved recurring contract earnings. Future contracts with undisclosed economics add visibility, not value ("contracted, economics not disclosed"); if economics can be modeled, they replace the covered merchant cash flows — never add value on top of output already valued at forward prices. Check termination rights, delivery obligations, required investment, and conditions precedent. Unproven residual = unsigned deals, unapproved uprates, uncontracted new builds; report it as a share of EV and apply the module's caps.

**Valuation rating (feeds Branch B pillar 5):** Positive when the price is supported in both cases; Watch when supported in one, or when this procedure was not completed; Negative when supported in neither. "Supported" means the required inputs do not exceed anything the company or a verified Branch B peer has achieved at comparable scale.

## 5. Liquidity stress build

Compare **usable resources** — unrestricted cash plus committed, drawable facility capacity, after existing utilization and restrictions, with cash-versus-letter-of-credit eligibility stated — against **stressed needs** under a stated scenario: incremental collateral, replacement-power purchases during outages, operating needs, and maturities within the scenario window. Note payment timing. Prefer a company-disclosed scenario; a historical event (e.g., a winter-storm price spike) is a benchmark only after explaining comparability with today's portfolio and financing. An analyst-designed stress failure is an Estimated warning, never by itself a Severe flag.

## 6. Segment EV shares for mixed companies

Value each scored segment on its own branch's method (Branch A: P/E or EV/EBITDA against regulated peers, with the rate-base growth basis stated; Branch B: forward-curve and normalized cases at Branch B peer multiples, or the section 2–3 cash flows). Allocate corporate costs, holdco debt, and other corporate liabilities explicitly. Never derive the split from the company's current aggregate market value. Show the weights and whether the conclusion category changes under a ±10-point shift. If reliable shares cannot be established, report branch scores separately and conclude **mixed, needs more evidence**.

## Output

A short table per case (horizon, key price inputs with sources and dates, EBITDA, FCF, implied requirement), the proven/unproven split, the liquidity comparison, and the resulting pillar ratings — every figure labeled.
