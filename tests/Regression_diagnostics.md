# Regression Diagnostics

Regression diagnostics evaluate model assumptions and fit, including residual analysis for linearity, homoscedasticity, normality, and outliers.

</br>

## Example:
Simple linear regression: y = 2x + 1 + error. Data: (1,4), (2,5), (3,8), (4,9), (5,12). Check residuals.

</br>

1. Fit model: ŷ = 2x + 1  
    Predicted: 3,5,7,9,11  
    Actual: 4,5,8,9,12  
    Residuals: 4-3=1, 5-5=0, 8-7=1, 9-9=0, 12-11=1

</br>

2. Residual plot: Plot residuals vs x or ŷ. Here, residuals are 1,0,1,0,1 – constant, suggesting homoscedasticity.

</br>

3. Normality of residuals: Shapiro-Wilk on residuals [1,0,1,0,1] – symmetric, likely normal.

</br>

4. Outliers: All residuals small, no obvious outliers.

</br>

5. R²: 1 - (SS_res / SS_tot) = 1 - (1+0+1+0+1)/ ( (4-8)^2 + ... ) ≈ 1 - 3/54 ≈ 0.944 (good fit)

</br>

6. Conclusion: Model assumptions met, good fit.