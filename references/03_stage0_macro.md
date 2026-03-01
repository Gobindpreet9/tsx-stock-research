# Stage 0 — Macro Regime Assessment

> **Reference for**: `[SUBAGENT 0A]`, `[SUBAGENT 0B]`, `[SUBAGENT 0C]`, `[SUBAGENT 0D]`

---

## Objective

Classify current market regime before trend analysis. This sets risk appetite and sector bias for all subsequent stages.

**Launch these subagents simultaneously**.

---

## Subagent Assignments

### [SUBAGENT 0A] — Interest Rate & Credit Analysis

**Analyze**:
- Central bank policy rates (BoC, Fed)
- Yield curve shape (2s10s, 3m10s)
- Credit spreads (IG, HY)
- Real interest rates

**Output Format**:
```
RATE ENVIRONMENT: [Restrictive/Neutral/Accommodative]
YIELD CURVE: [Inverted/Normal/Steepening]
CREDIT CONDITIONS: [Tightening/Stable/Easing]
RATE TRAJECTORY: [Cutting/Pausing/Hiking]
IMPLICATIONS: [Which sectors win/lose]
```

---

### [SUBAGENT 0B] — Economic Cycle Positioning

**Assess**:
- Leading indicators (PMI, permits, claims)
- Coincident indicators (GDP, employment, IP)
- Lagging indicators (inflation, unemployment)
- Recession probability models

**Output Format**:
```
CYCLE STAGE: [Early/Mid/Late Expansion/Recession/Recovery]
RECESSION PROBABILITY: [X%] over next 12 months
KEY LEADING INDICATORS: [Trending up/down/flat]
CYCLE IMPLICATIONS: [Favor growth/value/defensive/quality]
```

---

### [SUBAGENT 0C] — Market Regime Classification

**Analyze**:
- S&P 500 and TSX trend (50/200-day MA)
- Volatility regime (VIX)
- Sector rotation
- Risk-on/off indicators (HY spreads, copper/gold)
- CAD/USD trends

**Output Format**:
```
MARKET REGIME: [Bull/Bear/Sideways/Transition]
VOLATILITY REGIME: [Low/Normal/Elevated/Crisis]
RISK APPETITE: [Risk-On/Risk-Off/Mixed]
SECTOR LEADERS: [Top 3 sectors last 3-6 months]
STYLE FAVORABILITY: [Growth/Value/Quality/Momentum/Small-cap]
```

---

### [SUBAGENT 0D] — Commodity & Currency Outlook (Canada Focus)

**Analyze Canada-specific factors**:
- Oil & gas (WTI, WCS, nat gas)
- Key metals (copper, lithium, uranium, gold)
- CAD/USD forecast
- Housing market
- Commodity terms of trade

**Output Format**:
```
OIL OUTLOOK: [Bullish/Neutral/Bearish] - [Price range]
KEY COMMODITIES: [Uptrend/downtrend]
CAD OUTLOOK: [Strengthening/Stable/Weakening]
HOUSING: [Correction/Stable/Recovery]
CANADA TAILWINDS: [List]
CANADA HEADWINDS: [List]
```

---

## Stage 0 Synthesis

**Combine all outputs into**:

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

## Data Sources

See `references/01_data_sources.md` for required data sources.
