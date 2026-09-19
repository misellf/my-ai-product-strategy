# Cost Curve & Pricing Strategy

## Cost Model

| Cost Category | Per-User/Month | Notes |
|--------------|----------------|-------|
| Inference (primary model) | $22| |
| Inference (cascading/triage) |$8 | |
| Infrastructure |$0.5 | |
| Data/storage | $1.5| |
| Human-in-the-loop |$0 | |
| **Total AI COGS** | $32| |

## Cascading Strategy
<!-- Cheap model → frontier model routing logic -->

**Triage model:** Mid, Medium-cost Model

**Frontier model:** Advanced reasoning model

**Routing rule:** Route all requests to the triage model first. Escalate to the frontier model when the request is complex, high-risk, requires multi-step reasoning, or the triage model’s confidence is below the agreed threshold.

**Expected cascade ratio:** 60%/40%

## Pricing Model

**Current pricing:**

**Proposed AI pricing:**

**Model:** outcome-based 

## Stress Tests

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x | | |
| Heaviest segment doubles | | |
| Model provider raises prices 50% | | |

## Board One-Pager
<!-- Before/After: Old SaaS revenue vs. AI usage revenue for your product -->

**Before (traditional SaaS):**
**After (AI-enabled):**
**Net margin shift:**
