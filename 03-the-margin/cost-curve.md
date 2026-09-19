# Cost Curve & Pricing Strategy

## Cost Model

| Cost Category | Per-User/Month | Notes |
|--------------|----------------|-------|
| Inference (primary model) | $15| |
| Inference (cascading/triage) |$8 | |
| Infrastructure |$0.75 | |
| Data/storage | $1.5| |
| Human-in-the-loop |$0 | |
| **Total AI COGS** | $26.25| |

## Cascading Strategy
<!-- Cheap model → frontier model routing logic -->

**Triage model:** Mid, Medium-cost Model

**Frontier model:** Advanced reasoning model

**Routing rule:** Route all requests to the triage model first. Escalate to the frontier model when the request is complex, high-risk, requires multi-step reasoning, or the triage model’s confidence is below the agreed threshold.

**Expected cascade ratio:** 60%/40%

## Pricing Model

**Strategy posture:** Maximize
**Pricing model:** Outcome / Resolution
**Unit of work metered:** Resolved conversations
**Base fee ($/month):** 0
**Price per unit:** $35
**Estimated units/user/month:** 4
**Implied revenue/user/month:** $140.00

Decision Note
As an internal AI product, its value comes from helping product managers and leaders make faster, better-informed investment and prioritization decisions. By providing timely insights into customer problems, opportunities, and hypotheses, the product reduces uncertainty, avoids investment in low-value initiatives, and directs resources toward opportunities most likely to generate measurable business value.


## Stress Tests

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x | 42.3% ($59.25) | Increase model-routing efficiency, reduce unnecessary tokens and retries, use caching, and reserve the frontier model for requests where it materially improves the outcome. Consider increasing the outcome price if higher costs persist.
| Heaviest segment doubles | 61.1% ($85.50) | Introduce usage tiers or volume-based outcome pricing, monitor high-usage users, apply reasonable usage limits, and optimize workflows generating disproportionate model calls.
| Model provider raises prices 50% | 64.1% ($89.75)| Shift eligible workloads to lower-cost models, negotiate committed-volume pricing, maintain provider flexibility, and introduce a pricing-adjustment mechanism to protect margins from sustained increases. |


## Margin Calculator

### Inputs
**Avg requests/user/month:** 1750

**Blended cost/request:** $0.015

**Revenue/user/month:** $140

**Non-AI COGS/user/month:** $2

## Current Margin
**AI COGS/user:** $26.25
**Total COGS/user:** $28.25
**Gross margin:** 79.8% ($111.75/user)

## Stress Test
| Scenario | AI COGS | Margin |
|----------|---------|--------|
| 3x Cost  | $78.75 | 42.3% ($59.25) |
| 2x Usage | $52.50 | 61.1% ($85.50) |


## Board One-Pager
<!-- Before/After: Old SaaS revenue vs. AI usage revenue for your product -->

## Before, Traditional SaaS

**Revenue:** $100/seat × 1 seat

**COGS:** $12.00 (fixed)

**Gross margin:** 88.0%

## After, AI-Powered

**Revenue:** $0 base + $35 × 4 outcomes

**COGS:** $28.25 (variable)

**Gross margin:** 79.8%

#Net margin shift

**margin %:** −8.2 percentage points

**gross $:** +$23.75 per user/month
