# SLO Document for UpCommerce

## Background
UpCommerce is a rapidly growing e-commerce platform that has been experiencing reliability challenges as it scales. The company has promised 99% uptime to its merchants but has no auto-scaling infrastructure or error budget. With a major marketing campaign planned for the next 12 months, the platform needs to establish proper SLOs to ensure reliability during increased traffic.

## SLO Table

| SLO Type | SLO | Service Level Indicator | Target | Remarks |
|----------|-----|------------------------|--------|---------|
| Request-Driven | Availability | Percentage of successful requests (2xx and 3xx responses) | 99% | This aligns with the uptime promise to merchants. |
| Request-Driven | Latency | Percentage of requests served within 100ms | 95% | Following SkyHorizonz.com's latency standard to remain competitive. |
| Pipeline | Product Upload | Percentage of product uploads completed within 2 hours | 99% | Addressing vendor complaints about 36-hour upload delays. |
| Storage | Customer Purchase History | Percentage of customer purchase history accessible for 24 months | 95% | Addressing loyalty program issues with 12-month limit. |

## Monthly Error Budget Calculation

To calculate the monthly error budget for the 99% uptime SLO:

- Total time in a month = 30 days × 24 hours × 60 minutes × 60 seconds = 2,592,000 seconds
- For a 99% uptime SLO, the allowable downtime (error budget) is: (100% - 99%) × 2,592,000 seconds
- Allowable downtime = 1% × 2,592,000 = 25,920 seconds per month
- This equals 25,920 seconds ÷ 60 = 432 minutes per month
- Or 432 minutes ÷ 60 = 7.2 hours per month

Therefore, UpCommerce has an error budget of 7.2 hours per month for the availability SLO.

## What to do with the Error Budget?

With the error budget of 7.2 hours per month (or 87.6 hours per year), the team can:

1. **Plan and schedule maintenance**: Use part of the error budget for planned maintenance windows, system updates, and feature releases without impacting the SLO.

2. **Manage incident response**: Allocate time for handling unexpected incidents and emergencies while still staying within the error budget.

3. **Implement feature releases**: Use some of the budget for deploying new features that might cause brief service disruptions.

4. **Enable safe experimentation**: Allow for canary deployments and A/B testing that might occasionally impact service availability.

## Why This is Useful for Service Reliability

Having an error budget is useful for service reliability because:

1. **Balances reliability with innovation**: It provides a framework for making trade-offs between stability and feature development, allowing for controlled risk-taking.

2. **Enables data-driven decision making**: Teams can make informed decisions about when to prioritize reliability improvements versus feature development based on actual vs. budgeted error consumption.

3. **Creates accountability**: Teams are held accountable for staying within the error budget, promoting more careful planning and implementation of changes.

4. **Improves customer satisfaction**: By managing the error budget, teams can ensure they meet their service commitments to customers while still delivering ongoing improvements.

5. **Facilitates capacity planning**: Understanding the error budget helps with planning infrastructure improvements and scaling efforts to meet growing demand, which is crucial for UpCommerce's upcoming marketing campaign.