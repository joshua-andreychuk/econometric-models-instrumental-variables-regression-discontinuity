# econometric-models-instrumental-variables-regression-discontinuity

# **Econometric Models: Instrumental Variables and Regression Discontinuity Analysis with Stata**

This project applies various **econometric models** and **causal inference techniques** using **Stata** to analyze demand estimation and sales impacts based on Yelp ratings. The objectives include addressing endogeneity using **instrumental variables** and applying **regression discontinuity (RD)** models to evaluate how changes in star ratings affect restaurant sales.

---

## **Technologies Used**

- **Stata**:  
  Statistical software used to perform 2SLS regression, regression discontinuity, and other econometric analyses.

- **Instrumental Variables (IV) Regression (Causal Inference Technique)**:  
  Addresses endogeneity by using external instruments that are correlated with the endogenous variable but not directly with the outcome.

- **Regression Discontinuity (RD) (Causal Inference Technique)**:  
  Exploits cutoff points in a continuous variable to estimate local causal effects by comparing observations near the threshold.

---

## **Project Overview**

### **1. Demand Estimation for Coffee (IV Analysis)**
- **Goal**: Estimate the causal effect of price on coffee demand, accounting for potential endogeneity.
- **Causal Inference Technique**: Instrumental variables (IV) regression using **FuelCost** and **LandCost** as instruments for Price.
  
- **Key Findings**:
  - The IV regression yields a coefficient of **-8.34** for Price, indicating that a $1 increase in coffee price decreases quantity sold by approximately 8.34 units.
  - The instruments satisfy the relevance condition (significant correlation with Price) and are assumed to meet the exogeneity condition.

---

### **2. Impact of Yelp Ratings on Restaurant Sales (RD Analysis)**
- **Goal**: Assess the causal impact of changes in Yelp star ratings on restaurant sales.
- **Causal Inference Technique**: Regression discontinuity (RD) analysis using **average Yelp rating** as the forcing variable and **sales** as the outcome.

- **Key Findings**:
  - **1 to 2 Stars**: A tendency for higher sales exists, though the result is not statistically significant at the 95% confidence level.
  - **2 to 3 Stars** (bandwidth: 0.75): Statistically significant increase in sales.
  - **3 to 4 Stars**: No statistically significant change in sales.
  - **4 to 5 Stars** (bandwidth: 0.75): Statistically significant increase, with the greatest observed impact at approximately **$2,540.60**.

---

## **Data Overview**

The project uses two datasets:

1. **Coffee Sales Data**:  
   Contains information on **QuantitySold**, **Price**, and potential instruments (**FuelCost** and **LandCost**), used for the demand estimation analysis.

2. **Yelp Ratings Data**:  
   Tracks **sales**, **average Yelp ratings**, and **Yelp stars** for a sample of restaurants, used for the regression discontinuity analysis.

---

## **Results Summary**

### **Instrumental Variables Analysis**
- Price has a significant negative impact on quantity sold when controlling for endogeneity.
- The IV model confirms the relevance and presumed exogeneity of the instruments.

### **Regression Discontinuity Analysis**
- Sales show statistically significant increases at certain Yelp rating thresholds (e.g., 4 to 5 stars).
- Results highlight the importance of improving ratings to increase restaurant sales.
