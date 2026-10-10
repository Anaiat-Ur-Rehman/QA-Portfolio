# Computer-Using Agent (CUA) & LLM Evaluation Report

## Project Overview
- **Evaluation Focus:** Computer-Using Agent (CUA) Multi-Turn Trajectory Auditing
- **Environment:** Multi-Application Workflows (Browser, Workspace, Terminal)
- **Evaluator:** Anaiat Ur Rehman
- **Date:** October 2026

## Evaluation Scope & Key Metrics

| Metric Category | Target Criteria | Evaluated Tasks | Pass Rate |
| :--- | :--- | :--- | :--- |
| **Instruction Following** | Strict adherence to multi-step prompt constraints | 15 | 93.3% |
| **Trajectory Efficiency** | Minimal redundant actions in tool calls / UI clicks | 15 | 86.7% |
| **Safety & Alignment** | Zero unauthorized actions or unsafe system modifications | 15 | 100% |
| **Ground Truth Accuracy** | Factually correct end-state outputs and data extraction | 15 | 93.3% |

## Trajectory Audit Example

### Task Scenario:
"Extract Q3 financial data from a PDF attachment, populate a spreadsheet, and send a summary draft email."

### Observed Agent Trajectory:
1. **Step 1:** Downloaded PDF attachment and extracted numeric tables. *(Success)*
2. **Step 2:** Formatted extracted data into CSV structure. *(Success)*
3. **Step 3:** Attempted email draft creation before populating spreadsheet. *(Sequence Error)*

### Audit Finding:
- **Issue Type:** Workflow Sequence Deviation
- **Severity:** Medium
- **Root Cause:** Agent prioritized final output task prior to intermediate verification step.
- **Remediation / Prompt Refinement:** Adjusted step-by-step constraint ordering to enforce strict dependency checking.

## Final Quality Summary
The target CUA model displays high baseline capability in direct UI/Workspace interaction. Task completion accuracy is high (93.3%), with primary failure modes stemming from action sequence optimization rather than execution capability.
