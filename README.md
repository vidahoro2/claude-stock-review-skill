# Stock Review — a sector-aware fundamental analysis skill for Claude

A [Claude](https://claude.com) skill for fast, disciplined, sector-aware fundamental review of public companies. It classifies a company into one of 23 sectors, loads only that sector's analytical packet, researches primary sources, and returns a compact research scorecard — then deeper analysis on request.

**This skill produces neutral research only. It never gives buy / sell / hold advice.**

## What it does

The core idea is that different businesses require different lenses. A bank is not scored the way a SaaS company is; a REIT is not valued the way an oil & gas producer is. Importing the wrong sector's metrics is the most common mistake in fundamental analysis, and this skill is built to prevent that.

When you ask Claude to review a company, the skill:

1. **Classifies** the company by where its operating profit actually comes from (not revenue), across 23 sectors.
2. **Loads one sector packet** — each packet has its own key metrics, its own explicit "what NOT to use" list, and its own valuation toolkit.
3. **Researches primary sources** (filings, investor materials) rather than relying on memory.
4. **Returns a compact scorecard first** — showing whether the company warrants deeper research and which figures need verification — and only produces a full memo when you ask.

### Example prompts

- `review DKNG`
- `analyze JPMorgan`
- `what does the guide say about NVDA`
- `stock review O`
- follow-ups: `make deeper analysis`, `verify missing data`, `compare vs peers`, `deep dive valuation`, `create full research memo`

## Sectors covered

Banks · Insurers · Asset Managers & Exchanges · Fintech & Payments · Software / SaaS · Electronic Technology · Health Technology · Health Services · REITs · Utilities · Energy (Oil & Gas) · Retail · Consumer Staples · Consumer Durables · Consumer Services · Commercial Services · Industrial Services · Producer Manufacturing · Process Industries · Distribution Services · Transportation · Communications / Telecom · Mining & Metals.

## Installing

**Claude Code / Cowork:** copy the `stock-review/` folder into your skills directory:

```
~/.claude/skills/stock-review/
```

so that `~/.claude/skills/stock-review/SKILL.md` exists. Restart your session and the skill loads automatically when you ask Claude to review a stock.

**Structure:**

```
stock-review/
├── SKILL.md                        # the skill definition and workflow
└── references/
    ├── 01_Core_Framework.md        # universal rules, loaded only when needed
    ├── AI_Packet_<Sector>.md       # one packet per sector (23 total)
    └── deep_dives.md               # deep-dive procedures
```

## Extending it

Each sector packet is a self-contained markdown file. To add or refine a sector, copy the shape of an existing `AI_Packet_*.md` — its metrics, its "what NOT to use" list, and its valuation approach — and add the row to the classification table in `SKILL.md`. Keep the three shared rules (handling conflicting figures, marking estimated proxies, and treating guidance as guidance rather than achievement) consistent across packets.

## Disclaimer

This skill is provided for **research and educational purposes only**. It does not constitute investment, financial, legal, or tax advice, and nothing it produces is a recommendation to buy, sell, or hold any security. Company data can be wrong, stale, or misclassified. Do your own research and consult a licensed professional before making any investment decision. The authors accept no liability for decisions made using this skill.

## License

Released under the MIT License. See [LICENSE](LICENSE).
