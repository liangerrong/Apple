# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is an equity research workspace for Apple (AAPL). It is not a software project — there is no build system, tests, or source code.

## Workflow Protocol

All research must strictly follow `Deep Research_simplified_EN.md`. Key rules:

- **Output directory**: All files go into `RESEARCH/[project_name]/` — never write research files to the root
- **File size limit**: No single markdown file may exceed ~1,500 lines
- **Task tracking**: Use TodoWrite/TodoRead from the start of every research session
- **Evidence standard**: No assertion without a source; C1 critical assertions require ≥2 independent sources from different independence groups

## Folder Convention

```
RESEARCH/[project_name]/
  00_research_contract.md      # Lock scope before starting
  01_research_plan.md          # Sub-questions + query plan
  02_query_log.csv             # Every query run (timestamped)
  03_source_catalog.csv        # All sources with quality ratings
  03b_alt_data_log.md          # Grassroots / alternative data
  04_evidence_ledger.csv       # All assertions with verification_status
  05_contradictions_log.md     # Conflicts + resolution
  06_key_metrics.csv           # C1 figures with source_id (auditable)
  07_working_notes/            # Synthesis notes + Red Team arbitration table
  08_report/                   # 10-section report §00–§09
  09_qa/                       # Citation, numeric, and scope audits
  10_graph/                    # graph_state.json + graph_trace.md
```

## Tool Usage

- **NotebookLM MCP**: Retriever only — answers reflect what is in loaded files, not external facts. Confirm which files are loaded before querying. Session ID must be preserved across follow-up questions.
- **Tavily Search**: Primary source for competitive data, market share, analyst estimates, regulatory news, and alt data.
- **A-share MCP**: Excluded — does not cover US stocks.

## Assertion Tiers

| Tier | Rule |
|------|------|
| C1 Critical | ≥2 independent sources required; covers revenue, margins, market share, ROIC, causal conclusions |
| C2 Supporting | Industry trends, analyst estimates, qualitative assessments |
| C3 Background | Definitions, common knowledge |

## Report Structure (§00–§09)

Every research project produces these sections in `08_report/`:
`00_executive_summary` · `01_company_scope` · `02_business_breakdown` · `03_bmc` · `04_competitive_landscape` · `05_moat_sustainability` · `06_outlook_valuation` · `07_risks` · `08_red_team` · `09_references`

Each section ends with the **Impact Analysis Engine**: So What / Now What / What If / Compared To.

## Red Team (Phase 5B)

- Must use `equity-red-team` subagent — same context that wrote §01–§07 cannot self-challenge
- Subagent reads **only** raw data files (`06_key_metrics.csv`, `04_evidence_ledger.csv`, `10_graph/graph_state.json`, `03b_alt_data_log.md`, `05_contradictions_log.md`)
- Must produce ≥3 rebuttals; severity: OVERTHROWS / SIGNIFICANTLY WEAKENS / RAISES DOUBT
- Phase 5C arbitration (main conversation): Accept / Partial Accept / Reject; Reject requires ≥2 counter-evidence items

## Existing Research

- `RESEARCH/Apple_2026/` — Apple AAPL initiating coverage, FY2025 actuals, completed April 2026. All 7 phases complete; QA passed.
