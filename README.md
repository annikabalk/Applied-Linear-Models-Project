# Applied-Linear-Models-Project

# Final Project README  
**Title:** Investigating the Association Between Coronary Artery Calcification and CKD Progression  
**Author:** Annika Balk  
**Course:** MA678 – Applied Linear Models  
**Submission Date:** 12/10/2024

## Project Overview  
This project explores how coronary artery calcification (CAC) may be associated with the progression of Chronic Kidney Disease (CKD), with a particular focus on identifying whether CAC can be used as a predictor for end-stage renal disease. I worked with a dataset from the Harvard Dataverse, narrowing it down to 130 unique patients after removing duplicates that violated model assumptions.

## Methodology  
### 1. **Exploratory Data Analysis (EDA):**  
I started by identifying multicollinearity among organ-system-specific measures (like creatinine and urea), and used both correlation matrices and chi-square tests to support modeling decisions. I also created multiple visualizations to investigate the trends between CKD stages and cardiovascular indicators like CAC and coronary artery disease.

### 2. **Handling Missing Data:**  
About 25 eGFR values were missing—all from patients with early-stage CKD. Instead of using multiple imputation (which biased results toward more severe disease), I imputed using a uniform distribution within clinically normal eGFR ranges for Stage 1–2.

### 3. **Modeling Approach:**  
- **Multinomial Regression:**  
  Fit five models with CKD stage as the outcome, adjusting for confounders like age, sex, hypertension, obesity, and total cholesterol. CAC emerged as a strong predictor. The final model achieved 76.9% accuracy and a 52% reduction in residual deviance. I also justified the inclusion of an age-hypertension interaction using visualization.

- **Hierarchical Modeling:**  
  I used eGFR as a continuous outcome (log-transformed due to skewness) and built no/partial/complete pooling models treating CAC group as a hierarchical level. Partial pooling performed decent, but overall didn’t offer much beyond the multinomial model.

## Key Takeaways  
- CAC is significantly associated with advanced CKD stages.  
- Multinomial modeling provided stronger and more interpretable results than hierarchical models in this context.  
- While hierarchical modeling was a worthwhile exploration, CAC didn’t benefit from being treated as a group-level variable.  
- My findings align with current literature on the strong cardiovascular-kidney link—especially in later stages of disease progression.

## File Structure  
- `FinalReport_AnnikaBalk_678.pdf` – Full report with EDA, models, figures, assumptions, and references.  
- Appendix includes:  
  - Additional plots  
  - Assumption checks for log(GFR)  
  - Model diagnostics for hierarchical models

## References  
Key sources include recent publications in *JAMA Cardiology*, *Lancet*, and *Journal of the American Society of Nephrology*. Full list in the report.

## Closing Note  
Thank you for taking the time to read through this project. I hope to study more about chronic diseases in the future.