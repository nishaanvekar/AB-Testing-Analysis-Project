# A/B Testing Analysis Python Project

## Overview
An e-commerce website tested two page variants to determine which drives higher user conversion. This analysis determines whether Variant B should replace Variant A.
This Project is performed on Google Colab (browsing site)
---

## Dataset

- 1,000 users | 500 Control (A), 500 Treatment (B)
- Features: Group, Device, Time Spent, Conversion (0/1)

---
## Sample Size Calculation
- Baseline conversion rate: 13%
- Minimum detectable effect: 2%
- Required sample size: ~1,000 per group
- Actual sample: 500 per group → Note: slightly underpowered
---

## Tools Used

* Python
* Pandas
* Seaborn
* Statsmodels

---

## Analysis Performed

* Conversion rate comparison
* Segmentation by device
* Z-test and P-value for statistical significance
* Uplift calculation
* Confidence interval estimation

---
## Key Results
| Metric | Variant A | Variant B |
|--------|-----------|-----------|
| Conversion Rate | 34.9% | 24.4% |
| Uplift | — | +39% relative |
| P-value | — | 0.032 |
| Significant? | — | Yes |

## Key Insights

* Variant B conversion rate: 34% vs Variant A: 24% — a 38.9% relative uplift.
* Uplift: +5.2 percentage points (p-value: 0.032, statistically significant at α=0.05)
* Mobile conversion: B=35.9% vs A=24.4% | Desktop conversion: B=29.8% vs A=25.6%"

## Hypothesis
**H0 (Null):** There is no significant difference in conversion rates between Variant A and Variant B.
**H1 (Alternate):** Variant B has a significantly higher conversion rate than Variant A.
**Significance Level:** α = 0.05
**Statistical Test:** Two-proportion Z-test

---
## Segmentation Insights
- Mobile: B outperforms A by +7.2pp
- Desktop: B outperforms A by +3.2pp


## Visuals

<img width="576" height="455" alt="image" src="https://github.com/user-attachments/assets/e5424334-ab71-4c41-9079-8083c8805403" />


## Conclusion

Variant B outperforms Variant A with a statistically significant uplift of +5.2pp (p=0.032). Mobile users show the strongest response (+7.2pp lift).

Recommendation: **Proceed with phased rollout** — launch Variant B to mobile users first (highest impact segment), monitor for 2 weeks, then expand to desktop if conversion holds above 15%.

Risk: Sample size (n=1000) is slightly below recommended (n=2400). Results are directionally strong but a 2-week extension would increase confidence.

---

## Project Structure

* data/
* notebooks/
* visuals/

---

## Author

Nisha Anvekar 
Data Analyst Project showcasing A/B testing & statistical analysis
