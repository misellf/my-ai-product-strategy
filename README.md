# Your Role: Product Manager and AI Product Strategy Lead

> Product leaders will make faster, more confident prioritization decisions when AI automatically validates hypotheses and synthesizes organizational signals into strategic recommendations.

---

## Strategy at a Glance

| Component | Module | Status | Key Artifact |
|---|---|---|---|
| **The Bet** | M1 | [x] | `01-the-bet/` |
| **The Moat** | M2 | [x] | `02-the-moat/` |
| **The Margin** | M3 | [x] | `03-the-margin/` |
| **The Contract** | M4 | [x] | `04-the-contract/` |
| **The Guardrails** | M5 | [x] | `05-the-guardrails/` |
| **The Pitch** | M6 | [x] | `06-the-pitch/` |

---

## The Bet (M1)

**What we're building, for whom, and why now.**

- **Product:** ProdPriority — an AI Oracle and Copilot that helps Product Managers and Chief Product Officers validate hypotheses, synthesize organizational evidence, and make better prioritization decisions.
- **AI Value Archetype:** Oracle / Copilot. The AI analyzes organizational data, validates assumptions, identifies themes, and recommends priorities aligned with business strategy.
- **Vulnerability Scores:** Contextual Moat 2/5 · Data Advantage 5/5 · Platform Exposure 2/5
- **Top Risk:** Weak workflow integration and exposure to AI platforms or enterprise data providers that could reproduce the core recommendation experience.
- **Confidence:** High
- **Prototype:** http://localhost:8080
- **Kill Criteria:** If the AI cannot consistently generate actionable, trustworthy insights that improve prioritization decisions, or if product leaders do not adopt the recommendations as part of their decision-making process, the product should be discontinued.

→ Details: [`01-the-bet/`](01-the-bet/)

---

## The Moat (M2)

**Why this won't get copied in six months.**

- **Data Flywheel Score:** 15/20
- **Weakest Loop:** Correction, Network, and Domain Context loops
- **Competitive Position:** Strong potential data advantage but currently limited workflow depth and switching costs. The product becomes defensible when recommendations, human decisions, and realized business outcomes are connected.
- **Top Encroachment Threat:** OpenAI, with Palantir and Productboard as vertical and adjacent threats.
- **Encroachment Defense:** Build a proprietary decision-outcome dataset, integrate deeply into product-management workflows, connect cross-functional organizational evidence, provide source-level traceability, and support multiple model providers.
- **Vendor Portability:** Locked — the current implementation depends on Claude, although a generic interface provides a starting point for multi-provider support.

→ Details: [`02-the-moat/`](02-the-moat/)

---

## The Margin (M3)

**Will this make money or bleed it?**

- **Gross Margin (current):** 88.0% under the traditional SaaS model
- **Gross Margin (AI-adjusted):** 79.8%
- **Pricing Model:** Outcome-based pricing using resolved conversations
- **Pricing Today → Tomorrow:** $100 per seat per month → $35 per resolved outcome, with an estimated four outcomes per user per month
- **Implied Revenue:** $140 per user per month
- **Total AI COGS / unit:** $6.56 per resolved outcome, or $26.25 per user per month
- **Total COGS:** $28.25 per user per month, including $2 of non-AI COGS
- **Cascading Strategy:** Triage: mid-tier, medium-cost model; frontier: advanced reasoning model; ratio 60%/40%
- **Net Margin Shift:** −8.2 percentage points, but +$23.75 in gross profit per user per month
- **Break-even at:** 0.81 resolved outcomes per user per month; operationally, at least 1 resolved outcome per user per month

→ Details: [`03-the-margin/`](03-the-margin/)

---

## The Contract (M4)

**Why users will trust a probabilistic system.**

- **Reliability Target:** 95% golden-dataset accuracy
- **Hallucination Target:** Less than 1%
- **Golden Dataset:** 10 rows, 3 adversarial
- **Confidence UX:** Show uncertainty using tiered confidence, evidence citations, qualified language, missing-evidence prompts, and human escalation.
- **HITL Trigger:** Route an output to human review when confidence is below the approved threshold, evidence is missing or contradictory, the decision is high-risk or high-value, the user flags the output, or a reliability threshold is breached.
- **HITL Reviewer:** Accountable Product Manager or product leader, supported by Engineering, Architecture, Data, Risk, Finance, or Customer Experience when specialist review is required.
- **Feedback Loop:** Capture corrections, overrides, rationales, and supporting evidence as structured feedback. Use validated feedback to improve evaluation cases, prompts, routing, confidence calibration, and model configuration.
- **Failure Mode Coverage:** A recommendation can be factually grounded but still wrong because its sources are outdated, incomplete, duplicated, strategically manipulated, or missing important cross-functional evidence.
- **Ship Requirement:** No ship-blocking rule violations, an average LLM-judge score of at least 4/5, and evidence-grounding and transparency scores of at least 4/5.

→ Details: [`04-the-contract/`](04-the-contract/)

---

## The Guardrails (M5)

**What breaks when this scales, and what compounds.**

- **Compounding System:** The intended advantage is a recommendation → decision → outcome learning loop. The current recursive-learning loop is broken, while cross-domain transfer and network intelligence are still missing.
- **Compounding Fix:** Assign every recommendation a decision ID, capture whether it was accepted, changed, or rejected, record the rationale, connect the decision to business outcomes, and feed validated results back into evaluations and future recommendations.
- **Governance Posture:** Human-accountable, evidence-grounded, risk-based, least-privilege, and advisory. ProdPriority supports decisions but does not make or execute final investment decisions.
- **Autonomy Boundaries:** The AI may retrieve approved data, synthesize evidence, identify contradictions, assess hypotheses, compare opportunities, cite sources, and draft recommendations. Humans must approve priorities, funding, roadmap changes, high-risk decisions, external communications, and policy exceptions.
- **Escalation Triggers:** Low confidence; missing, outdated, contradictory, or untraceable evidence; sensitive data; material financial, customer, security, regulatory, or reputational risk; user challenge; prompt injection; or a reliability-threshold breach.
- **Audit Cadence:** Real-time security monitoring · daily alert review · weekly review of escalations and overrides · monthly reliability and drift review · quarterly governance and regulatory review
- **Shadow AI Audit:** 8 workarounds identified · 6 build candidates · 6 tools found and 5 retained after triage · estimated adjacent spend of $200/team/month
- **Agent Boundaries:** Retrieval agents can only access approved sources; synthesis agents cannot fabricate or suppress evidence; prioritization agents cannot approve funding or change roadmaps; safety agents can trigger escalation but cannot approve their own exceptions.
- **Regulatory Exposure:** Canadian privacy requirements, GDPR when EU personal data is processed, the EU AI Act when applicable, organizational security and records-management policies, and relevant sector-specific requirements.
- **Risk Tier:** Provisionally limited, provided ProdPriority remains an internal advisory system and does not make regulated decisions about individuals.

→ Details: [`05-the-guardrails/`](05-the-guardrails/)

---

## The Pitch (M6)

**How you get this funded, shipped, and adopted.**

- **Horizon 1 — Now (0–3 months):** Establish trust through source citations, tiered confidence, golden-dataset evaluation, human review, decision logging, and a controlled pilot with Product Managers and product leaders.
- **Horizon 2 — Next (3–9 months):** Integrate Jira, Confluence, customer feedback, analytics, support, CRM, strategy, and financial data. Connect recommendations to accepted, rejected, or changed decisions and their outcomes.
- **Horizon 3 — Bet (9–18 months):** Create cross-domain learning and anonymized network intelligence that identifies recurring opportunity patterns, improves confidence calibration, and produces organization-wide prioritization benchmarks.
- **Board Narrative:** ProdPriority reduces costly product-investment uncertainty by turning fragmented organizational evidence into transparent recommendations and learning from which decisions produce measurable business outcomes.
- **The Case:**
  1. **Why now:** Product leaders face growing volumes of fragmented customer, delivery, market, and business data while being expected to make faster investment decisions.
  2. **What is defensible:** Proprietary organizational context and a closed decision-outcome loop that general-purpose AI platforms cannot reproduce without access to the same evidence and outcomes.
  3. **The economics:** The AI model generates $140 in monthly revenue and $111.75 in gross profit per user, despite reducing gross margin percentage from 88.0% to 79.8%.
- **The Risks:**
  1. **Trust and failure modes:** Hallucinations, stale evidence, unsupported confidence, source manipulation, and inconsistent recommendations.
  2. **Scale and governance:** Sensitive-data exposure, uncontrolled integrations, model drift, cost growth, and unclear decision accountability.
  3. **Competitive:** OpenAI, Palantir, Productboard, or another enterprise platform could reproduce the visible recommendation experience.
- **The Ask:** Approve a 90-day controlled pilot with 3–5 product teams and dedicated Product, Engineering, Data, Security, and Risk support. Measure recommendation adoption, decision-cycle time, evaluation accuracy, user trust, and evidence of avoided or redirected low-value investment.
- **Key Metric:** Percentage of prioritization decisions improved or accelerated by an evidence-grounded ProdPriority recommendation.
- **M1 Baseline:** Product leaders will make faster, more confident prioritization decisions when AI automatically validates hypotheses and synthesizes organizational signals into strategic recommendations.
- **Now:** ProdPriority is a governed decision-intelligence system that connects organizational evidence to transparent recommendations, preserves human accountability, and learns which product-investment decisions generate measurable outcomes.
- **Key Strategic Change:** The strategy has evolved from building an AI prioritization assistant to creating a proprietary decision-learning system whose defensibility comes from evidence traceability, workflow integration, and the recommendation-to-outcome feedback loop.

→ Details: [`06-the-pitch/`](06-the-pitch/)
