# Three-Horizon Roadmap & Board Pitch

## Roadmap

### Horizon 1, Ship (0–4 weeks)

| Initiative | Strategy Component | Why it ships now | Confidence |
|---|---|---|---|
| Pilot ProdPriority with product leadership teams | Bet | Tests the core value proposition with real prioritization decisions and establishes the first adoption baseline. | H |
| Create the organizational evidence ingestion pipeline | Bet | The product cannot validate hypotheses or synthesize evidence without a reliable way to ingest approved organizational information. | H |
| Deliver source-level citations and evidence traceability | Contract | Every material recommendation must be traceable to evidence before leaders can safely use it. | H |
| Implement tiered confidence and uncertainty UX | Contract | Users need visible confidence, unresolved assumptions, and missing-evidence warnings before acting on recommendations. | H |
| Build human review and override workflow | Guardrails | Low-confidence and high-risk recommendations need accountable human review from the first pilot. | H |
| Automate golden-dataset regression testing | Contract | The 95% accuracy and less-than-1% hallucination targets must become release gates before production use. | H |
| Establish permission-scoped data access and audit logging | Guardrails | The pilot will handle sensitive organizational data and must preserve existing permissions and decision accountability. | H |

### Horizon 2, Validate (1–3 months)

| Initiative | Strategy Component | Hypothesis | Kill Criteria | Confidence |
|---|---|---|---|---|
| Deploy cascading model routing and cost telemetry | Margin | A 60% triage and 40% frontier mix can maintain recommendation quality while keeping AI COGS at or below $26.25 per user per month. | If we cannot meet the reliability targets within the $26.25 monthly AI COGS limit by week 6, we stop the current routing design. | M |
| Create decision and outcome tracking | Moat | Connecting recommendations to decisions and expected outcomes will produce differentiated evidence about which product investments succeed. | If fewer than 60% of pilot recommendations have a recorded decision and measurement plan by week 6, we stop building the full workflow and simplify the capture process. | M |
| Launch recommendation challenge mode | Contract | Counterarguments and alternative interpretations will improve user trust and reduce acceptance of weak recommendations. | If fewer than 30% of pilot users apply challenge mode to high-value decisions or it produces no measurable trust improvement by week 6, we stop. | M |
| Integrate Jira and Confluence evidence | Bet | Direct access to planning, strategy, discovery, and delivery data will reduce manual preparation and increase repeat usage. | If the integration does not reduce evidence-preparation time by at least 30% across three pilot teams by week 6, we stop expanding it. | M |
| Integrate customer, support, CRM, and analytics signals | Moat | Cross-functional signals will produce more complete and better-grounded prioritization recommendations than product data alone. | If fewer than 50% of evaluated recommendations benefit from evidence across three or more domains by week 6, we stop adding sources. | M |
| Deliver configurable prioritization criteria and scenario comparison | Bet | Transparent criteria and scenario comparison will help leaders understand trade-offs and make more consistent investment decisions. | If fewer than 60% of pilot users prefer the scenario comparison to their current prioritization approach by week 6, we stop. | M |
| Close the correction-to-outcome learning loop | Moat | Validated corrections and realized outcomes will improve evaluations, routing, confidence calibration, and future recommendations. | If two feedback cycles produce no measurable improvement in evaluation performance or confidence calibration by week 6, we stop automating the loop. | M |
| Generate executive decision briefs | Bet | Decision-ready summaries will reduce preparation time and make ProdPriority easier to use in investment reviews. | If briefs do not reduce review-preparation time by at least 25% or are not used in real decision forums by week 6, we stop treating this as a separate initiative. | M |
| Implement multi-provider model portability | Margin | A provider-neutral interface will reduce vendor exposure without causing a material reliability or governance regression. | If an alternate provider cannot remain within 5% of the primary model’s quality target or be activated within 48 hours by week 6, we stop the portability build. | M |

### Horizon 3, Explore (3–6 months)

| Initiative | Strategy Component | What must be true first | Confidence |
|---|---|---|---|
| Enable cross-domain opportunity learning | Moat | The correction-to-outcome loop must work within individual domains, common identifiers must connect evidence and outcomes, and privacy controls must prevent inappropriate context transfer. | L |
| Create organization-wide product decision intelligence | Moat | At least three product domains must contribute reliable outcome data, cross-domain transfer must improve recommendations, and governance must approve anonymized benchmarking. | L |

### Unmapped (cut or rethink)

| Initiative | Why it's unmapped | Recommendation |
|---|---|---|
| None | Every initiative connects to at least one of the five strategy components. | Continue, but treat executive decision briefs as a capability within the core workflow rather than a standalone investment if capacity is constrained. |

### Mapping Disagreements

No disagreements, all user mappings stand.

Horizon 2 is the most over-indexed, with nine simultaneous validation bets. Reduce work in progress and sequence integrations, learning loops, economics, and portability behind the Horizon 1 reliability foundation.

If budget is cut, protect **cross-domain opportunity learning** because it is the Horizon 3 bet most likely to convert isolated product usage into a defensible organizational advantage.

Kill **Generate executive decision briefs** as a standalone initiative today and absorb basic export functionality into the pilot, because presentation formatting does not validate the core product or strengthen the moat.

## Board Pitch

**Thesis (1 sentence):**
ProdPriority will help product leaders identify and act on the opportunities most likely to advance business strategy by turning fragmented organizational evidence into faster, traceable prioritization decisions.

**The case:**
1. Why now: The CEO has identified slow opportunity identification and prioritization as a competitive constraint, while the evidence required to make those decisions remains fragmented across product, customer, delivery, financial, risk, and strategy systems. ProdPriority addresses that internal urgency, but the strategy does not yet quantify the current decision-cycle time, cost of poor prioritization, or value lost through delayed decisions; establishing that baseline is the first requirement of the pilot.
2. What's defensible: The intended M2 moat is a proprietary decision-outcome dataset that connects organizational evidence, AI recommendations, human decisions, corrections, and realized business outcomes. General-purpose platforms can reproduce the visible recommendation experience, but they cannot immediately reproduce this organization-specific history or its integration into product-investment workflows. That moat does not exist yet: the recursive-learning loop is broken, cross-domain transfer and network intelligence are missing, and workflow depth is limited. The six-month investment must prove that the learning loop measurably improves recommendation quality and creates switching costs.
3. The economics: At $140 revenue and $28.25 total COGS per user per month, ProdPriority produces $111.75 in gross profit and a 79.8% gross margin. If AI COGS triples, margin falls to 42.3% and gross profit to $59.25; if usage doubles without additional revenue, margin falls to 61.1% and gross profit to $85.50. The planned 60% triage and 40% frontier-model cascade must keep AI COGS at or below $26.25 per user per month without reducing reliability. Outcome pricing is still an assumption: the pilot must establish what qualifies as a resolved conversation, whether internal buyers accept $35 per outcome, and whether outcomes can be measured consistently.

**The risks:**
1. Trust / failure modes: The critical failure is a confident recommendation that directs material investment toward the wrong opportunity because the evidence was incomplete, outdated, duplicated, manipulated, or missing an important cross-functional signal. ProdPriority addresses this with source-level citations, visible uncertainty, human escalation, a 95% accuracy target, a hallucination target below 1%, and release-blocking evaluations. The current golden dataset contains only 10 cases, including three adversarial cases, which is insufficient evidence for production reliability; it must be expanded and tested against representative product domains before broader release.
2. Scale / governance: At 10x usage, the main constraints will be source-system permissions, integration reliability, model cost, low-confidence review volume, audit capacity, and the quality of human corrections entering the learning loop. ProdPriority must retain least-privilege access, preserve source permissions, log every material recommendation and approval, and keep funding and roadmap decisions with accountable product leaders. The current dependence on Claude also creates vendor and pricing exposure; portability must be demonstrated against an alternate provider before enterprise scale.
3. Competitive: The decisive threat is OpenAI, Palantir, Productboard, or an existing enterprise platform combining organizational search with product-prioritization recommendations before ProdPriority closes its learning loop. If Jira and Confluence integration does not reduce evidence-preparation time by at least 30%, fewer than 60% of pilot recommendations are connected to a decision and measurement plan, or two feedback cycles produce no measurable reliability improvement, we stop expanding the product and reassess build versus buy.

**The ask:**
Approve $1 million for two engineers, one Product Manager, and one Business Analyst over six months, released through defined reliability, adoption, economics, and governance gates. The investment will deliver a controlled working model with secure evidence ingestion, source citations, tiered confidence, human review, automated regression testing, audit logging, model-cost telemetry, and a pilot with product leadership teams. Success means demonstrating at least 95% evaluation accuracy, less than 1% hallucination, AI COGS at or below $26.25 per user per month, measurable reduction in decision-preparation time, and repeated use in real prioritization decisions. Funding this work pauses executive decision briefs as a standalone initiative, broad cross-domain integrations, network intelligence, and other Horizon 3 capabilities until the core workflow proves reliability, adoption, and decision value.

## M1 Baseline vs. Now
*Your 3-sentence AI strategy from Module 1 vs. what you'd say now:*

**M1 baseline:**

**Now:**
