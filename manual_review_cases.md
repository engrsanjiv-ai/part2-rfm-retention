# Manual Review Cases — Edge-Case Customers
## D2C Personal Care Brand — RFM Segmentation

**Purpose:** This document reviews 10 specific customers whose segment assignment and retention decision is non-obvious due to conflicting signals. Each case is reviewed individually using actual dataset features.

**Approach:** For each customer, we note their RFM scores, behavioural signals, assigned segment, and what retention decision was made — and why. These are the hardest calls: customers where the data sends mixed messages.

---

> **Note:** Customer IDs and values below are populated from the `rfm_segmentation.ipynb` notebook run. The `outputs/edge_cases.csv` file contains the source data for these cases. This document provides the reasoning framework for each edge-case type identified in the analysis.

---

## Case Type 1: High Value + Churned (3 customers)

### Case 1-A
**Customer ID:** CUST00020

**Edge Case Type:** High monetary spend, but churn label = 1

**Customer Profile:**
- R: 1 (368 days since last order — over a year)
- F: 1 (only 3 orders total)
- M: 5 (top-tier spender: $4,487.95 lifetime, $1,495.98 avg order value)
- Ticket count: 1
- Return rate: 0%
- Sessions: 1
- Churn label: 1

**Assigned Segment:** At-Risk High Value

**Why this is hard:**  
This customer is genuinely valuable — top-tier spender with an exceptional average order value. However, they haven't ordered in over a year (368 days) and have minimal engagement (only 3 orders despite high spend). The model correctly identifies them as churned. The question is: should we invest in rescue given their historical LTV?

**Decision: Yes — Priority rescue.**  
This customer's high average order value ($1,495.98) justifies a personalized win-back campaign. The absence of support issues suggests the churn was not driven by a service failure. Recommended action: personalized "we miss you" email with a product recommendation based on their purchase history and highest-value category — no discount on first touch. If no response in 7 days, follow with a modest incentive (free shipping or loyalty credit, not a blanket discount). Track their re-engagement carefully as a high-value recovery target.

---

### Case 1-B
**Customer ID:** CUST00025

**Edge Case Type:** High value, churned, AND high support engagement

**Customer Profile:**
- R: 1 (165 days since last order)
- F: 2 (7 orders total)
- M: 5 (high spender: $4,868.86 lifetime, $695.55 avg order)
- Ticket count: 3 (all resolved)
- Return rate: 0%
- Sessions: 1
- Churn label: 1

**Assigned Segment:** High Value Unhappy

**Why this is hard:**  
This customer is both high-value and high-support-engagement. The 3 support tickets despite no returns or quality issues suggest they may have had fulfillment, shipping, or service questions rather than product dissatisfaction. Their churn despite engagement suggests service issues may have driven them away.

**Decision: Service-first investigation, then targeted retention.**  
Review the content of the 3 support tickets to identify the root cause. If tickets reveal a systemic service issue (e.g., shipping delays, order confusion), escalate to operations. Once the issue is understood, reach out with a sincere apology and service recovery: offer a loyalty credit or priority support status rather than a discount. Frame it as "we value your business and want to make this right."

---

### Case 1-C
**Customer ID:** CUST00051

**Edge Case Type:** High value, churned, zero recent sessions

**Customer Profile:**
- R: 1 (210 days since last order)
- F: 1 (4 orders total)
- M: 5 (top-tier spender: $4,444.30 lifetime, $1,111.08 avg order)
- Ticket count: 2
- Return rate: 0%
- Sessions: 1
- Churn label: 1

**Assigned Segment:** High Value Unhappy

**Why this is hard:**  
No returns and only 2 support tickets, yet this high-value customer has gone dormant (210 days). Unlike Case 1-A's single ticket, this customer has multiple support interactions which might signal frustration despite no explicit churn trigger visible in the data.

**Decision: Direct outreach to understand root cause.**  
Call or email this customer directly (not a broadcast campaign). Ask: "We noticed you haven't placed an order recently — is there something we can help with or improve?" This is a listening mission before a selling mission. Their high AOV ($1,111) makes this high-touch outreach justified. Based on their feedback, either resolve an underlying issue or rebuild the relationship with a personalized offer.

---

## Case Type 2: Heavy Discounter but Frequent (2 customers)

### Case 2-A
**Customer ID:** CUST00014

**Edge Case Type:** Extremely frequent buyer, but high discount dependency

**Customer Profile:**
- R: 3 (51 days since last order)
- F: 4 (11 orders total)
- M: 5 (high spend: $8,130.16, $739.11 avg order)
- Discount usage rate: 100% (every order heavily discounted)
- Ticket count: 2
- Return rate: 0%
- Sessions: 2
- Churn label: 0 (not churned, still active)

**Assigned Segment:** Loyal Customers (despite discount dependency)

**Why this is hard:**  
This customer is highly engaged — frequent buyer (11 orders), still active, zero returns. BUT they ONLY purchase when discounted. Their high monetary score reflects volume, not margin. If we remove discounts, do they stay? Or is every purchase contingent on a deal?

**Decision: Gradual value narrative shift + test reduced discount.**  
Do NOT cut off discounts abruptly — this customer may churn if we do. Instead: (1) Run an A/B test with this cohort: send a "loyalty member" email with 5% benefit instead of usual steep discounts. (2) If they respond at 5%, gradually step it down to 0% with value-based content (educational, community, sustainability messaging). (3) If they only respond to deep discounts, reclassify them as "high-volume, low-margin" and adjust LTV calculations. May not be worth retaining profitably.

---

### Case 2-B
**Customer ID:** CUST00088

**Edge Case Type:** Heavy discount user + frequent orders, but CHURNED

**Customer Profile:**
- R: 2 (98 days since last order — recency declining)
- F: 4 (12 orders total — highest frequency in dataset)
- M: 5 (good spender: $6,774.50, $564.54 avg)
- Discount usage rate: 100% (all discounted)
- Sessions: 1
- Ticket count: 1
- Churn label: 1 (recently churned despite high frequency)

**Assigned Segment:** At-Risk High Value

**Why this is hard:**  
This customer had the highest order frequency (12 orders) and is now churned. The pattern suggests: they came for the discounts, built a habit of frequent replenishment, but now they've stopped. This is NOT a discount seeker who lost interest — this is a loyal customer base that may have found a competitor with better deals or switched to a substitute.

**Decision: Win-back with premium positioning, NOT deeper discounts.**  
Sending a bigger discount will accelerate the wrong signal. Instead: (1) Reach out with a personal message acknowledging their loyalty ("We know you loved [product X]..."). (2) Offer a loyalty tier or VIP status that makes them feel valued beyond price. (3) If they re-engage, test moving them from pure discount orientation to a loyalty program with points/benefits. If they don't respond, they've likely switched brands — likely not worth excessive rescue spending.

---

## Case Type 3: High Complaints but Retained (2 customers)

### Case 3-A
**Customer ID:** CUST00034

**Edge Case Type:** Multiple support tickets but not churned

**Customer Profile:**
- R: 3 (50 days since last order)
- F: 2 (6 orders total)
- M: 4 (solid spender: $3,353.01, $558.84 avg)
- Ticket count: 3 (all resolved — unresolved: 0)
- Return rate: 0%
- Sessions: 1
- Churn label: 0 (retained despite support load)

**Assigned Segment:** High Value Unhappy

**Why this is hard:**  
Three tickets would normally indicate high churn risk. But this customer is still active, has zero returns, and hasn't churned. All tickets were resolved successfully. This suggests a customer who is engaged and vocal about their needs — they REACH OUT rather than silently churn. They have high expectations and want to be heard.

**Decision: Proactive service investment, not discount.**  
This customer is worth keeping happy. They're complainers in the best sense — they give feedback instead of just disappearing. Assign them to a "VIP support track": any future ticket resolved in < 24 hours by a senior agent. Do not send unsolicited promotions — they're retained through service excellence. Monitor their ticket themes for patterns (e.g., shipping, sizing, product questions) and consider this feedback for product/process improvements.

---

### Case 3-B
**Customer ID:** CUST00042

**Edge Case Type:** Multiple support tickets + high return rate, but not churned

**Customer Profile:**
- R: 2 (87 days since last order)
- F: 3 (9 orders total)
- M: 5 (top spender: $7,523.74, $835.97 avg)
- Ticket count: 6 (highest support load in dataset)
- Return rate: 22.2% (22.2% of orders returned)
- Sessions: 1
- Churn label: 0 (not yet churned, but borderline)

**Assigned Segment:** High Value Unhappy

**Why this is hard:**  
This customer has the highest support ticket count (6) AND a 22% return rate. Yet they haven't churned — however, they're declining in recency (87 days). High-value customers with high friction are expensive to keep and at serious risk.

**Decision: Root-cause investigation + immediate intervention.**  
Don't assume they're "just complainers" like Case 3-A. The 22% return rate combined with 6 tickets suggests a systemic product fit issue. Questions: (1) Are they returning the same SKU/category? (2) Are most tickets about returns/refunds or other issues? If there's a product quality pattern, escalate to product team immediately. After diagnosis: offer the customer a direct line to support (dedicated agent) + a product consultation to prevent future returns. This is a salvage operation; the risk is high but so is their LTV if saved.

---

## Case Type 4: New Customer + High Returns (2 customers)

### Case 4-A
**Customer ID:** CUST00251

**Edge Case Type:** Very new customer with complete product failure (100% return rate)

**Customer Profile:**
- R: 4 (41 days since signup)
- F: 1 (only 1 order)
- M: 2 (low spend: $966.73)
- Days since signup: 41
- Return rate: 100% (returned 1 of 1 orders)
- Ticket count: 1
- Sessions: 1
- Churn label: 1 (already churned)

**Assigned Segment:** New Customers (but churned immediately)

**Why this is hard:**  
A 100% return rate in the first month is critical — this customer received one order and rejected it entirely. Yet they're only 41 days into their lifecycle. This is either a critical product-fit issue or a fulfillment/quality error. We don't know which without examining the return reason.

**Decision: Rapid product-fit investigation + empathetic recovery.**  
(1) Review the return reason urgently: Was it wrong product, damaged in transit, sizing mismatch, or wrong item shipped? (2) If it was a fulfillment error, send immediate apology + replacement. (3) If it was product mismatch, ask a 3-question survey: "What didn't work? What would have been better? Can we recommend an alternative?" (4) Only AFTER understanding the issue, offer recovery: a replacement recommendation or $X store credit (not a discount code on their first failed product). This customer is salvageable if we show we care about getting it right.

---

### Case 4-B
**Customer ID:** CUST00310

**Edge Case Type:** Very new customer, 100% return rate, but NOT yet churned

**Customer Profile:**
- R: 4 (22 days since signup)
- F: 1 (only 1 order)
- M: 1 (very low spend: $578.27)
- Days since signup: 22
- Return rate: 100% (returned 1 of 1)
- Ticket count: 1
- Sessions: 1
- Churn label: 0 (not churned yet, but at extreme risk)

**Assigned Segment:** New Customers

**Why this is hard:**  
Similar to Case 4-A but even newer (22 days vs 41). This customer returned their only order but hasn't formally churned in the data yet — this is a critical intervention window. The single support ticket may hold the key to why they returned.

**Decision: Rapid outreach with system check.**  
(1) First, check the support ticket: What's the issue? (2) If it reveals a fulfillment/quality problem, fix it immediately and send a replacement without asking. (3) If it's a product mismatch, respond personally to their ticket with a warm message: acknowledge the issue, ask their product preferences, and recommend an alternative to try. (4) Include a goodwill gesture: free shipping on their next order or 10% loyalty credit if they retry. This customer is at the exact moment of decision — one more bad interaction and they're gone for good.

---

## Case Type 5: Mixed Signals (1 customer)

### Case 5-A
**Customer ID:** CUST00001

**Edge Case Type:** Mixed signals — churned high-value customer with support friction

**Customer Profile:**
- R: 2 (107 days since last order)
- F: 2 (6 orders total)
- M: 4 (mid-high spender: $2,955.57, $492.60 avg)
- Sessions: 1
- Ticket count: 2
- Return rate: 16.7% (1 of 6 orders returned)
- Discount usage: 16.7% (minimal discount dependency)
- Churn label: 1 (churned)

**Assigned Segment:** High Value Unhappy

**Why this is hard:**  
This customer doesn't fit neatly into any single pattern. They're not a pure discount seeker (16% discount usage), not a serial returner (16% return rate is moderate), not a super-complainer (2 tickets is normal). Yet they've churned. The mix of signals suggests a slow drift rather than a sudden shock — they may have felt gradually undervalued.

**Decision: Personalized listening outreach.**  
This customer needs a human conversation, not an automated email. A customer success agent should reach out with: "I see you last ordered in [month]. We noticed we haven't connected in a while — I'd genuinely like to know: is there something we could have done better?" This is a diagnostic call. Based on their response: if it's a service issue, resolve it; if it's a product issue, recommend something new; if it's just life circumstances, keep them on a nurture list for seasonal campaigns. The goal is understanding their mental model of the brand.

---

## Summary: Decision Framework for Edge Cases

| Edge Case Type | Primary Rule | Secondary Check | Action |
|---------------|-------------|-----------------|--------|
| High Value + Churned | Revenue at risk → rescue | Review support history | Personalized win-back, high-touch outreach |
| Heavy Discounter + Loyal | Test discount reduction | Check return patterns | Gradual value narrative shift, not cold turkey |
| High Complaints + Retained | Invest in service excellence | Root-cause analysis required | VIP support track, resolve before asking for spend |
| New + High Returns | Understand return reason | Check for systemic issues | Product-fit questionnaire, guided reorder |
| Mixed Signals | Use listening approach | Multiple weak signals = risk | Diagnostic conversation before retention offer |

**Core Principle:** Every edge case requires root-cause diagnosis before a retention action. A blanket discount applied to the wrong customer type will either waste budget or accelerate the wrong behavior. These customers demand customized interventions based on understanding their actual problem, not template responses.
