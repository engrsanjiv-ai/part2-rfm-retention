# Retention Strategy & Campaign Budget Plan
## D2C Personal Care Brand — RFM Segmentation Output

**Prepared by:** ML Engineering Team  
**Based on:** RFM + behavioural enrichment segmentation  
**Segments defined:** 7  
**Budget constraint:** Limited campaign budget — prioritised by expected ROI

---

## Overview: Segment Landscape

| Segment | Size | Churn Rate | Median Recency | Median Frequency | Median Monetary | Action Priority |
|---------|------|-----------|-----------------|-----------------|-----------------|-----------------|
| Champions | 5 (0.2%) | 20.0% | 19 days | 11 | ₹9,242 | Protect & Reward |
| Loyal Customers | 9 (0.4%) | 33.3% | 52 days | 11 | ₹8,130 | Nurture & Upsell |
| Promising | 225 (9.4%) | 14.2% | 33 days | 6 | ₹4,265 | Accelerate |
| At-Risk High Value | 437 (18.2%) | 78.0% | 147 days | 4 | ₹2,579 | 🔴 Urgent Rescue |
| High Value Unhappy | 391 (16.3%) | 39.4% | 57 days | 6 | ₹4,444 | 🔴 Urgent Fix |
| New Customers | 460 (19.2%) | 22.6% | 20 days | 1 | ₹806 | Onboard Well |
| Dormant | 873 (36.4%) | 56.4% | 79 days | 2 | ₹1,252 | Low-Cost Win-Back |

**Total Customers: 2,400**

---

## Segment 1: Champions

### Who are they?
Customers with the highest recency (R≥4), frequency (F≥4), and monetary (M≥4) scores. They buy often, spend a lot, and bought recently. They have almost no support complaints. These are the customers every D2C brand lives on.

### Behavioural Evidence
- Recency: median 19 days (typically ordered within 3 weeks)
- Frequency: median 11 orders
- Monetary: median ₹9,242 lifetime spend (top tier)
- Ticket count: 0.6 on average (minimal support friction)
- Return rate: 1.8% (very low)
- Session count: 1.0 Avg (session signal is flat across all segments )
- Dataset: 5 customers

### Churn Rate
20.0% — Lowest among all segments. These customers are not churn risks; they are an asset.

### Retention Action
**Do NOT discount.** Offering discounts to Champions trains them to expect them and erodes margin on your most loyal buyers.

Instead:
- Enrol them in an exclusive loyalty tier (if not already)
- Offer early access to new product launches
- Send personalised "thank you" messages with product recommendations based on purchase history
- Invite them to a referral programme — Champions are your best acquisition channel
- Share their anonymised loyalty status: "You're in our top 10% of customers"

### Expected Business Value
Champions generate disproportionate revenue. Even a 2% improvement in retention here protects significant LTV. Cost per action: low (loyalty comms, referral programme).

---

## Segment 2: Loyal Customers

### Who are they?
High frequency (F≥4) and high monetary (M≥4) scores with acceptable recency (R≥3). They may be slightly less recent than Champions but have a long, valuable history.

### Behavioural Evidence
- Recency: median 52 days
- Frequency: median 11 orders (high repeat rate)
- Monetary: median ₹8,130 lifetime spend
- Ticket count: 3.6 on average (elevated support engagement)
- Return rate: 9.8%
- Dataset: 9 customers

### Churn Rate
33.3% — Low-to-medium risk. However, elevated ticket count (3.6 avg) suggests support quality issues are eroding loyalty.

### Retention Action
- Reward with a **loyalty milestone benefit** (free shipping upgrade, gift with next purchase)
- Personalised product recommendations: "Based on your last 5 orders, you might like X"
- Nudge for membership tier upgrade if not already on highest tier
- Monthly "just for you" content email — no discount, product tips and guides

### Expected Business Value
Strong LTV segment. Small investments here (loyalty perks, content) generate strong repeat behaviour. Avoid discount dependency.

---

## Segment 3: At-Risk High Value 🔴

### Who are they?
Customers who were previously strong on frequency or monetary value (F≥3 or M≥3) but whose recency has dropped significantly (R≤2 — likely 45–90+ days since last order). These are former Champions or Loyal customers who are disengaging.

### Behavioural Evidence
- Recency: median 147 days — significant dormancy
- Frequency: median 4 orders historically
- Monetary: median ₹2,579 lifetime spend
- Last order typically 4.5–5 months ago
- Support tickets: 0.58 on average
- Session count: 1.0 average (identical across all segment)
- Dataset: 437 customers (18.2% of total)

### Churn Rate
78.0% — **Critical.** This is the highest churn rate in the dataset. These customers are actively leaving. This is the most urgent rescue segment.

### Retention Action
This is the segment where a **small, targeted incentive is justified**:
1. **Day 45 inactivity trigger:** Personalised re-engagement email — "We miss you, [Name]. Here's what's new."
2. **Day 60 trigger:** One-time 10–15% personalised offer (not a blanket promo code — personalised to their top category)
3. **Check for open support tickets** — if they have any, resolve them first before sending the promo
4. **Phone/WhatsApp outreach** for top 20% by historical spend

### Expected Business Value
Rescuing even 20% of At-Risk High Value customers saves significant revenue. At an average order value of ₹X, each recovered customer contributes multiple future orders. This segment should receive the largest share of the retention budget.

---

## Segment 4: High Value Unhappy 🔴

### Who are they?
Customers with high monetary value (M≥4) but elevated support complaints (ticket_count≥2), unresolved tickets, or return rates above 25%. These customers are valuable — but they're having a bad experience.

### Behavioural Evidence
- Recency: median 57 days
- Frequency: median 6 orders
- Monetary: median ₹4,444 lifetime spend (high-value profile)
- Support tickets: 2.38 on average (elevated friction — highest ticket count in dataset)
- Return rate: 12.8% (elevated — indicating product quality or fit concerns)
- Dataset: 391 customers (16.3% of total)

### Churn Rate
39.4% — High and predictable. These customers signal frustration explicitly through support tickets and returns. Without intervention, churn will accelerate.

### Retention Action
**Critical: Fix the problem before offering anything promotional.**
1. Proactive outreach from customer support within 48 hours of second ticket: "We saw you had an issue — can we make this right?"
2. Dedicated resolution of their open complaint — close all tickets before any campaign
3. Only after resolution: a personalised "apology gift" (free product sample, upgraded shipping on next order — not just a discount)
4. Check if the product quality issue is systemic (multiple customers returning same SKU) — flag to product team

### Expected Business Value
High. These customers already trust the brand enough to spend significantly. The churn is preventable if the product/support team acts fast. Cost of inaction: full LTV lost + potential negative reviews.

---

## Segment 5: Promising

### Who are they?
Customers with moderate recency (R≥3), frequency (F≥2), and monetary (M≥2). They are engaged but haven't yet developed a strong purchase habit. They show potential — they just need the right nudge to become Loyal Customers.

### Behavioural Evidence
- Recency: median 33 days (active)
- Frequency: median 6 orders
- Monetary: median ₹4,265 lifetime spend
- Support tickets: 0.62 on average (low friction)
- Return rate: 2.5% (very low — good product fit)
- Dataset: 225 customers (9.4% of total)

### Churn Rate
14.2% — Lowest churn outside of Champions and Loyal Customers. These customers are engaged and well-satisfied. Activation is high-ROI.

### Retention Action
- **Second/third order nudge:** "Complete your routine — customers who add [Product B] to [Product A] love the results."
- **Subscription/auto-replenishment pitch:** Position a subscription on their most-purchased SKU
- **Membership tier invitation:** "You're one order away from [Silver] benefits"
- Educational content about their purchased categories

### Expected Business Value
High long-term value. Promising customers who cross into Loyal Customers add 3–5× their current LTV. Investment here is future-value protection.

---

## Segment 6: New Customers

### Who are they?
Customers who joined in the last 60 days OR have only 1–2 orders and high recency. They are in the critical first-purchase-to-second-purchase window.

### Behavioural Evidence
- Recency: median 20 days (very recent)
- Frequency: median 1 order (first-time buyers and very early repeat)
- Monetary: median ₹806 first order value
- Support tickets: 0.31 on average (low — mostly smooth onboarding)
- Return rate: 7.7% (typical for new customers testing fit)
- Dataset: 460 customers (19.2% of total)

### Churn Rate
22.6% — Moderate, but this is AFTER the first order. The critical metric is second-order conversion rate, not current churn.

### Retention Action
- **Day 3 post-purchase:** Usage tips for what they just bought
- **Day 10:** "How are you liking [Product X]?" — CSAT check, invite review
- **Day 20:** Product recommendation nudge: "Customers who bought X also love Y"
- **Day 25:** If no second order — low-friction offer: free sample with next order (not a discount)
- Onboarding email sequence: brand story, product education, community

### Expected Business Value
Second order conversion is the highest-leverage metric for this brand. Every % increase in second-order conversion rate compounds into significant revenue over a 12-month cohort.

---

## Segment 7: Dormant

### Who are they?
Low recency (R≤2, typically 60–180+ days since last order), low frequency, low monetary. These customers have largely disengaged. Some may have churned already.

### Behavioural Evidence
- Recency: median 79 days (over 2.5 months dormant)
- Frequency: median 2 orders
- Monetary: median ₹1,252 lifetime spend (low)
- Support tickets: 0.48 on average
- Return rate: 5.9%
- Dataset: 873 customers (36.4% of total — largest segment)

### Churn Rate
56.4% — Very high. These customers have largely withdrawn already, so the baseline churn label is baked in. Win-back rates are typically 2–8% for this segment.

### Retention Action
- **Low-cost win-back only:** A single well-crafted re-engagement email — no expensive personalisation
- Subject line curiosity hook: "Something new you might have missed"
- If no response after 2 touches → suppress from all campaigns (reduce list fatigue and email domain reputation risk)
- **Do not send discounts** to unresponsive dormant customers — ROI is near zero and erodes margin
- Segment out the truly lost (180+ days, 1 order) for annual suppression review

### Expected Business Value
Low. Win-back rates for dormant customers typically run 2–8%. Budget accordingly — only spend what is needed for one low-cost email sequence.

---

## Campaign Budget Prioritisation

Assume a fixed campaign budget of 100 units (relative allocation) across 2,400 customers.

| Priority | Segment | Size | Churn Rate | Budget Allocation | Rationale |
|----------|---------|------|-----------|-------------------|-----------|
| 1 | At-Risk High Value | 437 (18.2%) | 78.0% | **35 units** | Highest revenue risk; each recovered customer = significant LTV saved |
| 2 | High Value Unhappy | 391 (16.3%) | 39.4% | **25 units** | High LTV at stake; support + personalized recovery justified |
| 3 | Promising | 225 (9.4%) | 14.2% | **18 units** | Future LTV compounding; low churn makes investment safe |
| 4 | New Customers | 460 (19.2%) | 22.6% | **15 units** | Second-order conversion is highest-leverage action for cohort growth |
| 5 | Loyal Customers | 9 (0.4%) | 33.3% | **4 units** | VIP treatment only; low cost, recognition + referral program |
| 6 | Champions | 5 (0.2%) | 20.0% | **2 units** | Brand advocacy only; no spend needed |
| 7 | Dormant | 873 (36.4%) | 56.4% | **1 unit** | One low-cost email sequence only; ROI minimal |

**Total: 100 units**

### Why At-Risk High Value gets priority over Champions
Champions are already safe (only 5 customers). At-Risk High Value customers (437 customers, 78% churn) are in an active decay window — they were strong customers recently and are sliding out. The expected value of rescuing one At-Risk High Value customer is higher than the marginal value of recognising one Champion. Additionally, At-Risk High Value customers have a median lifetime spend of ₹2,579, making each recovery meaningful.

### Why Dormant gets minimal budget
Win-back rates for dormant customers with 1–2 orders who have been silent 60+ days are typically 2–8%. At 873 customers (36% of base), even a 5% recovery rate = 44 customers. At a median LTV of ₹1,252, the return is modest. Instead, use dormant segment for list hygiene: suppress from active campaigns to protect email domain reputation and focus budget on higher-intent segments.

---

## Monitoring Recommendations

After deploying retention actions per segment:

1. **Segment migration metrics** (monthly):
   - % of At-Risk High Value → Loyal Customers (target: ≥15% month-over-month)
   - % of Promising → Loyal Customers (target: ≥25%)
   - % of New Customers → Promising/Loyal (measure second-order conversion)

2. **At-Risk High Value recovery** (weekly):
   - Campaign response rate (email open, click, conversion)
   - Order placed within 30 days of campaign send
   - Target: Recover 20–25% of segment

3. **New Customers** (weekly):
   - Second-order conversion rate (critical metric)
   - Days to second order
   - Target: ≥30% second-order conversion within 60 days

4. **High Value Unhappy** (weekly):
   - Support ticket resolution time (target: <24 hours for this segment)
   - Re-engagement email open rate post-resolution
   - Target: 40%+ sustained engagement after support fix

5. **Revenue impact**:
   - Segment-level LTV trend (recalculate every 30 days)
   - Cohort retention rate by segment

6. **System maintenance**:
   - **Recalculate RFM scores every 30 days** and re-assign segments
   - Static segmentation decays rapidly; refresh ensures targeting remains sharp
   - Archive old segment assignments for cohort analysis
