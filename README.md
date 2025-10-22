# SRE Fundamentals Task Completion Summary

## Task Overview
- Created a new folder named "SRE_FUNDAMENTALS_WITH_GOOGLE"
- Developed an SLO document for UpCommerce based on the provided scenario
- Calculated the monthly error budget as required
- Explained the utility of the error budget for service reliability

## Files Created
1. upcommerce_slo_document.md - Contains the complete SLO document with:
   - SLO table with SLO types, indicators, and targets
   - Correct error budget calculation
   - Explanation of how to use the error budget
   - Justification of why error budgeting is useful for service reliability

## Key SLOs Established for UpCommerce:
- Request-Driven: 99% availability
- Request-Driven: 95% of requests served within 100ms
- Pipeline: 99% of product uploads completed within 2 hours
- Storage: 95% of customer purchase history accessible for 24 months

## Error Budget Calculation:
- 99% uptime SLO = 7.2 hours of allowable downtime per month
- This provides a framework for managing system reliability vs. feature development trade-offs