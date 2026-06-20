# KPI and Experiment Analysis Project

## Business Context

This project assesses whether a redesigned onboarding experience delivers better business outcomes compared to the existing process. Users were split into a Control group and a Treatment group, and key performance metrics were examined to measure the impact of the new onboarding flow.

---

## Dataset Description

The dataset contains user-level experiment data covering:

* User ID
* Experiment Group
* Region
* Device Type
* Traffic Source
* Plan Type
* Landing Page Visit Status
* Trial Start Status
* Onboarding Completion Status
* Paid Conversion Status
* Revenue (30 Days)
* Support Tickets (30 Days)
* Refund Request Status
* Days to Convert
* Engagement Score

Total Users: 1,408

* Control Group: 693
* Treatment Group: 715

---

## North Star Metric Selected

**Paid Conversion Rate**

Formula:

Paid Conversion Rate = Converted Users / Total Users

This metric was chosen because the core purpose of the onboarding experience is to turn users into paying customers.

---

## KPI Tree Summary

### North Star Metric

* Paid Conversion Rate

### Primary KPIs

* Landing Page Visit Rate
* Trial Start Rate
* Onboarding Completion Rate
* Paid Conversion Rate
* Revenue per User

### Supporting KPIs

* Engagement Score
* Days to Convert
* Revenue per Converted User

### Guardrail Metrics

* Refund Rate
* Support Ticket Rate
* Revenue Quality

KPI tree diagram saved as:

* outputs/kpi_tree.png

---

## Experiment Analysis Approach

The analysis covered the following steps:

1. Missing value checks
2. Group balance validation
3. Duplicate user ID checks
4. Invalid binary value checks
5. Revenue outlier review
6. Segment distribution analysis
7. Experiment metric comparison
8. Segment-level analysis
9. Hypothesis testing
10. Guardrail metric evaluation

---

## Hypothesis Test Summary

### Test Performed

Two-Sample t-Test Assuming Unequal Variances

### Results

* Control Conversion Rate: 3.17%
* Treatment Conversion Rate: 6.99%
* Improvement: 120.5%
* P-value (Two-Tail): 0.00107

### Decision

The p-value fell below the significance threshold of 0.05.

As a result, the Null Hypothesis was rejected and the Treatment onboarding experience was found to produce a statistically significant uplift in Paid Conversion Rate.

---

## Guardrail Metrics Considered

### Refund Rate

* Control: 0.00%
* Treatment: 0.42%

### Support Ticket Rate

* Control: 14.72%
* Treatment: 24.76%

### Revenue Quality

* Control: 1630.10
* Treatment: 770.41

### Engagement Score

* Control: 57.03
* Treatment: 62.93

### Average Days to Convert

* Control: 8.86
* Treatment: 6.40

The primary concern identified was a rise in support ticket volume under the Treatment group.

---

## Final Recommendation

### Recommendation: Launch

The Treatment onboarding experience is recommended for full launch.

Supporting evidence:

* Paid Conversion Rate grew from 3.17% to 6.99%.
* Statistical testing validated the significance of the result.
* User engagement showed improvement.
* Revenue per user increased.
* Users converted in less time.
* Positive outcomes were observed across the majority of segments.

---

## Assumptions and Limitations

### Assumptions

* Users were randomly distributed across experiment groups.
* Conversion events were recorded accurately.
* Revenue figures represent valid and legitimate transactions.

### Limitations

* Long-term user retention was not part of this analysis.
* Customer lifetime value data was not available.
* Findings are based on a single experiment dataset.
* Revenue quality should be actively monitored following rollout.

---

## Screenshots Included

* screenshots/summary_metrics.png
* screenshots/hypothesis_test_output.png
* screenshots/kpi_tree_preview.png

---

## Deliverables

### Analysis

* experiment_analysis.xlsx
* hypothesis_test_notes.md

### Outputs

* kpi_tree.png
* experiment_summary.xlsx
* recommendation_memo.md

### Screenshots

* summary_metrics.png
* hypothesis_test_output.png
* kpi_tree_preview.png

---

## Conclusion

The Treatment onboarding experience produced a meaningful improvement in Paid Conversion Rate and overall user engagement. Statistical testing confirmed that the observed gains were not attributable to chance. Based on the experiment results, guardrail analysis, and segment-level findings, the Treatment experience is strongly recommended for rollout.
