<img width="889" height="490" alt="inflight entertaimrnt rating" src="https://github.com/user-attachments/assets/dbee577e-edeb-46e3-8b54-7fa351142d03" />
<img width="527" height="393" alt="Confusion matrix" src="https://github.com/user-attachments/assets/2266a79a-7d96-41f6-b638-f365ba4a7015" />
Based on the coefficients and odds ratios, the model has provided distinct clues about what truly drives passenger satisfaction. Here is the comprehensive project interpretation and business breakdown.
​1. Interpretation of Key Drivers (Coefficients & Odds Ratios)
​In Logistic Regression, positive coefficients (and Odds Ratios > 1) increase the likelihood of a passenger being satisfied. Negative coefficients (and Odds Ratios < 1) heavily drag down satisfaction. Because you scaled your continuous features, we can compare these impacts directly.
The Heaviest Negative Drivers (Detractors)
​Disloyal Customers (Coef: -1.8906, Odds Ratio: 0.1510): This is the strongest single predictor in your model. A disloyal customer has roughly 85% lower odds of being satisfied compared to a loyal customer, holding all else constant.
​Travel Class & Type (Class_Eco: -0.7256, Class_Eco Plus: -0.7751, Personal Travel: -0.7581): Flying Economy or Economy Plus, or traveling for personal reasons instead of business, significantly slashes the odds of satisfaction by more than 50% across the board.
The Heaviest Positive Drivers (Promoters)
​Inflight Entertainment (Coef: 0.9736, Odds Ratio: 2.6475): This is your ultimate operational lever. For every standard deviation increase in satisfaction with inflight entertainment, a passenger is 2.65 times more likely to report an overall satisfied trip.
​Physical & Service Comforts: Seat comfort (Odds Ratio: 1.50) and On-board service (Odds Ratio: 1.49) follow closely. Upgrading the physical cabin comfort and flight attendant training directly scales positive outcomes.
​Surprising Metrics
​Inflight Wi-Fi Service (Coef: -0.1202): Interestingly, Wi-Fi has a slightly negative coefficient here. This often indicates a suppressor effect in survey data—passengers might only heavily notice or rate Wi-Fi when it fails, or it strongly correlates with another feature (like Online Booking).
2. Strategic Business Recommendations
​Based on these data-backed insights, the airline should shift its strategies from generic improvements to highly targeted interventions:
Prioritize Inflight Entertainment & Cabin Experience: Since Inflight Entertainment is the strongest positive operational driver, upgrading the media catalog, screens, and headphone quality yields the highest return on investment (ROI) for customer satisfaction. Pairing this with seat comfort upgrades creates a potent baseline experience.
​Targeted Loyalty Retention Programs: Because "Disloyal Customers" are overwhelmingly dissatisfied, the airline should focus marketing and operational efforts on converting first-time or casual flyers into loyalty program members immediately upon booking.
​Differentiate the Economy Experience: Traveling in Economy/Eco Plus or for Personal Travel strongly correlates with dissatisfaction. The airline needs to figure out what pain points exist specifically in the back of the aircraft (e.g., legroom, boarding priority) to narrow the satisfaction gap between business and leisure travelers.
​3. Model Limitations & Next Steps
​Before deployment, consider these constraints to communicate to stakeholders:
​Survey Subjectivity: Survey responses (1-5 scales) are inherently subjective. What one passenger considers "3-star seat comfort," another might consider "4-star."
​Multicollinearity: Features like Departure Delay and Arrival Delay are highly correlated. While the model handles them, collinear features can sometimes make individual coefficients bounce around or behave counterintuitively (like the slight positive coefficient for departure delay).
​Deployment Next Steps: To deploy this model, save the pipeline (including the StandardScaler weights and the LogisticRegression coefficients) using a library like pickle or joblib. This allows the airline's backend infrastructure to score passenger satisfaction probabilities in real-time as they complete flights.
