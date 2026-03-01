# Stage 4 — Portfolio Construction & Risk Management

> **Reference for**: `[SUBAGENT 4A]` through `[SUBAGENT 4E]`

---

## Objective

**Wait for ALL Stage 3 analyses**. Launch these subagents **simultaneously**.

---

## Subagent Assignments

### [SUBAGENT 4A] — Portfolio Construction

**From all STRONG BUY/BUY stocks**:

1. Rank by composite score (descending)
2. Apply regime filter from Stage 0
3. **Chain allocation**: 2-4 positions per chain based on conviction (more for high-conviction, fewer for lower)
4. **Diversification**:
   - Max 40% per sector (GICS L1) when conviction is high (25% default)
   - Mix of market caps
   - Monitor correlation clusters
   - **Technology sub-sector limits**: Max 20% per sub-sector (SaaS, Cybersecurity, Semiconductors, E-commerce, Fintech, Gaming)
5. Build 15-25 position model portfolio
6. Apply volatility-adjusted sizing from Stage 3H
7. **Tax optimization**: Prioritize TFSA/FHSA/RRSP for rebalancing-heavy positions (no tax drag). Place buy-and-hold in taxable if advantageous.

**Output Format**:
```
=== MODEL PORTFOLIO ===
| Ticker | Company | Allocation % | Account | Trend Chain | Suggested Hold | Entry | Stop Loss | Type |
TOTAL POSITIONS: [X]
CASH RESERVE: [X%] - [Stage 0 rationale]
CANADIAN %: [X%] (preference noted, not requirement)
SECTOR BREAKDOWN: [GICS sectors]
CORRELATION MONITORING: [Groups that may move together]
TAX ACCOUNT ALLOCATION: [TFSA/FHSA/RRSP/Taxable breakdown]
```

---

### [SUBAGENT 4B] — Trend Timing & Risk Matrix

1. Innings assessment per chain (1st-3rd early, 4th-6th mid, 7th-9th late)
2. Kill switch per chain (scenario that invalidates thesis)
3. Correlation overview between chains (identify clusters)
4. Macro risk overlay (rates, recession, CAD/USD, oil scenarios)
5. Timeline: 6-month plays vs. 2-year holds vs. 5-year compounders

**Output Format**:
```
=== TREND TIMING MATRIX ===
| Trend Chain | Innings | Timeline | Kill Switch | Macro Sensitivity |

MACRO SCENARIO ANALYSIS:
- Bull: [Scenario] → Portfolio impact: [Estimate]
- Base: [Scenario] → Portfolio impact: [Estimate]
- Bear: [Scenario] → Portfolio impact: [Estimate]
```

---

### [SUBAGENT 4C] — ETF & Passive Alternatives

Map each chain to best Canadian/U.S. ETF, compare vs. active picks, suggest 5-8 ETF "lazy portfolio" capturing 80% of thesis, flag chains with no good ETF (alpha opportunity).

**Output Format**:
```
=== ETF MAPPING ===
| Trend Chain | Best CAD ETF | Best US ETF | Expense Ratio | Overlap |

LAZY PORTFOLIO:
| ETF | Allocation | Thesis |

ALPHA OPPORTUNITIES: [Chains requiring stock-picking]
```

---

### [SUBAGENT 4D] — Watchlist & Catalyst Calendar

Compile HOLD/WATCH stocks with upgrade triggers. Build 12-month catalyst calendar. Flag Canadian policy decisions impacting chains.

**Output Format**:
```
=== WATCHLIST ===
| Ticker | Verdict | Upgrade Trigger | Target Buy Price |

=== CATALYST CALENDAR ===
[Month-by-month calendar]

CANADIAN POLICY EVENTS:
- [Date]: [Decision] - Impact: [Chains/stocks affected]
```

---

### [SUBAGENT 4E] — Risk Management Rules

**Output Format**:
```
=== RISK MANAGEMENT RULES ===

POSITION LIMITS:
- Max single position: 5% (core), 2% (satellite)
- Max sector: 40% (high conviction) / 25% (default)
- Tech sub-sector max: 20% each (SaaS, Cybersecurity, Semiconductors, etc.)
- Max drawdown: 15% (reduce at 12%)
- Correlation monitoring: Avoid >3 stocks from same macro driver

STOP LOSS RULES:
- Core: Trailing stop 15% from high
- Satellite: Hard stop 12% below entry
- Time stop: Exit if no catalyst within 18 months of expected date

REBALANCING:
- Schedule: Semi-annual OR when position >2x target weight
- Method: Trim winners, add underweights or raise cash
- Note: TFSA/FHSA/RRSP rebalancing has no tax drag; taxable accounts consider holding periods

CHAIN ALLOCATION:
- 2-4 positions per chain based on conviction
- High conviction (>8 score): Up to 4 positions
- Medium conviction (6-8): 2-3 positions
- Lower conviction (<6): Consider ETF or skip

CASH MANAGEMENT:
- Target: [X%] based on Stage 0 regime
- Deploy when: [Conditions]
- Raise when: [Conditions]
```

---

## Framework Principles

Apply critical thinking protocols from `references/02_framework_principles.md`:
- Second-Order Thinking (portfolio-level exposure)
- Supply Chain Mapping (concentration risk)

---

## Data Sources

See `references/01_data_sources.md` for required data sources.
