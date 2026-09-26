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

**The case:**
1. Why now:
2. What's defensible:
3. The economics:

**The risks:**
1. Trust / failure modes:
2. Scale / governance:
3. Competitive:

**The ask:**

## M1 Baseline vs. Now
*Your 3-sentence AI strategy from Module 1 vs. what you'd say now:*

**M1 baseline:**

**Now:**
