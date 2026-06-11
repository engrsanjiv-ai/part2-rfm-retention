# Retention Strategy & Campaign Budget Plan
## D2C Personal Care Brand — RFM Segmentation Output

**Prepared by:** ML Engineering Team  
**Based on:** RFM + behavioural enrichment segmentation  
**Segments defined:** 8  
**Budget constraint:** Limited campaign budget — prioritised by expected ROI

---

## Overview: Segment Landscape

| Segment | Size (est. %) | Churn Risk | Revenue Risk | Action Priority |
|---------|--------------|------------|--------------|-----------------|
| Champions | ~10–15% | Very Low | Very High | Protect & Reward |
| Loyal Customers | ~12–18% | Low | High | Nurture & Upsell |
| Promising | ~10–15% | Medium | Medium | Accelerate |
| At-Risk High Value | ~8–12% | High | Very High | 🔴 Urgent Rescue |
| High Value Unhappy | ~5–8% | High | Very High | 🔴 Urgent Fix |
| Discount Seekers | ~10–15% | Medium-High | Low-Medium | Reframe or Accept |
| New Customers | ~10–15% | Medium | Low-Medium | Onboard Well |
| Dormant | ~15–25% | Very High | Low | Low-Cost Win-Back |

---

## Segment 1: Champions

### Who are they?
Customers with the highest recency (R≥4), frequency (F≥4), and monetary (M≥4) scores. They buy often, spend a lot, and bought recently. They have almost no support complaints. These are the customers every D2C brand lives on.

### Behavioural Evidence
- Recency: typically ordered within 15–25 days
- Frequency: 8+ lifetime orders
- Monetary: top 20% by total spend
- Ticket count: ≤ 1 on average
- Return rate: low (< 10%)
- Session count: high engagement across app/web

### Churn Rate
Lowest among all segments — typically 5–10%. These customers are not churn risks; they are an asset.

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
- 5–10 lifetime orders
- Regular purchase cadence, may skip a month but returns
- Low support ticket count
- Moderate app engagement

### Churn Rate
Low — typically 10–18%. Risk increases if recency slides to R=2.

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
- Previously 4–8 orders — now silent
- Last order 45–90+ days ago
- May have had a support ticket or bad delivery experience
- Session count dropping

### Churn Rate
High — typically 35–55%. This is the most urgent rescue segment.

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
- Top-quartile spend — high LTV potential
- 2+ support tickets, often product quality or wrong item
- May have low CSAT scores
- Still buying (recent enough) but frustration is building

### Churn Rate
High — typically 40–60% without intervention. Particularly dangerous because losing them has both revenue and word-of-mouth consequences.

### Retention Action
**Critical: Fix the problem before offering anything promotional.**
1. Proactive outreach from customer support within 48 hours of second ticket: "We saw you had an issue — can we make this right?"
2. Dedicated resolution of their open complaint — close all tickets before any campaign
3. Only after resolution: a personalised "apology gift" (free product sample, upgraded shipping on next order — not just a discount)
4. Check if the product quality issue is systemic (multiple customers returning same SKU) — flag to product team

### Expected Business Value
High. These customers already trust the brand enough to spend significantly. The churn is preventable if the product/support team acts fast. Cost of inaction: full LTV lost + potential negative reviews.

---

## Segment 5: Discount Seekers

### Who are they?
Customers with good frequency (F≥3) but low monetary value (M≤2) and high discount usage rate (≥50%). They buy regularly — but almost always with a promo code or campaign offer. Their average order value is below the base when no discount is present.

### Behavioural Evidence
- Consistent order history aligned with campaign dates
- Order frequency drops sharply between campaign windows
- High campaign response rate (opened, clicked, redeemed)
- Low average order value compared to frequency

### Churn Rate
Medium-high (25–40%) — but their churn doesn't hurt revenue as much as At-Risk High Value.

### Retention Action
**Do not send more discounts.** This rewards the very behaviour we want to reduce.
1. **Value reframing campaign:** Product education content — ingredient benefits, how-to guides, testimonials. Goal: shift purchase motivation from price to product quality.
2. **Anchor price awareness:** Show them "You've saved ₹X over the last year" — reinforces loyalty without triggering discount expectation for the next purchase.
3. **Introduce a points-based loyalty system** where they earn on every purchase (discounted or not) — this shifts the reward mechanism away from discount codes toward an engagement loop.
4. **Accept some churn:** A subset of this segment will only buy at a discount. It is acceptable to let that sub-group lapse rather than continuously subsidise them.

### Expected Business Value
Medium. Recovering discount seekers to full-price buying is hard but valuable if achieved. Avoid spending significant campaign budget on this segment — the ROI on further discounting is negative.

---

## Segment 6: Promising

### Who are they?
Customers with moderate recency (R≥3), frequency (F≥2), and monetary (M≥2). They are engaged but haven't yet developed a strong purchase habit. They show potential — they just need the right nudge to become Loyal Customers.

### Behavioural Evidence
- 2–4 orders, reasonably recent
- Moderate app/web engagement
- Low support ticket count
- Not discount-dependent

### Churn Rate
Medium — typically 20–30%. They will churn if not activated into a stronger habit.

### Retention Action
- **Second/third order nudge:** "Complete your routine — customers who add [Product B] to [Product A] love the results."
- **Subscription/auto-replenishment pitch:** Position a subscription on their most-purchased SKU
- **Membership tier invitation:** "You're one order away from [Silver] benefits"
- Educational content about their purchased categories

### Expected Business Value
High long-term value. Promising customers who cross into Loyal Customers add 3–5× their current LTV. Investment here is future-value protection.

---

## Segment 7: New Customers

### Who are they?
Customers who joined in the last 60 days OR have only 1–2 orders and high recency. They are in the critical first-purchase-to-second-purchase window.

### Behavioural Evidence
- 1–2 orders, recent
- Unknown long-term behaviour
- May be from paid acquisition campaigns
- Often have higher return rates (testing the brand)

### Churn Rate
Variable — 25–45%. The window between first and second order determines long-term retention.

### Retention Action
- **Day 3 post-purchase:** Usage tips for what they just bought
- **Day 10:** "How are you liking [Product X]?" — CSAT check, invite review
- **Day 20:** Product recommendation nudge: "Customers who bought X also love Y"
- **Day 25:** If no second order — low-friction offer: free sample with next order (not a discount)
- Onboarding email sequence: brand story, product education, community

### Expected Business Value
Second order conversion is the highest-leverage metric for this brand. Every % increase in second-order conversion rate compounds into significant revenue over a 12-month cohort.

---

## Segment 8: Dormant

### Who are they?
Low recency (R≤2, typically 60–180+ days since last order), low frequency, low monetary. These customers have largely disengaged. Some may have churned already.

### Behavioural Evidence
- Last order 90–180+ days ago
- Few lifetime orders (often 1–2)
- Low or zero app sessions recently
- May have had a single bad experience

### Churn Rate
Very high — 55–75%. Most of these customers are already churned in practice.

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

Assume a fixed campaign budget of 100 units (relative allocation).

| Priority | Segment | Budget Allocation | Rationale |
|----------|---------|-------------------|-----------|
| 1 | At-Risk High Value | **30 units** | Highest revenue risk; targeted personalised rescue |
| 2 | High Value Unhappy | **25 units** | High LTV at stake; requires support + retention |
| 3 | Promising | **15 units** | Future LTV investment; low cost, high return |
| 4 | New Customers | **15 units** | Second-order conversion is the highest-leverage action |
| 5 | Loyal Customers | **10 units** | Low-cost nurture; milestone rewards only |
| 6 | Discount Seekers | **3 units** | Value reframe only; no discounts |
| 7 | Champions | **2 units** | Recognition & referral only; no spend needed |
| 8 | Dormant | **0 units** | One suppression-ready email; no paid budget |

**Total: 100 units**

### Why At-Risk High Value gets priority over Champions
Champions are already safe. At-Risk High Value customers are in an active decay window — they were Champions or Loyal Customers recently and are sliding out. The expected value of rescuing one At-Risk High Value customer is higher than the marginal cost of recognising one Champion.

### Why Dormant gets near-zero budget
Win-back rates for dormant customers with 1–2 orders who have been silent for 90+ days are typically 2–5%. The cost-per-recovered-customer is extremely high relative to the LTV. Suppression from active campaign lists actually improves email deliverability for the other segments.

---

## Monitoring Recommendations

After deploying retention actions per segment:

1. Track **segment migration** monthly — what % of At-Risk moved to Loyal or Promising?
2. Track **second-order conversion rate** for New Customers (weekly)
3. Track **campaign response rate and order placed within 30 days** for At-Risk High Value
4. Track **average order value trend** for Discount Seekers — is the value reframe working?
5. **Recalculate RFM scores** every 30 days and re-assign segments — static segmentation decays quickly
