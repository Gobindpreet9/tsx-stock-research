# TSX Stock Research Framework

A multi-stage parallelized investment trend research framework focused on Canadian (TSX) stocks.

## Overview

This framework conducts comprehensive macro and micro analysis to generate investment recommendations. It uses parallel subagents to research:

- **Stage 0**: Macro Regime Assessment (rates, economic cycle, market regime, commodities)
- **Stage 1**: Trend Chain Discovery (technology, geopolitics, demographics, energy, defense)
- **Stage 2**: Stock Universe Generation (8-15 candidates per trend)
- **Stage 3**: Individual Stock Deep Analysis (scores, valuation, risk assessment)
- **Stage 4**: Portfolio Construction & Risk Management
- **Stage 5**: Final Report Assembly

## Report Management

- **Maximum Reports**: 10 most recent reports kept in `./reports/`
- **Rotation Policy**: When creating a new report, oldest is deleted if limit reached
- **Naming Convention**: `YYYY-MM-DD_Investment_Research_Report.md`

## Usage

Feed `AGENTS.md` to an AI system with parallel execution capabilities. Each `[SUBAGENT]` block runs independently.

## Latest Report

See [`reports/`](./reports/) for the most recent investment research.

## Disclaimer

This framework is for informational purposes only and does not constitute investment advice. All investments carry risk, including loss of principal.

---

*Framework Date: February 2026*
