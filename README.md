# HXAI
HXAI: Privacy Preserving Hierarchical Explainable Artificial Intelligence



# README: Experiment Section for HXAI

## Overview
This section evaluates the Hierarchical Explainable AI (HXAI) framework's ability to balance privacy, utility, and explainability in smart home energy management. The experiments assess how privacy-preserving mechanisms, including differential privacy, affect both local and zonal analyses and explore how specific and multiple queries are handled while safeguarding household privacy.

## Dataset
- **Households:** 50 smart homes, each with 7 appliances.
- **Appliances:** Heating, Fridge, Fan, Oven, Washing Machine, Dryer, Cooler.
- **Data Points:** 100 time points per household.
- **Energy Consumption Data:** Generated using utility models for actual appliance service ranges.

## Experimental Setup
The experiments are designed to demonstrate:
1. **Local (End) Level Analysis:** Provide households with noise-free SHAP explanations of their energy consumption.
2. **Zonal (Edge) Level Analysis:** Evaluate how privacy-preserving Laplace noise affects zonal energy consumption insights for electricity providers.
3. **Specific and Multiple Query Handling:** Assess the privacy-utility trade-offs for individual and aggregated queries, showing the impact of repeated queries on privacy leakage.

## Key Experiments

### 1. Local (End) Level Analysis:
- Households receive detailed SHAP-based explanations, helping them optimize appliance usage to reduce energy costs.
- For example, a washing machine's SHAP values can show a wide range of energy impact depending on usage, helping the household schedule it during off-peak hours.

### 2. Zonal (Edge) Level Analysis:
- Privacy-preserving noise is applied to aggregate zonal data to protect household-level details while maintaining the utility for energy providers.
- SHAP reports are generated with and without noise, demonstrating minimal utility loss despite privacy protections.

### 3. Specific Query Handling:
- Specific queries demand higher utility and thus a larger privacy budget compared to general queries.
- Example: A query such as "What percentage reduction in washing machine and cooler consumption occurs after a price drop in a 30 km radius?" aggregates data across households. The noisy SHAP report provided ensures that individual households' data is anonymized, protecting their privacy.
- The experiment shows that while privacy-preserving noise affects the precise values of energy consumption contributions, the general trends and rankings of appliance usage remain intact, allowing the energy provider to make informed decisions without compromising individual privacy.

### 4. Multiple Query Handling:
- The experiment simulates multiple specific queries sent to households over time, demonstrating how privacy leakage accumulates with each query.
- As more specific queries are made (e.g., repeated requests for appliance-level data), the cumulative privacy leakage increases non-linearly. Once the leakage exceeds the privacy threshold (ε), households stop responding to further queries, preserving their privacy.
- This emphasizes the importance of managing query frequency to balance privacy and utility. The system is designed to block further queries once a household’s privacy budget is exhausted, preventing excessive data exposure.

### 5. Privacy-Utility Trade-off:
- The experiments explore how varying the privacy budget (ε) impacts the accuracy of energy predictions.
- A negotiation process allows for a balance between privacy and utility. For instance, ε = 6.73 is found to provide an optimal balance, where the energy provider retains useful insights without breaching household privacy.
- The HXAI framework enables energy providers to implement appliance upgrade schemes based on zonal insights, driving energy efficiency without compromising individual privacy.

## Conclusion
The HXAI framework successfully balances privacy and utility by using differential privacy in response to both specific and multiple queries. The results demonstrate that privacy-preserving mechanisms can protect individual households’ data while still providing actionable insights for grid management and energy cost reductions.



