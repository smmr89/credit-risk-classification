# **Credit Risk Analysis Report**

## Overview

Credit risk introduces an inherent imbalance in classification, given the prevalence of healthy loans over risky ones.

This analysis serves to gauge the model's ability to proficiently differentiate between healthy and risky loans.

The labeled dataset encompasses key variables like loan size, interest rate, borrower's income, debt-to-income ratio, account count, derogatory marks, and total debt. These factors collectively contribute to predicting the loan status, categorizing it as either a sound loan (value = 0) or a high-risk loan (value = 1).

A logistic regression model is run to make predictions based on training data. Furhter, a second model using resampled data from a random over sampling technique is used to improve the results. The results and a summary recommendation is presented below.

## Accuracy, Prescision and Recall Scores

- <u>Logistic Regression Model</u>

    | [balanced accuracy = 0.95] | precision | recall |
    |----------------------------|-----------|--------|
    | healthy loan               |    1.00   |  0.99  |
    | high-risk loan             |    0.85   |  0.91  |

    Confusion Matrix

    |               | Predicted Healthy | Predicted High-risk |
    |---------------|-------------------|---------------------|
    | Actual Healthy|       18663       |          102        |
    | Actual High-risk|       56        |          563        |


- <u>Logistic Regresion Model with Random Over Sampler</u>

    | [balanced accuracy = 0.99] | precision | recall |
    |----------------------------|-----------|--------|
    | healthy loan               |    1.00   |  0.99  |
    | high-risk loan             |    0.84   |  0.99  |

    Confusion Matrix

    |               | Predicted Healthy | Predicted High-risk |
    |---------------|-------------------|---------------------|
    | Actual Healthy|       18649       |          116        |
    | Actual High-risk|        4         |          615        |


## Summary

<u>Recommendation:</u>
Model 2, the Logistic Regression Model with Random Oversampler, outperforms Model 1 in terms of balanced accuracy (0.99 vs. 0.95) and recall for high-risk loans (0.99 vs. 0.91). This suggests that the oversampling technique has effectively improved the model's ability to correctly identify high-risk loans. However, it's essential to consider the trade-offs, especially in precision for high-risk loans, which decreased slightly from 0.85 to 0.84.

<u>Conditions/Caveats for Recommendation:</u>

Consider the Business Context: Assess the relative importance of precision and recall based on the business context. For example, in scenarios where the cost of missing a high-risk loan is high, prioritizing recall might be crucial.

Resource and Computational Costs: Oversampling techniques can be computationally expensive. Consider the resource implications and the feasibility of implementation in a production environment.

In summary, while Model 2 appears to offer improved performance, the final decision should be made based on a careful consideration of business priorities, resource constraints, and the specific goals of the machine learning project.