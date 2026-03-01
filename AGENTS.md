# Investment Research Framework — Main Orchestration

> **Usage**: This is the main orchestration prompt. Subagents should read relevant reference files from `./references/` directory.
>
> **Framework Version**: 2.0 (Modular)
>
> **Last Updated**: March 2026

---

## Overview

Multi-stage parallelized investment trend research framework focused on Canadian (TSX) stocks with global opportunity capture.

**5 Stages**:
1. **Stage 0**: Macro Regime Assessment (4 parallel subagents)
2. **Stage 1**: Trend Chain Discovery (7 parallel subagents)
3. **Stage 2**: Stock Universe Generation (per chain)
4. **Stage 3**: Individual Stock Deep Analysis (per stock)
5. **Stage 4**: Portfolio Construction & Risk Management (5 subagents)
6. **Stage 5**: Final Report Assembly (synthesis)

---

## Reference Files (Subagents Read These)

| File | For Subagents |
|------|---------------|
| `references/01_data_sources.md` | **ALL** - Required data sources |
| `references/02_framework_principles.md` | **ALL** - Critical thinking protocols |
| `references/03_stage0_macro.md` | 0A, 0B, 0C, 0D |
| `references/04_stage1_trends.md` | 1A-1G |
| `references/05_stage2_stocks.md` | 2-{CHAIN_ID} |
| `references/06_stage3_analysis.md` | 3-{TICKER} |
| `references/07_stage4_portfolio.md` | 4A-4E |
| `references/08_stage5_report.md` | FINAL AGENT |

---

## Execution Flow

```
┌─────────────────────────────────────────────────────────────┐
│ STAGE 0: Macro Regime Assessment                            │
│ Subagents: 0A, 0B, 0C, 0D (SIMULTANEOUS)                    │
└─────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────┐
│ STAGE 1: Trend Chain Discovery                              │
│ Subagents: 1A, 1B, 1C, 1D, 1E, 1F, 1G (SIMULTANEOUS)        │
└─────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────┐
│ STAGE 2: Stock Universe Generation                          │
│ Subagents: 2-{CHAIN_ID} (per chain, SIMULTANEOUS)           │
└─────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────┐
│ STAGE 3: Individual Stock Deep Analysis                     │
│ Subagents: 3-{TICKER} (per stock, MASSIVELY PARALLEL)       │
└─────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────┐
│ STAGE 4: Portfolio Construction & Risk Management           │
│ Subagents: 4A, 4B, 4C, 4D, 4E (SIMULTANEOUS)                │
└─────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────┐
│ STAGE 5: Final Report Assembly                              │
│ Subagent: FINAL AGENT (SYNTHESIS)                           │
└─────────────────────────────────────────────────────────────┘
```

---

## Key Principles

### 1. Parallel Execution

- **Default**: All subagents within a stage run **simultaneously**
- **Exception**: Stages must wait for previous stage completion

### 2. Canadian-First Philosophy

Prioritize Canadian-listed stocks when quality is comparable, but **do not compromise returns for geography**. Capture global opportunities while favoring Canadian structural advantages (commodities, uranium, financials, energy transition).

### 3. Data Freshness

**Flag any data >30 days old**. Include source and date for all data points.

### 4. Bias Checks

- Each Stage 3 analysis **MUST** include a strong bear case
- Search for "why {TICKER} is overvalued"
- Apply all 5 critical thinking protocols from `references/02_framework_principles.md`

### 5. Iteration

- If portfolio too concentrated or missing chains → loop to Stage 2
- If Stage 0 macro changes significantly → re-run framework
- Cross-cutting validation at each stage gate

---

## Main Agent Responsibilities

1. **Orchestrate** the 5-stage flow
2. **Launch** subagents in parallel within each stage
3. **Collect** and synthesize outputs
4. **Validate** completion criteria before proceeding
5. **Assemble** final report in Stage 5

---

## Success Criteria

**Report Complete When**:
- [ ] All trend chains identified (10-15)
- [ ] Stock universe generated (8-15 per chain)
- [ ] Individual analysis complete (all candidates)
- [ ] Model portfolio constructed (15-25 positions)
- [ ] Risk management rules defined
- [ ] Canadian-specific section included
- [ ] Thesis tracking templates created

---

## Report Management

**Location**: `./reports/`

**Naming**: `{Date}_Investment_Research_Report.md`

**Retention**: Maximum 10 most recent reports

---

## Version History

- **v2.0** (Mar 2026): Modular structure with reference files
- **v1.0** (Feb 2026): Initial monolithic prompt

---

**Begin by reading**: `references/01_data_sources.md` and `references/02_framework_principles.md`
