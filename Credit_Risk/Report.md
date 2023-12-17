# **Credit Risk Analysis Report**

## Overview

Credit risk introduces an inherent imbalance in classification, given the prevalence of healthy loans over risky ones.

This analysis serves to gauge the model's ability to proficiently differentiate between healthy and risky loans.

The labeled dataset encompasses key variables like loan size, interest rate, borrower's income, debt-to-income ratio, account count, derogatory marks, and total debt. These factors collectively contribute to predicting the loan status, categorizing it as either a sound loan (value = 0) or a high-risk loan (value = 1).

Mention the steps..

------

## Accuracy, Prescision and Recall Scores

- Logistic Regression Model

    | [balanced accuracy = 0.95] | precision | recall |
    |----------------------------|-----------|--------|
    | healthy loan               |    1.00   |  0.99  |
    | high-risk loan             |    0.85   |  0.91  |

- Logistic Regresion Model with Random Over Sampler

    | [balanced accuracy = 0.99] | precision | recall |
    |----------------------------|-----------|--------|
    | healthy loan               |    1.00   |  0.99  |
    | high-risk loan             |    0.84   |  0.99  |

## Summary

