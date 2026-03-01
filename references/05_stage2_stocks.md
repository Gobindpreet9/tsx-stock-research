# Stage 2 — Stock Universe Generation

> **Reference for**: `[SUBAGENT 2-{CHAIN_ID}]`

---

## Objective

For each trend chain, generate 8-15 candidate stocks. **Canadian-listed preferred but not required** — will select best opportunities regardless of exchange.

**Wait for Stage 0 and Stage 1. Apply macro regime bias when selecting**.

---

## Selection Criteria

1. **Canadian-first preference**: Prioritize TSX/TSX-V listed when quality is comparable; do not exclude superior non-Canadian opportunities
2. **Best-in-class**: Include U.S./International when they dominate the node or no quality Canadian option exists
3. **Market cap mix**: Large (>$10B), mid ($2B-$10B), small (<$2B)
4. **Minimums**: $1 share price, $200M market cap (no penny stocks)
5. **Regime alignment**: Note Stage 0 favorability

---

## Output Format (Per Candidate)

```
TICKER: [TSX:XXX or NYSE:XXX]
COMPANY: [Name]
MARKET CAP: [Approximate]
CHAIN NODE: [Which part of chain]
CANADIAN LISTED: [Yes/No]
REGIME FIT: [Favored/Neutral/Disfavored]
THESIS: [1 sentence]
RISK FLAG: [1 sentence]
DATA FRESHNESS: [Date]
```

---

## Also Include

- **ETFs** for basket exposure
- **Upcoming IPOs** worth watching
- **Insider ownership** levels

---

## Special Considerations

### Component Suppliers (Picks and Shovels)

For physical technology trends, ensure you include:
- Component suppliers (diversified customer base)
- Infrastructure providers
- "Picks and shovels" plays that benefit regardless of end-product winner

**Example**: For robotics, include Nabtesco (gears), Cognex (vision), not just robot makers.

### Geographic Gaps

If no Canadian pure-play exists:
- Explicitly flag: "No Canadian pure-play available"
- Provide best global alternatives
- Consider ETFs as proxy

---

## Framework Principles

Apply critical thinking protocols from `references/02_framework_principles.md`:
- Supply Chain Mapping (identify component suppliers)
- Geographic Gap Acknowledgment
- Second-Order Thinking

---

## Data Sources

See `references/01_data_sources.md` for required data sources.
