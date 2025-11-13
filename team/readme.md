# Team README 🚢📊

**Team Members:** Max Matteucci, Ethan Lebon, Ian Hedges  
**Project:** MGMT 467 Unit 2, Predictive Modeling with BQML

## Summary 📈
We built four models to evaluate survival predictions using logistic regression, engineered features, and cost-aware thresholding. Model A provided a solid baseline with manifest features. Model B improved performance with engineered variables. Model C added cost-based thresholding for a high-risk segment, and Model D extended this thresholding across the full dataset with fairness checks.

## Sensitivity and Risk ⚠️
Our sensitivity analysis at thresholds of .25, .5, and .75 showed that false negatives are the most costly error. Lower thresholds improved recall and reduced total cost, helping mitigate the risk of missing true survivors.

## Final Recommendation ✅
We recommend the engineered model with a lower, cost-aware threshold because it provides the best balance of accuracy, recall, fairness, and operational safety.
