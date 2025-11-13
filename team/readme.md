insert text here
# Team README

Team Members: Max Matteucci, Ethan Lebon, Ian Hedges  
Project: MGMT 467 Unit 2, Predictive Modeling with BQML

## Summary
Our team built four models to evaluate survival predictions using logistic regression, engineered features, and cost-aware thresholding. Model A provided a solid baseline with simple manifest features. Model B showed clear improvements by adding engineered variables. Model C introduced cost-based thresholding for a high-risk segment, and Model D extended this approach across the full dataset with fairness checks.

## Sensitivity and Risk
A sensitivity analysis at thresholds of .25, .5, and .75 showed that false negatives are the most costly error. Lower thresholds improved recall and reduced overall cost, helping mitigate the risk of missing true survivors.

## Final Recommendation
We recommend the engineered model with a lower, cost-aware threshold because it offers the best balance of accuracy, recall, fairness, and operational safety.
