# House Price Prediction & Real Estate Valuation Analysis

A machine learning project designed to identify the key spatial, structural, and amenity-based drivers of property valuation. This repository includes data analysis, feature correlation evaluation, model performance comparisons (**Linear Regression vs. Random Forest**), and strategic recommendations for real estate stakeholders.

---

## Executive Summary

Predictive modeling reveals that **spatial and structural attributes** dominate property valuations, with total area, bathroom count, and air conditioning serving as the strongest pricing predictors. 

While both Linear Regression and Random Forest models accurately predict standard property values, the **Random Forest Regressor** demonstrates superior precision when evaluating high-end, luxury properties subject to non-linear price scaling. Additionally, market data highlights that traditional infrastructure (like hot water heating) offers minimal pricing leverage, whereas completely unfurnished properties face significant market discounts.

---

## Key Insights 

### 1. Which features influence house prices the most?
* **Space and Capacity Rule the Market:** Mathematical correlation and model feature weights confirm that **Total Area (0.54 correlation)** and **Number of Bathrooms (0.52 correlation)** provide the highest predictive leverage.
* **Essential vs. Desirable:** While **Air Conditioning (0.45 correlation)** serves as a strong premium upgrade, physical space and operational capacity remain the baseline, non-negotiable metrics buyers evaluate first.

### 2. How accurate are the predictive models?
* **Baseline Accuracy:** Both models reliably estimate standard market valuations for typical residential properties.
* **Linear Regression vs. Random Forest:** The Random Forest model was selected for optimal deployment. It successfully captures non-linear feature interactions (e.g., multi-story layouts paired with modern split-unit ACs), which exponentially increase a property's value beyond simple additive linear estimates.

### 3. What were the most surprising findings in the data?
* **Minimal Infrastructure Pricing Impact:** **Hot Water Heating (0.09 correlation)** showed almost no independent correlation with property price. Modern buyers view basic infrastructure as a standard requirement rather than a premium value driver.
* **The "Unfurnished" Discount:** Properties listed as completely **Unfurnished (-0.28 correlation)** suffer a substantial valuation penalty compared to furnished or semi-furnished alternatives.

---

## Feature Correlation Matrix Summary

| Feature Category | Attribute | Correlation with Price | Market Value Impact |
| :--- | :--- | :---: | :--- |
| **Spatial / Capacity** | Total Area | `0.54` | Primary Value Driver |
| **Spatial / Capacity** | Number of Bathrooms | `0.52` | Baseline Non-Negotiable |
| **Amenities** | Air Conditioning | `0.45` | High-Yield Premium Upgrade |
| **Amenities** | Parking Spaces | `0.38` | Significant Valuation Boost |
| **Infrastructure** | Hot Water Heating | `0.09` | Negligible Independent Impact |
| **Furnishing Status** | Unfurnished | `-0.28` | Heavy Market Penalty |

---

## Strategic Recommendations for Real Estate

1. **Focus on High-ROI Upgrades Over Full Renovations:** Rather than spending heavily on structural overhauls, property developers and agents should prioritize installing efficient split-unit **Air Conditioning** and paving/defining **Parking Spaces** before listing. These updates are relatively inexpensive yet yield high valuation returns.
2. **Mitigate the Unfurnished Penalty:** Agents should advise sellers to stage or partially furnish vacant properties to eliminate the steep pricing penalty associated with completely unfurnished listings.
3. **Deploy Non-Linear Models for Luxury Listings:** Valuation platforms evaluating multi-feature properties should utilize ensemble methods (Random Forest) over standard linear regressions to avoid underpricing high-tier properties.

---

## Data Pipeline & Tech Stack

* **Language:** Python 3.8+
* **Data Processing & Analysis:** `pandas`, `numpy`
* **Machine Learning:** `scikit-learn` (OneHotEncoder, Linear Regression, Random Forest Regressor)
* **Metrics:** MAE, RMSE, R2 Score
* **Visualization:** `matplotlib`, `seaborn`

---
