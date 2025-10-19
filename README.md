# Coupon Acceptance Analysis

## Project Overview

This project analyzes customer behavior regarding coupon acceptance using data from the UCI Machine Learning repository. The analysis focuses on understanding the factors that influence whether drivers accept coupons delivered to their mobile devices while driving.

**Dataset**: Survey data collected via Amazon Mechanical Turk describing different driving scenarios including destination, time, weather, passengers, and coupon types.

**Notebook**: [prompt.ipynb](./prompt.ipynb)

## Key Findings

### Overall Acceptance Rate

- **56.84%** of all coupons were accepted across the dataset

### Bar Coupon Analysis

- **41.00%** acceptance rate for bar coupons specifically
- **Key insights**:
  - Frequent bar-goers (>3 times/month): **76.88%** acceptance rate
  - Infrequent bar-goers (≤3 times/month): **37.06%** acceptance rate
  - Drivers over 25 who visit bars >1/month: **69.52%** acceptance rate
  - Drivers with no kids, non-farming occupation, and frequent bar visits: **71.32%** acceptance rate

### Coffee House Coupon Analysis

- **49.92%** overall acceptance rate for coffee house coupons
- **Key insights**:
  - Frequent coffee house visitors (>3 times/month): **67.50%** acceptance rate
  - Infrequent visitors (≤3 times/month): **44.94%** acceptance rate
  - Acceptance by passenger type:
    - With friends: **59.69%**
    - With partner: **57.05%**
    - With kids: **48.31%**
    - Alone: **43.79%**

## Data Quality Issues Addressed

- Removed `car` column (99.15% missing data)
- Filled missing values in venue frequency columns with 'unknown'
- Maintained data integrity for analysis

## Recommendations

### For Bar Coupons

1. **Target frequent bar-goers**: Focus marketing efforts on users who visit bars more than 3 times per month
2. **Age consideration**: Prioritize users over 25 years old for bar coupon campaigns
3. **Passenger context**: Avoid targeting drivers with children for bar coupons

### For Coffee House Coupons

1. **Social context matters**: Target users driving with friends or partners
2. **Frequency-based targeting**: Focus on users who visit coffee houses more than 3 times per month
3. **Time optimization**: Consider time-of-day patterns for coupon delivery

### General Recommendations

1. **Behavioral targeting**: Use historical visit frequency as a primary targeting criterion
2. **Contextual awareness**: Consider passenger type and driving destination
3. **Segmented campaigns**: Develop different strategies for different coupon types

## Next Steps

1. **Expand analysis**: Investigate other coupon types (restaurants, carry-out) using similar methodology
2. **Weather analysis**: Examine how weather conditions affect acceptance rates
3. **Time-based patterns**: Analyze optimal times for coupon delivery
4. **Machine learning model**: Develop predictive models for coupon acceptance
5. **A/B testing**: Implement targeted campaigns based on findings

## Technical Implementation

- **Libraries used**: pandas, seaborn, matplotlib, numpy
- **Data preprocessing**: Missing value handling, categorical grouping
- **Visualizations**: Bar plots, histograms, heatmaps for data exploration
- **Statistical analysis**: Acceptance rate comparisons across different customer segments
