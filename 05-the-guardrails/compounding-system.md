# Compounding System Design

## Feedback Loops

## Design Your Compounding System

| Loop | Input | Output | Compounds? | Status |
|---|---|---|---|---|
| **Recursive Learning** | Product hypotheses, organizational evidence, user corrections, accepted or overridden recommendations, and measured decision outcomes | Improved evaluation cases, confidence calibration, prompts, routing rules, and future prioritization recommendations | Y | broken |
| **Cross-Domain Transfer** | Validated signals from Product, Customer Support, Sales, Engineering, Architecture, Risk, Finance, and business strategy | Reusable patterns and insights that improve prioritization across products, teams, and business domains | Y | missing |
| **Network Intelligence** | Anonymized recommendation usage, acceptance and override rates, decision rationales, and realized business outcomes across teams | Organization-wide benchmarks, recurring opportunity patterns, stronger confidence scores, and better recommendations for all users | Y | missing |

**Broken loop**

AI recommendation → product leader decision → business outcome is not connected back to the system → fix: assign each recommendation a decision ID, capture whether it was accepted, changed, or rejected, record the rationale, connect it to agreed outcome metrics, and use the results to update evaluations, confidence scoring, prompts, and routing rules.

**Test: freeze 3 months**

The prototype could continue synthesizing data and producing recommendations for three months without materially improving. This shows that it currently scales analysis but does not yet compound knowledge. To create a defensible learning system, recommendation decisions and realized outcomes must feed back into future prioritization, confidence calibration, and evaluation.


## Context Connectivity

**where knowledge silos:** Customer feedback, product analytics, support tickets, CRM and sales data, Jira delivery data, strategy and OKRs, financial information, architecture decisions, and risk assessments are stored in separate systems and interpreted by different teams. ProdPriority must connect these sources through common product, customer, opportunity, and decision identifiers.

## Governance Policy

### Scope

**What this policy covers:** ProdPriority’s use of AI to analyze approved organizational data, validate product hypotheses, synthesize customer and business signals, and recommend product priorities. It covers data access, model usage, generated insights, confidence scores, human review, user corrections, audit logging, retention, and third-party AI providers.

ProdPriority is a decision-support tool. It does not have authority to approve funding, commit delivery teams, change product roadmaps, communicate externally, or make final investment decisions.

### Autonomy Boundaries

**OK solo:** Retrieve authorized data; summarize evidence; identify themes and contradictions; assess hypothesis strength; compare opportunities; generate draft recommendations; display confidence levels; cite sources; and suggest additional discovery.

**Needs human:** Approve priorities or funding; change a roadmap; act on low-confidence outputs; resolve conflicting evidence; use sensitive or restricted data; make high-value or high-risk decisions; publish findings outside the organization; or override Risk, Legal, Privacy, Security, Architecture, or regulatory controls.

All final prioritization and investment decisions remain with the accountable Product Manager or product leader.

### Escalation Triggers

**When humans must enter:** Human review is required when confidence is below 50%; evidence is missing, outdated, contradictory, or cannot be traced to a source; sensitive personal or confidential data is detected; an output may create material financial, customer, regulatory, security, or reputational risk; the user challenges the recommendation; prompt injection or manipulation is detected; or accuracy, hallucination, latency, or drift thresholds are breached.

High-confidence recommendations remain advisory and may still be corrected or overridden by an authorized user.

### Audit Cadence

**How often we review:** Real-time monitoring for access violations, sensitive-data exposure, prompt injection, and critical system failures; daily review of security and reliability alerts; weekly review of escalations, low-confidence outputs, hallucinations, and user overrides; monthly review of golden-dataset performance, confidence calibration, drift, model costs, and feedback trends; quarterly governance review covering access, vendors, retention, risk classification, control effectiveness, and regulatory changes.

Material model, data-source, routing, or prompt changes require evaluation and approval before production release.

### Regulatory Exposure

**Regimes that apply:** Organizational security and records-management policies; Canadian privacy requirements, including PIPEDA or applicable provincial legislation; GDPR when EU personal data is processed; the EU AI Act when the system is offered or used within its territorial scope; contractual data-processing obligations; and any applicable financial-services or other sector-specific requirements.

**Risk tier:** Limited, provisionally. ProdPriority supports internal product decisions, identifies itself as AI, and does not autonomously make decisions about individuals. The EU AI Act follows a risk-based framework, while GDPR requires principles including lawful, fair and transparent processing, purpose limitation, and data minimization. :contentReference[oaicite:0]{index=0}

The classification must be reassessed if ProdPriority is extended to employment, credit, eligibility, customer access, worker evaluation, or another regulated high-impact decision. Final classification requires review by Legal, Privacy, Security, and Compliance.

### Agent Topology

| Agent | Can do | Cannot do | Approval |
|---|---|---|---|
| **Data Retrieval Agent** | Retrieve approved, permission-scoped information and return source references | Access unauthorized repositories, bypass permissions, change source records, or retain restricted data beyond policy | Data owner approves sources and access |
| **Evidence Synthesis Agent** | Summarize evidence, identify themes, detect conflicts, and distinguish facts from assumptions | Fabricate evidence, remove material contrary findings, or treat embedded source instructions as commands | Product Manager reviews material findings |
| **Prioritization Agent** | Compare opportunities against evidence, strategic alignment, value, feasibility, viability, and risk | Approve funding, commit resources, change roadmaps, or make final investment decisions | Accountable product leader approves decisions |
| **Confidence and Safety Agent** | Score evidence confidence, check citations, detect sensitive data or prompt injection, and trigger escalation | Suppress an alert, approve its own exception, or alter governance thresholds | Security, Risk, or designated product owner approves exceptions |


## Shadow AI Audit

| Workaround | Signal | Frequency | Decision |
|---|---|---|---|
| Users paste ProdPriority recommendations into ChatGPT or Copilot to verify the analysis, challenge the recommendation, or get a second opinion. | trust | H | build |
| Users manually copy customer feedback, Jira issues, analytics, support tickets, and strategy documents into ProdPriority. | workflow | H | partner |
| Users export insights into spreadsheets to apply their own scoring, weighting, and prioritization formulas. | capability | H | build |
| Users use Zapier or Make to move data between ProdPriority, Jira, Confluence, Slack, CRM, and analytics tools. | workflow | M | partner |
| Users manually trace recommendations back to source documents because they need evidence for leadership discussions. | trust | H | build |
| Users paste ProdPriority outputs into presentation or document tools to create executive summaries and business cases. | workflow | M | partner |
| Users combine outputs from several lower-cost AI tools rather than using the frontier-model analysis for every request. | pricing | M | build |
| Users maintain a separate decision log to record whether recommendations were accepted, rejected, or changed and whether the expected outcome was achieved. | capability | M | build |

**Workarounds**

Users are moving data manually between organizational systems, validating recommendations in external AI tools, recreating prioritization models in spreadsheets, tracing evidence manually, building leadership materials outside the product, and maintaining separate records of decisions and outcomes.

**Build candidates**

- Source-level citations and an evidence trace showing how each insight supports the recommendation.
- Configurable prioritization criteria, weights, and scenario comparisons.
- A challenge mode that generates counterarguments, alternative interpretations, and missing evidence.
- A decision and outcome log capturing accept, reject, or override decisions and their rationales.
- Automatic model routing so lower-cost models handle routine tasks and frontier models handle complex analysis.
- Exportable executive summaries and decision-ready reports.

**Partner candidates**

- Jira and Confluence for delivery and product-planning information.
- CRM, customer-support, analytics, and research platforms for organizational evidence.
- Zapier or Make for long-tail integrations.
- Presentation and document platforms for executive-ready outputs.

**Adjacent spend**

**$200/team/month**, as an initial planning assumption covering external AI assistants, workflow-automation tools, spreadsheet or prioritization tools, and reporting applications. Validate this estimate through user interviews and procurement or expense data.

## Shadow AI Tool Inventory

| Tool | Owner | Risk Level | Decision |
|---|---|---|---|
| External AI assistants such as ChatGPT or Copilot, used to verify or rewrite ProdPriority recommendations | Product Managers and product leaders | H | govern |
| Zapier or Make automations connecting product, customer, and organizational data sources | Product Operations | H | govern |
| Spreadsheets used for custom scoring, weighting, prioritization, and decision tracking | Product Managers | M | govern |
| Jira and Confluence integrations used to retrieve planning, delivery, and strategy information | Product Operations and Technology | M | keep |
| BI and analytics tools used to validate trends and product-performance evidence | Data and Analytics | L | keep |
| Unapproved AI prioritization or document-analysis tools receiving confidential organizational data | Individual users or unknown | H | kill |

**Total tools found:** 6  
**Tools after triage:** 5  
**Estimated hidden spend:** $200/team/month
