# Invistico_Airline
Project Report

1. Executive Summary & Business Recommendations
Example Data-Backed Argument: "Analysis of the model coefficients reveals that Inflight entertainment and Seat comfort have the strongest positive coefficients. Conversely, Departure/Arrival time convenience had lower statistical impact. Therefore, instead of spending capital altering flight schedules, the airline should prioritize upgrading cabin interiors. Specifically, moving an average user's Inflight Wi-Fi rating from a 2 to a 4 increases their overall satisfaction likelihood drastically."

2. The True Positive vs. False Positive Trade-off
False Positive Cost: Predicting a customer is satisfied when they aren't. Risk: The airline ignores them, but they churn and switch to a competitor.

False Negative Cost: Predicting a customer is dissatisfied when they are actually happy. Risk: The airline spends unnecessary retention marketing/vouchers on someone already loyal.

Report Note: Since retaining a customer is cheaper than acquiring a new one, maximizing Recall (catching every unhappy customer) is often prioritized over Precision here.

3. Model Limitations & Deployment Next Steps
Limitations: Logistic regression assumes a linear relationship between log-odds of the features and the target. It might miss complex, non-linear interactions (e.g., long flight distances making bad seat comfort feel exponentially worse).

