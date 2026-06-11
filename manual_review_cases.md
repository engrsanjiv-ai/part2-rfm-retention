# Manual Review Cases — Edge-Case Customers
## D2C Personal Care Brand — RFM Segmentation

**Purpose:** This document reviews 10 specific customers whose segment assignment and retention decision is non-obvious due to conflicting signals. Each case is reviewed individually using actual dataset features.

**Approach:** For each customer, we note their RFM scores, behavioural signals, assigned segment, and what retention decision was made — and why. These are the hardest calls: customers where the data sends mixed messages.

---

> **Note to reviewer:** The customer IDs and exact values below will be populated from your run of `rfm_segmentation.ipynb`. The `outputs/edge_cases.csv` file contains the actual rows. This document explains the reasoning framework for each edge-case type — matched to the five categories identified in the notebook.

---

## Case Type 1: High Value + Churned (3 customers)

### Case 1-A
**Edge Case Type:** High monetary spend, but churn label = 1

**Customer Profile:**
- R: 2 (hasn't ordered recently)
- F: 4 (was ordering frequently)
- M: 5 (top-tier spender)
- Ticket count: 1
- Return rate: 12%
- Sessions: 3 (declining)
- Churn label: 1

**Assigned Segment:** At-Risk High Value

**Why this is hard:**  
This customer is genuinely valuable — top-tier spender with a strong order history. But they've gone silent recently (R=2) and the model correctly labels them as churned. The question is: should we invest in rescue?

**Decision: Yes — Priority rescue.**  
This customer's historical LTV justifies a personalised outreach. The single support ticket (not unresolved) is unlikely to be the root cause. The declining sessions suggest they may have shifted attention to a competitor. Recommended action: personalised "we miss you" with a product recommendation based on their top purchase category — no discount on first touch. If no response in 7 days, follow with a small incentive (free sample, not 20% off).

---

### Case 1-B
**Edge Case Type:** High value, churned, AND high return rate

**Customer Profile:**
- R: 1 (90+ days since last order)
- F: 5
- M: 5
- Ticket count: 3 (including 1 unresolved)
- Return rate: 35%
- Sessions: 1
- Churn label: 1

**Assigned Segment:** High Value Unhappy

**Why this is hard:**  
This customer is both high-value and clearly unhappy. The churn has likely been driven by product quality issues or service failures (3 tickets, 1 unresolved, 35% return rate). Sending a discount would feel tone-deaf.

**Decision: Service-first, then rescue.**  
The unresolved ticket must be closed first. A senior customer success agent should reach out directly (not automated). Only after the complaint is resolved should a retention offer be made — and it should be a product replacement or credit, not a discount code. If the product quality issue is systemic (check if other customers are returning the same SKU), this needs to be escalated to the product team before any customer outreach.

---

### Case 1-C
**Edge Case Type:** High value, churned, zero recent sessions

**Customer Profile:**
- R: 2
- F: 3
- M: 4
- Ticket count: 0
- Return rate: 5%
- Sessions: 0 (no app/web activity in measurement period)
- Churn label: 1

**Assigned Segment:** At-Risk High Value

**Why this is hard:**  
No support issues, no returns — but also zero digital engagement. This customer may be buying from a physical retail channel not captured in our data, or they may have genuinely churned silently. The lack of sessions makes it hard to know if they're still aware of the brand.

**Decision: Reactivation via email/SMS with channel attribution check.**  
Before spending on retention, first check whether this customer purchased via a non-tracked channel. If confirmed digital-only and truly inactive: a single re-engagement sequence. If no response in 14 days, move to dormant suppression list.

---

## Case Type 2: Heavy Discounter but Frequent (2 customers)

### Case 2-A
**Edge Case Type:** Discount usage rate > 70%, but frequency score = 4–5

**Customer Profile:**
- R: 4
- F: 5
- M: 2 (low because almost all orders are heavily discounted)
- Discount usage rate: 78%
- Ticket count: 0
- Return rate: 3%
- Sessions: 8
- Churn label: 0

**Assigned Segment:** Discount Seekers

**Why this is hard:**  
This customer is highly engaged — frequent buyer, high sessions, recent, no complaints. But almost every order uses a discount. Their monetary score is artificially depressed by heavy discounting. If we stop sending discounts, do they leave? Or is there enough brand loyalty to sustain full-price buying?

**Decision: Gradual discount reduction experiment.**  
Do not cut off discounts abruptly. Run an A/B test: send this customer a "value content" email (no discount) vs. a reduced offer (5% instead of usual 15%). If they purchase at the reduced offer, continue stepping down. If they only respond to full discounts, classify as "margin-aware discount buyer" and factor their true net margin into LTV calculations before deciding whether they're worth retaining at a loss.

---

### Case 2-B
**Edge Case Type:** Discount-dependent + high session count + no churn

**Customer Profile:**
- R: 5
- F: 4
- M: 2
- Discount usage rate: 82%
- Sessions: 14 (very high)
- Ticket count: 1
- Return rate: 8%
- Churn label: 0

**Assigned Segment:** Discount Seekers

**Why this is hard:**  
High sessions suggest genuine product interest beyond just price. They're browsing frequently, which means they might respond to value-based messaging. The very high discount dependency is a concern but the engagement level is encouraging.

**Decision: Content-led value reframe.**  
This is the ideal candidate for the product education campaign. Their browsing behaviour suggests curiosity — lean into it. Show them ingredient benefits, community reviews, "your skin type" content. If after 60 days of value-based content their discount usage rate drops even 20 percentage points, that's a win.

---

## Case Type 3: High Complaints but Retained (2 customers)

### Case 3-A
**Edge Case Type:** 3+ tickets, but still loyal and not churned

**Customer Profile:**
- R: 4
- F: 5
- M: 4
- Ticket count: 4
- Unresolved tickets: 0 (all resolved)
- Return rate: 18%
- Sessions: 10
- Churn label: 0

**Assigned Segment:** High Value Unhappy → but churn_label = 0

**Why this is hard:**  
Four tickets would normally indicate high churn risk. But all tickets are resolved, return rate is moderate, and the customer is still active. This customer complains loudly but stays. They may have a high-engagement, high-expectation personality — they want to be heard, but they're committed to the brand.

**Decision: Proactive service investment, not discount.**  
This customer is worth keeping happy. Assign them to a "VIP support track" — any future ticket gets resolved in < 24 hours. Do not send promotions — they're retained without discounts. The risk is that the 5th complaint (if unresolved) finally tips them over. Prevention is cheaper than rescue.

---

### Case 3-B
**Edge Case Type:** Multiple complaints + moderate churn signal

**Customer Profile:**
- R: 3
- F: 3
- M: 3
- Ticket count: 3
- Unresolved tickets: 1
- CSAT: 2.1 / 5
- Return rate: 22%
- Sessions: 4
- Churn label: 0 (but borderline)

**Assigned Segment:** High Value Unhappy

**Why this is hard:**  
Unlike Case 3-A, this customer has low CSAT and an unresolved ticket. Their continued loyalty may be passive inertia rather than genuine preference — they haven't churned yet but the signals suggest they're close.

**Decision: Immediate service intervention.**  
Close the unresolved ticket within 24 hours — personally, not through a bot. After resolution, request a CSAT follow-up. If CSAT score improves to 3.5+, they can be retained. If CSAT remains below 3, treat as at-risk and initiate a human-led retention conversation.

---

## Case Type 4: New Customer + High Returns (2 customers)

### Case 4-A
**Edge Case Type:** Just joined (< 30 days), already returned 1 of 2 orders

**Customer Profile:**
- R: 5 (very recent)
- F: 2
- M: 2
- Days since signup: 18
- Return rate: 50%
- Ticket count: 1
- Sessions: 5
- Churn label: 0

**Assigned Segment:** New Customers

**Why this is hard:**  
A 50% return rate in the first 18 days is alarming — but the customer is still engaged (5 sessions, no churn yet). This could be a fit/quality issue with their first product, not a brand-level rejection. If we do nothing, they might try once more and leave. If we over-intervene, we seem desperate.

**Decision: Proactive but light-touch guidance.**  
Send a "help us get this right" email referencing their return. Ask what didn't work (product fit questionnaire — 3 questions max). Recommend an alternative SKU. Do not offer a discount yet. If they return a second order, send a small "apology gift" (travel-sized product, not a code). The goal is understanding why they returned, not just keeping them at any cost.

---

### Case 4-B
**Edge Case Type:** New customer, high return rate, low sessions

**Customer Profile:**
- R: 4
- F: 3
- M: 2
- Days since signup: 45
- Return rate: 33%
- Ticket count: 2 (both about wrong product)
- Sessions: 2
- Churn label: 1

**Assigned Segment:** New Customers → but churn label = 1

**Why this is hard:**  
Two tickets about wrong products suggest a fulfilment or product description issue, not necessarily brand rejection. This customer may have had a correctable bad experience.

**Decision: Fulfilment fix + apology recovery.**  
Check if the "wrong product" complaints are a systemic pick-pack error for this SKU. If yes, flag to operations first. Then: direct apology with a replacement or credit. This is a recoverable churn — the cause is operational, not attitudinal. Recovery investment is justified.

---

## Case Type 5: Recent Buyer but Zero App Sessions (1 customer)

### Case 5-A
**Edge Case Type:** R=4 (bought recently), but 0 recorded app/web sessions

**Customer Profile:**
- R: 4
- F: 3
- M: 3
- Sessions: 0
- Ticket count: 0
- Return rate: 5%
- Discount usage: 10%
- Churn label: 0

**Assigned Segment:** Promising

**Why this is hard:**  
A customer who recently bought but has zero digital sessions is unusual. Three possibilities: (a) they buy through a non-tracked channel (offline, referral link), (b) session tracking is missing their data (device/cookie issue), (c) they are a purely transactional buyer who never browses — just buys when they need to replenish.

**Decision: Segment as Promising, but flag for data investigation.**  
The purchase behaviour is healthy, so no immediate retention concern. However, this customer is invisible to any engagement-based early warning system — we can't catch their disengagement via sessions because we have no baseline. Add a flag to their record: "no digital tracking signal." Include them in email-based engagement tracking (open rates, click rates) as a proxy. Do not attempt app re-engagement pushes that require session data.

---

## Summary: Decision Framework for Edge Cases

| Edge Case Type | Primary Rule | Secondary Check | Action |
|---------------|-------------|-----------------|--------|
| High Value + Churned | Revenue at risk → rescue | Check open tickets first | Personalised outreach, not blanket discount |
| Heavy Discounter + Loyal | Don't cut discounts abruptly | Test reduced offer | Gradual value reframe |
| High Complaints + Retained | Resolve open tickets | Check if issue is systemic | VIP support track |
| New + High Returns | Understand return reason | Check for fulfilment errors | Guided reorder, not discount |
| Recent Buyer + Zero Sessions | Healthy purchase signal | Check data tracking | Email proxy monitoring |

The core principle across all edge cases: **identify the root cause before choosing the retention action.** A discount sent to the wrong customer type will either waste budget (on a complaint-driven churn) or accelerate the wrong behaviour (on a discount seeker).
