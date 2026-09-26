# Compounding System Design

## Feedback Loops

## Design Your Compounding System

| Loop | Input | Output | Compounds? | Status |
|---|---|---|---|---|
| **Recursive Learning** | Product hypotheses, organizational evidence, user corrections, accepted or overridden recommendations, and measured decision outcomes | Improved evaluation cases, confidence calibration, prompts, routing rules, and future prioritization recommendations | Y | broken |
| **Cross-Domain Transfer** | Validated signals from Product, Customer Support, Sales, Engineering, Architecture, Risk, Finance, and business strategy | Reusable patterns and insights that improve prioritization across products, teams, and business domains | Y | missing |
| **Network Intelligence** | Anonymized recommendation usage, acceptance and override rates, decision rationales, and realized business outcomes across teams | Organization-wide benchmarks, recurring opportunity patterns, stronger confidence scores, and better recommendations for all users | Y | missing |

**Broken loop (partner found)**

AI recommendation → product leader decision → business outcome is not connected back to the system → fix: assign each recommendation a decision ID, capture whether it was accepted, changed, or rejected, record the rationale, connect it to agreed outcome metrics, and use the results to update evaluations, confidence scoring, prompts, and routing rules.

**Test: freeze 3 months (≈one frontier cycle), still win? If yes, you're not compounding.**

**Current answer: Yes.** The prototype could continue synthesizing data and producing recommendations for three months without materially improving. This shows that it currently scales analysis but does not yet compound knowledge. To create a defensible learning system, recommendation decisions and realized outcomes must feed back into future prioritization, confidence calibration, and evaluation.


## Context Connectivity

**where knowledge silos:** Customer feedback, product analytics, support tickets, CRM and sales data, Jira delivery data, strategy and OKRs, financial information, architecture decisions, and risk assessments are stored in separate systems and interpreted by different teams. ProdPriority must connect these sources through common product, customer, opportunity, and decision identifiers.

## Governance Policy

**Scope:**
**Autonomy boundaries:**
**Escalation triggers:**
**Audit cadence:**
**Regulatory exposure (EU AI Act / other):**

## Agent Topology
<!-- If using agents: what can each agent do? What can't it do? Who approves what? -->

## Shadow AI Audit

| Tool | Owner | Risk Level | Decision |
|------|-------|-----------|----------|
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |

**Total tools found:**
**Tools after triage:**
**Estimated hidden spend:**
