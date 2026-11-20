# ECON-3916-LAB17
# Classification: When 90% Accurate Is Worthless

## Objective

I used logistic regression to predict loan defaults and explored why accuracy alone can be misleading when classes are imbalanced.

## Methodology

- I worked with 6,000 simulated loan applications with a default rate of [YOUR VALUE].
- I compared the model against a baseline that approves every applicant, which had an accuracy of [YOUR VALUE].
- I fitted a logistic regression model and evaluated its accuracy and predicted defaults at the standard 0.5 classification threshold.
- I interpreted the model coefficients as log-odds and odds ratios to understand how each predictor affected the likelihood of default.
- I examined how an odds ratio of [YOUR VALUE] for one additional prior default translated into different probability changes depending on the starting probability.
- I calculated precision and recall across six classification thresholds to examine the trade-off between false positives and false negatives.
- I selected a classification threshold by minimizing the expected cost of prediction errors.
- I wrote a function called `precision_recall_at()` to calculate precision and recall at any chosen threshold.
- I compared the cost-minimizing threshold with the theoretical threshold derived from the error costs.

## Key Findings

- **Baseline accuracy:** Approving every applicant produced an accuracy of [YOUR VALUE], showing why a high accuracy score can be misleading when defaults are uncommon.
- **Logistic regression:** At the 0.5 threshold, my model achieved [YOUR VALUE] accuracy and predicted [YOUR VALUE] defaults.
- **Odds ratios:** One additional prior default had an odds ratio of [YOUR VALUE]. I found that the same odds ratio could produce different changes in predicted probability depending on the initial probability.
- **Precision and recall:** Changing the classification threshold affected the balance between identifying actual defaults and incorrectly flagging applicants who would repay.
- **Optimal threshold:** The threshold that minimized expected cost was [YOUR VALUE], compared with the closed-form threshold of [YOUR VALUE].
- **Expected cost:** The cost-minimizing threshold produced an expected cost of [YOUR VALUE] per applicant, compared with [YOUR VALUE] at the standard 0.5 threshold.
- **Performance at the closed-form threshold:** Precision was [YOUR VALUE] and recall was [YOUR VALUE].

## Conclusion

I learned that accuracy is not always a useful measure of classification performance, especially when one outcome is much more common than the other. In loan default prediction, the costs of different mistakes matter. Adjusting the classification threshold based on those costs can make a model more useful for actual lending decisions.

<!-- Optional extension, if completed:

## Calibration

I checked whether the model's predicted default probabilities matched observed default rates. My result was [YOUR RESULT].

-->
