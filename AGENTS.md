# Multi-Stage Parallelized Investment Trend Research Prompt

> **Usage**: Feed this prompt to an AI system with parallel execution capabilities. Each `[SUBAGENT]` block is an independent unit of work.

---

## Data Sources

All agents must use these sources. Flag when data is unavailable or stale (>30 days old):

### Financial Data
- **Company Filings**: SEDAR (Canada), SEC EDGAR (US), company investor relations
- **Financial Metrics**: Yahoo Finance, Google Finance, company quarterly/annual reports
- **Analyst Coverage**: Seeking Alpha, TipRanks, analyst consensus estimates
- **Insider Activity**: SEDI (Canada), SEC Form 4 (US)

### Market Data
- **Price/Volume**: Yahoo Finance, TradingView, broker platforms
- **Valuation Multiples**: Finviz, GuruFocus, YCharts
- **Short Interest**: FINRA (US), TSX short position reports

### Macro/Industry
- **Economic Data**: StatCan, BLS, FRED, Trading Economics
- **Commodity Prices**: Trading Economics, commodity exchanges
- **Industry Reports**: Industry associations, government reports, consultancy reports

### News/Sentiment
- **Company News**: Google News, company press releases, earnings calls
- **Industry News**: Trade publications, industry newsletters
- **Social Sentiment**: Reddit, Twitter/X (for sentiment indicators only, not primary research)

---

## STAGE 0: Macro Regime Assessment (Foundation)

**Objective**: Classify current market regime before trend analysis. This sets risk appetite and sector bias for all subsequent stages.

Launch these subagents **simultaneously**:

### [SUBAGENT 0A] — Interest Rate & Credit Analysis
Analyze: Central bank policy rates (BoC, Fed), yield curve shape (2s10s, 3m10s), credit spreads (IG, HY), real interest rates.

**Output**:
```
RATE ENVIRONMENT: [Restrictive/Neutral/Accommodative]
YIELD CURVE: [Inverted/Normal/Steepening]
CREDIT CONDITIONS: [Tightening/Stable/Easing]
RATE TRAJECTORY: [Cutting/Pausing/Hiking]
IMPLICATIONS: [Which sectors win/lose]
```

### [SUBAGENT 0B] — Economic Cycle Positioning
Assess: Leading indicators (PMI, permits, claims), coincident indicators (GDP, employment, IP), lagging indicators (inflation, unemployment), recession probability models.

**Output**:
```
CYCLE STAGE: [Early/Mid/Late Expansion/Recession/Recovery]
RECESSION PROBABILITY: [X%] over next 12 months
KEY LEADING INDICATORS: [Trending up/down/flat]
CYCLE IMPLICATIONS: [Favor growth/value/defensive/quality]
```

### [SUBAGENT 0C] — Market Regime Classification
Analyze: S&P 500 and TSX trend (50/200-day MA), volatility regime (VIX), sector rotation, risk-on/off indicators (HY spreads, copper/gold), CAD/USD trends.

**Output**:
```
MARKET REGIME: [Bull/Bear/Sideways/Transition]
VOLATILITY REGIME: [Low/Normal/Elevated/Crisis]
RISK APPETITE: [Risk-On/Risk-Off/Mixed]
SECTOR LEADERS: [Top 3 sectors last 3-6 months]
STYLE FAVORABILITY: [Growth/Value/Quality/Momentum/Small-cap]
```

### [SUBAGENT 0D] — Commodity & Currency Outlook
Canada-specific factors: Oil & gas (WTI, WCS, nat gas), key metals (copper, lithium, uranium, gold), CAD/USD forecast, housing market, commodity terms of trade.

**Output**:
```
OIL OUTLOOK: [Bullish/Neutral/Bearish] - [Price range]
KEY COMMODITIES: [Uptrend/downtrend]
CAD OUTLOOK: [Strengthening/Stable/Weakening]
HOUSING: [Correction/Stable/Recovery]
CANADA TAILWINDS: [List]
CANADA HEADWINDS: [List]
```

### [STAGE 0 SYNTHESIS]
```
=== MACRO REGIME SUMMARY ===
OVERALL REGIME: [Bull/Correction/Bear/Recovery]
RISK BUDGET: [Aggressive/Normal/Defensive]
TIME HORIZON BIAS: [Short-term (3-6mo) / Medium (6-18mo) / Long (18mo+)]
POSITION SIZING BIAS: [Larger/Normal/Smaller positions]

SECTOR FAVORABILITY RANKING:
1. [Sector] - [Why favorable]
2. [Sector] - [Why favorable]

SECTOR AVOIDANCE:
- [Sector] - [Why unfavorable]

KEY MACRO RISKS TO MONITOR:
- [Risk 1]: [Trigger to watch]
```

---

## STAGE 1: Trend Chain Discovery (Parallel Research)

**Objective**: Identify 10-15 macro investment trend chains across TWO TIME HORIZONS:
- **Immediate Trends (0-12 months)**: Already in motion, visible to market, may be mid/late innings
- **Emerging Trends (12-36 months)**: Early detection, pre-mainstream, positioning before crowd

For each trend, assess timing maturity and remaining runway. Avoid trend-following into late-stage dynamics unless clear undervalued nodes exist.

Map catalysts to second-, third-, fourth-order effects. Prioritize chains where Canada has structural advantage.


**Cross-reference each chain with Stage 0 regime assessment.**

**IMPORTANT**: The bullet points below are **TEMPLATES AND EXAMPLES ONLY**. Each subagent must spend significant time researching **CURRENT EMERGING TRENDS** from fresh sources (news, earnings calls, policy announcements, academic research, industry reports) rather than just analyzing these pre-listed examples. Discover what is actually happening NOW.

Launch the following subagents **simultaneously**:
### [SUBAGENT 1A] — Technology & Compute Trends
**Research BOTH time horizons:**

**Immediate (0-12mo) - assess if we're late:**
- AI infrastructure build-out → data centers → power demand
- Cloud migration maturity → optimization spend
- Cybersecurity escalation post-breaches

**Emerging (12-36mo) - early positioning:**
- AI agents/automation → labor displacement → retraining
- Quantum computing → cryptography disruption
- Edge AI → on-device inference → semiconductor shifts
- Synthetic biology → bio-manufacturing

⚠️ **TIMING CHECK**: For immediate trends, explicitly flag: Is the market narrative already saturated? Are valuations pricing in 3-5 years of growth already?
**Template examples (research current state of these AND find new ones):**
- AI compute demand → infrastructure → power → materials
- AI agents/automation → labor displacement → retraining
- Robotics → industrial automation → sensors → services
- Quantum computing → cryptography disruption
- Synthetic biology → bio-manufacturing → ag-tech → pharma

### [SUBAGENT 1B] — Geopolitical & Trade Trends
**Template examples (research current state of these AND find new ones):**
- U.S. isolationism → allied defense spend, tech sovereignty, reshoring
- U.S.-China decoupling → critical minerals, supply chain diversification
- De-dollarization/BRICS+ → gold, alternative payment rails
- Arctic sovereignty → Canadian northern infrastructure, shipping, resources
- Middle East instability → energy volatility → LNG, renewables
- EU strategic autonomy → defense, tech, energy independence

### [SUBAGENT 1C] — Demographic & Social Trends
**Template examples (research current state of these AND find new ones):**
- Aging population → healthcare, automation, wealth transfer, housing
- GLP-1/obesity drugs → downstream health impacts, disrupted industries
- Remote/hybrid work → suburban shift, cybersecurity, commercial RE decline
- Loneliness epidemic → pets, wellness, mental health platforms
- Immigration-driven growth (Canada) → housing, education, multicultural brands
- Cost of living crisis → discount retail, fintech, sharing economy

### [SUBAGENT 1D] — Energy, Climate & Resources Trends
**Research BOTH time horizons:**

**Immediate (0-12mo) - assess if we're late:**
- Nuclear/uranium restart → existing mine supply
- Battery metals demand → lithium/copper prices
- LNG infrastructure build-out

**Emerging (12-36mo) - early positioning:**
- SMRs (Small Modular Reactors) → regulatory approval
- Hydrogen economy → industrial adoption scale
- Carbon markets → compliance trading expansion
- Critical minerals → new mine development (7-10 year cycle)

⚠️ **TIMING CHECK**: Resource cycles are long. Mid-cycle ≠ late if supply response is constrained. Check inventory levels, project pipelines, substitution threats.
- Nuclear renaissance → uranium, SMRs, fuel services, grid modernization
- Climate adaptation → insurance repricing, wildfire tech, water infrastructure
- EV adoption → battery metals → recycling → charging infrastructure
- Hydrogen economy → electrolyzers, storage, industrial use
- Water scarcity → treatment tech, agricultural efficiency
- Carbon markets → carbon capture, offsets, trading platforms
- Canadian O&G transition → LNG exports, CCUS, petrochemicals

### [SUBAGENT 1E] — Space, Defense & Frontier Trends
- Space economy → satellite internet, earth observation, manufacturing
- Cybersecurity escalation → zero trust, identity management, OT security
- Defense modernization → drones, autonomous systems, cyber, space assets
- Digital infrastructure → fiber, 5G/6G, edge compute, undersea cables

### [SUBAGENT 1F] — Historical Pattern Matching
Research past macro cycles and identify which current trends rhyme:
- 1970s oil shock vs. 2020s energy shock
- 2000s China commodity supercycle vs. 2020s reshoring
- Post-2008 fintech vs. post-2023 AI fintech
- 1980s defense buildup vs. 2025+ NATO rebuild
- Dot-com → mobile → cloud → AI infrastructure winners

**Output for each**:
```
HISTORICAL PERIOD: [e.g., 1970s Oil Shock]
CURRENT ANALOG: [e.g., 2020s Energy Transition]
EARLY/MID/LATE WINNERS: [Stocks/sectors with % gains]
LOSERS: [What failed]
CURRENT EQUIVALENTS: [Map to current stocks]
KEY METRICS TO TRACK: [Transition signals]
```

### [SUBAGENT 1G] — Cross-Chain Correlation Analysis
```
CORRELATED CLUSTERS:
  Cluster A: [Chain 1, 3, 7] - [Why correlated]

HEDGE PAIRS:
  - [Chain A] hedges [Chain B] because: [reason]

SHARED NODES (Concentration Risk):
  - [Node X] appears in: [Chain 1, 3, 5]

RESOURCE CONFLICTS:
  - [Chain A] competes with [Chain B] for: [resource/capital/talent]
```

**Standard Chain Output Format** (INCLUDE TIMING ASSESSMENT):
```
CHAIN: [Name]
TIME HORIZON: [Immediate 0-12mo / Emerging 12-36mo]
CATALYST: [What triggers it]
MACRO ALIGNMENT: [Favored/Neutral/Disfavored - explain]
GRAPH: Node A → Node B → Node C
            ↘ Node D → Node E
STAGE: [Early/Mid/Late innings per node]
TIMING ASSESSMENT:
  - Market Awareness: [Mainstream/Early majority/Early adopters/Insiders only]
  - Price Action: [Already run X% / Building base / Just breaking out]
  - Valuation Status: [Pricing in Y years of growth]
  - Remaining Runway: [Specific catalysts not yet priced]
LATE-CYCLE CONSIDERATIONS:
  - If Late: [Why still valid (undervalued node, supply constraints, policy support)]
  - If Early: [Validation points needed to confirm thesis]
CANADIAN EDGE: [Yes/No + why]
PRICED IN: [Which nodes obvious vs. under-priced]
```

---

## STAGE 2: Stock Universe Generation (Parallel per Chain)

**Objective**: For each trend chain, generate 8-15 candidate stocks. **Canadian-listed preferred but not required** — will select best opportunities regardless of exchange.

**Wait for Stage 0 and Stage 1. Apply macro regime bias when selecting.**

### [SUBAGENT 2-{CHAIN_ID}] — Stock Universe for "{Chain Name}"

**Selection criteria**:
1. **Canadian-first preference**: Prioritize TSX/TSX-V listed when quality is comparable; do not exclude superior non-Canadian opportunities
2. **Best-in-class**: Include U.S./International when they dominate the node or no quality Canadian option exists
3. **Market cap mix**: Large (>$10B), mid ($2B-$10B), small (<$2B)
4. **Minimums**: $1 share price, $200M market cap (no penny stocks)
5. **Regime alignment**: Note Stage 0 favorability

**For each candidate**:
```
TICKER: [TSX: XXX or NYSE: XXX]
COMPANY: [Name]
MARKET CAP: [Approximate]
CHAIN NODE: [Which part of chain]
CANADIAN LISTED: [Yes/No]
REGIME FIT: [Favored/Neutral/Disfavored]
THESIS: [1 sentence]
RISK FLAG: [1 sentence]
DATA FRESHNESS: [Date]
```

**Also note**: ETFs for basket exposure, upcoming IPOs worth watching, insider ownership levels.

---

## STAGE 3: Individual Stock Deep Analysis (Massively Parallel)

**Objective**: For each candidate, run independent buy/pass analysis. Launch ALL stock analyses simultaneously.

**Wait for Stage 2. Then launch one subagent per stock.**

### [SUBAGENT 3-{TICKER}] — Deep Analysis: {Company Name}

**Context**: Trend chain `{Chain Name}`, macro regime `{Stage 0 synthesis}`

#### A. Business Quality (Score 1-10)
Revenue breakdown, competitive moat (pricing power, switching costs, network effects, regulatory barriers, IP), management quality (founder-led? insider ownership? capital allocation), pure-play vs. conglomerate (<20% trend exposure = conglomerate).

#### B. Financial Health (Score 1-10)
Revenue growth (3-year CAGR, recent quarter), profitability (gross/operating/FCF margins), balance sheet (net debt/EBITDA, current ratio, cash runway), ROIC vs. WACC, dividend profile if applicable. Flag data freshness.

#### C. Valuation (Score 1-10)
Current P/E, P/S, EV/EBITDA vs. 5-year average, relative vs. peers, PEG if growth, trend priced in?, DCF/sum-of-parts if applicable.

#### D. Trend Alignment & Timing (Score 1-10)
How directly benefits? % revenue tied to trend? Position in chain (early/mid/late node)? Catalysts next 6-12 months? Management commentary from earnings calls.

**⚠️ CRITICAL: Late-Cycle Assessment**
TREND TIMING ANALYSIS:
- Trend Stage: [1st/2nd/3rd = Early] [4th/5th/6th = Mid] [7th/8th/9th = Late]
- Price Performance vs. Trend: [Stock up X% while trend still early/mid/late]
- Market Narrative Saturation: [No one talks about it / Early buzz / Mainstream / Consensus]
- Valuation vs. Trend Maturity: [Pricing in 1yr/3yr/5yr+ of trend growth]
- Institutional Positioning: [Under-owned/Building/Peak ownership]

**LATE BUT STILL VALID CRITERIA (check at least 2):**
☐ Stock trades at discount to peers despite trend exposure
☐ Supply constraints prevent rapid competitive entry
☐ Regulatory/policy tailwinds extend runway
☐ Company is SECOND-DERIVATIVE play (not obvious first-order)
☐ Underlying trend has 5+ years of visibility

RUNWAY ASSESSMENT:
- Remaining Upside Catalysts: [List]
- Time to Peak Earnings: [Quarters/years]
- Trend Duration Estimate: [Temporary vs. secular]


#### E. Canadian Investor Considerations
TFSA/FHSA/RRSP eligibility, withholding tax if U.S.-listed, CAD/USD exposure, TSX liquidity (volume, spread), SEDI insider activity.

#### F. Risk Assessment
Top 3 risks, thesis invalidation triggers, correlation to other portfolio stocks, **REQUIRED: One strong bear case** (search for "why {TICKER} is overvalued").

#### G. Exit Criteria
- **Price Target**: Bull/Base/Bear (12-18 month)
- **Suggested Holding Period**: [Short-term (6-12mo) / Medium (1-2yr) / Long-term (2-5yr)] - based on catalyst visibility and trend maturity
- **Time Stop**: If no catalyst by [date, max 18 months from expected], reassess or exit
- **Thesis Invalidation Triggers**: [Specific events/metrics]
- **Stop Loss**: Core = Trailing stop X% from high; Satellite = Hard stop X% below entry
- **Take Profit**: Scale out at X% gain, full exit at Y%

#### H. Position Sizing
```
VOLATILITY: [30-60 day realized vol or ATR %]
RISK PER TRADE: 1-2% satellite, 2-3% core
STOP LOSS DISTANCE: X%

POSITION SIZE = (Portfolio × Risk%) / (Entry × Stop Loss%)

VOLATILITY ADJUSTMENT:
- High vol (>30% annual): Reduce 25%
- Low vol (<15% annual): Increase 25%
```

#### Final Verdict
```
TICKER: {Ticker}
COMPOSITE SCORE: [Avg of A-D: Business 30%, Financial 25%, Valuation 20%, Trend 25%]
REGIME ADJUSTMENT: [+/- 0.5 based on Stage 0]
VERDICT: [STRONG BUY / BUY / HOLD / PASS]
POSITION SIZE: [Core (3-5%) / Satellite (1-2%) / Watch List]
VOLATILITY-ADJUSTED SIZE: [From section H]
CONFIDENCE: [High/Medium/Low]
SUGGESTED HOLDING PERIOD: [Short/Medium/Long - with rationale]
KEY CATALYST: [Most important upcoming catalyst]
CATALYST DATE: [Expected timing]
ENTRY STRATEGY: [Buy now / Wait for pullback to $X / Wait for catalyst]
PRICE TARGETS: Bull $X / Base $Y / Bear $Z
STOP LOSS: $X or X% below entry
TIME STOP: [18 months from expected catalyst date, or specific date]
DATA FRESHNESS: [Date]
```

#### Thesis Tracking Template (for BUY/STRONG BUY)
```
## {TICKER} Thesis Tracker
**Entry Date**: [Date] | **Entry Price**: $X
**Suggested Holding Period**: [Short/Medium/Long]
**Thesis**: [1-2 sentences]
**Key Metrics**: [Metric]: Current [X], Target [Y] by [date]
**Catalyst Calendar**: [Date]: [Event]
**Validation Checkpoints**: [ ] [Checkpoint] - [Date]
**Bear Case**: [Key bear argument]
**Exit Triggers**: [ ] Price target | [ ] Stop loss | [ ] Thesis invalidation | [ ] Time stop
```

---

## STAGE 4: Portfolio Construction & Risk Management

**Wait for ALL Stage 3 analyses. Launch these subagents simultaneously:**

### [SUBAGENT 4A] — Portfolio Construction
From all STRONG BUY/BUY stocks:
1. Rank by composite score (descending)
2. Apply regime filter from Stage 0
3. **Chain allocation: 2-4 positions per chain based on conviction** (more for high-conviction, fewer for lower)
4. **Diversification**: Max 40% per sector (GICS L1) when conviction is high (25% default), mix of market caps, monitor correlation clusters
   - **Technology sub-sector limits**: Max 20% per sub-sector (SaaS, Cybersecurity, Semiconductors, E-commerce, Fintech, Gaming)
5. Build 15-25 position model portfolio
6. Apply volatility-adjusted sizing from Stage 3H
7. **Tax optimization**: Prioritize TFSA/FHSA/RRSP for rebalancing-heavy positions (no tax drag). Place buy-and-hold in taxable if advantageous.

**Output**:
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

### [SUBAGENT 4B] — Trend Timing & Risk Matrix
1. Innings assessment per chain (1st-3rd early, 4th-6th mid, 7th-9th late)
2. Kill switch per chain (scenario that invalidates thesis)
3. Correlation overview between chains (identify clusters)
4. Macro risk overlay (rates, recession, CAD/USD, oil scenarios)
5. Timeline: 6-month plays vs. 2-year holds vs. 5-year compounders

**Output**:
```
=== TREND TIMING MATRIX ===
| Trend Chain | Innings | Timeline | Kill Switch | Macro Sensitivity |

MACRO SCENARIO ANALYSIS:
- Bull: [Scenario] → Portfolio impact: [Estimate]
- Base: [Scenario] → Portfolio impact: [Estimate]
- Bear: [Scenario] → Portfolio impact: [Estimate]
```

### [SUBAGENT 4C] — ETF & Passive Alternatives
Map each chain to best Canadian/U.S. ETF, compare vs. active picks, suggest 5-8 ETF "lazy portfolio" capturing 80% of thesis, flag chains with no good ETF (alpha opportunity).

```
=== ETF MAPPING ===
| Trend Chain | Best CAD ETF | Best US ETF | Expense Ratio | Overlap |

LAZY PORTFOLIO: | ETF | Allocation | Thesis |
ALPHA OPPORTUNITIES: [Chains requiring stock-picking]
```

### [SUBAGENT 4D] — Watchlist & Catalyst Calendar
Compile HOLD/WATCH stocks with upgrade triggers. Build 12-month catalyst calendar. Flag Canadian policy decisions impacting chains.

```
=== WATCHLIST ===
| Ticker | Verdict | Upgrade Trigger | Target Buy Price |

=== CATALYST CALENDAR ===
[Month-by-month calendar]

CANADIAN POLICY EVENTS:
- [Date]: [Decision] - Impact: [Chains/stocks affected]
```

### [SUBAGENT 4E] — Risk Management Rules
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

## STAGE 5: Final Report Assembly

**Wait for Stage 4. Single agent synthesizes.**

### [FINAL AGENT] — Executive Summary & Report

Save as `{Date}_Investment_Research_Report.md` under ./reports:

1. **Executive Summary** (1 page): Top 5 conviction ideas, portfolio overview, key themes, macro regime
2. **Macro Regime Assessment**: From Stage 0
3. **Trend Chain Maps**: All chains as directed graphs with tickers mapped to nodes
4. **Top Picks Deep Dives**: 1 paragraph per stock (include suggested holding period)
5. **Model Portfolio**: From Stage 4A
6. **Risk Dashboard**: From Stage 4B
7. **Risk Management Rules**: From Stage 4E
8. **Passive Alternative**: From Stage 4C
9. **Watchlist & Calendar**: From Stage 4D
10. **Methodology Note**: Scores calculation, data sources, dates, caveats

**Canadian-Specific Section**:
- TFSA/FHSA/RRSP optimization
- Withholding tax for U.S. holdings
- CAD/USD hedging recommendation
- Canadian ETF alternatives
- Provincial/federal policy risks/opportunities

**Thesis Tracking Section**:
- Tracking template per BUY position (include holding period)
- Calendar reminders for catalysts and validation checkpoints

---

## Execution Notes

**Data freshness**: Use most recent data. Flag anything >30 days old. Include source and date.

**Bias check**: Each Stage 3 must include a strong bear case. Explicitly search for "why {Ticker} is overvalued."

**Iteration**: If portfolio too concentrated or missing chains, loop to Stage 2 for under-represented chains.

**Regime sensitivity**: If Stage 0 macro changes significantly (recession starts, rate shift), re-run the framework.

**Canadian-First Philosophy**: Prioritize Canadian-listed stocks when quality is comparable, but do not compromise returns for geography. The framework aims to capture global opportunities while favoring Canadian structural advantages (commodities, uranium, financials, energy transition).