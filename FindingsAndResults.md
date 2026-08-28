# Findings and Conclusions

## Model Performance Summary

All four models demonstrated the ability to predict hotel booking cancellations; however, performance varied across algorithms.

- Logistic Regression provided a strong baseline model and demonstrated that cancellation behavior could be predicted using historical booking information.
- Decision Tree produced interpretable results but showed lower overall predictive performance compared to ensemble methods.
- Gradient Boosting improved predictive accuracy by capturing more complex relationships within the data.
- Random Forest achieved the strongest overall performance and was selected as the final model.

The final Random Forest model achieved:

- ROC-AUC: 0.906 (Test Set)
- Cross-Validated ROC-AUC: 0.8994
- Optimal Parameters:
  - Number of Trees (n_estimators): 200
  - Maximum Tree Depth (max_depth): None

The model demonstrated a strong ability to distinguish between canceled and non-canceled reservations while maintaining good generalization performance across validation folds.

---

## Validation of Assumptions

Several assumptions identified during exploratory data analysis were confirmed through predictive modeling.

### Assumption 1: Longer Lead Times Increase Cancellation Risk

Analysis indicated that bookings made significantly in advance were more likely to be canceled than reservations made closer to arrival. Longer lead times allow more opportunities for travel plans to change.

**Result:** Supported.

### Assumption 2: Deposit Policies Influence Cancellation Behavior

Reservations with non-refundable deposits demonstrated significantly lower cancellation rates than reservations with no deposit requirements.

**Result:** Supported.

### Assumption 3: Booking Source Affects Cancellation Likelihood

Reservations originating from Online Travel Agencies (OTAs) showed higher cancellation rates than direct bookings, suggesting that channel-specific booking behavior influences cancellation risk.

**Result:** Supported.

### Assumption 4: Customer Booking History is Predictive

Customers with previous cancellations were more likely to cancel future reservations, indicating that historical behavior is an important predictor of future actions.

**Result:** Supported.

---

## Business Impact Analysis

Hotel booking cancellations create significant operational and financial challenges, including:

- Lost room revenue
- Occupancy forecasting uncertainty
- Staffing inefficiencies
- Inventory management challenges
- Revenue forecasting inaccuracies

The predictive model developed in this project enables hotel management to identify high-risk reservations before arrival, allowing proactive intervention strategies to reduce potential revenue loss.

Example business scenario:

- Average booking value = $150
- High-risk reservations identified annually = 1,000
- Successful intervention rate = 10%

Estimated annual revenue preservation:

**1,000 × 10% × $150 = $15,000**

This example is intentionally conservative. Large hotel chains processing tens of thousands of reservations annually could realize substantially greater financial benefits from predictive cancellation management.

Additional benefits include:

- Improved occupancy forecasting
- Better workforce planning
- More accurate inventory allocation
- Stronger revenue management strategies
- Improved customer retention efforts

---

## Practicality for Business Use

The proposed solution is highly practical because all required model inputs are already collected during the reservation process.

Key variables include:

- Lead time
- Market segment
- Distribution channel
- Deposit type
- Customer history
- ADR (Average Daily Rate)
- Special requests
- Room information

Because these features already exist within reservation systems, implementation would require minimal additional data collection.

Potential applications include:

- Real-time cancellation risk scoring
- Automated customer retention campaigns
- Dynamic overbooking strategies
- Revenue management optimization
- Occupancy forecasting support

The model provides a scalable and cost-effective approach for improving operational efficiency and reducing uncertainty associated with booking cancellations.

---

# Lessons Learned and Recommendations

## Lessons Learned

Several important insights emerged throughout the project.

### Data Quality Matters

Cleaning missing values, removing duplicate records, and preparing the dataset appropriately had a significant impact on model performance. High-quality data served as the foundation of an effective predictive solution.

### Feature Engineering Improves Results

Creating new variables such as:

- Total Guests
- Total Nights
- Family Booking Indicator
- Lead Time Category
- Booking Season

helped capture customer behavior patterns and improved predictive performance.

### Historical Behavior Predicts Future Behavior

Customer booking characteristics and previous reservation behavior provided valuable insight into cancellation risk. Factors such as lead time, deposit type, and prior booking activity were particularly influential.

### Model Selection Matters

While all four models provided useful predictive capability, Random Forest delivered the strongest overall performance and demonstrated the best balance between accuracy and reliability.

### Business Understanding Is Essential

The most valuable outcome of this project was not simply predicting cancellations, but identifying actionable trends that hotels can use to improve planning, forecasting, and customer retention efforts.

---

## Recommendations

Based on the results of this analysis, the following recommendations are proposed.

### Focus on Long Lead-Time Reservations

Reservations made far in advance should receive additional monitoring and customer outreach because they are more likely to be canceled.

### Develop Targeted Retention Campaigns

Customers identified as high risk should receive:

- Reservation reminders
- Personalized offers
- Loyalty incentives
- Flexible booking modification options

### Review Deposit Policies

Deposit requirements appear to influence customer commitment and may help reduce cancellation 

---
# References

Antonio, N., de Almeida, A., & Nunes, L. (2019). *Hotel Booking Demand Datasets*. Data in Brief, 22, 41–49.

Breiman, L. (2001). *Random Forests*. Machine Learning, 45(1), 5–32.

Han, J., Kamber, M., & Pei, J. (2011). *Data Mining: Concepts and Techniques*.

James, G., Witten, D., Hastie, T., & Tibshirani, R. (2021). *An Introduction to Statistical Learning*.

Kaggle. *Hotel Booking Demand Dataset*. https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand

Scikit-Learn Documentation. https://scikit-learn.org

Wirth, R., & Hipp, J. (2000). *CRISP-DM: Towards a Standard Process Model for Data Mining*.