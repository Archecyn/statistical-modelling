# Shapiro-Wilk Normality Test

The Shapiro-Wilk test assesses whether a sample comes from a normally distributed population. It compares the sample to what would be expected under normality.

</br>

## Example:
Test normality of data: 2.1, 2.5, 2.8, 3.0, 3.2, 3.5, 3.8 (n=7). α = 0.05.

</br>

1. Define H<sub>0</sub> and H<sub>A</sub>   

    H<sub>0</sub>: Data is normally distributed  

    H<sub>A</sub>: Data is not normally distributed

</br>

2. Alpha    
 α = 0.05

</br>

3. Sort data: 2.1, 2.5, 2.8, 3.0, 3.2, 3.5, 3.8

</br>

4. Calculate mean and standard deviation  
    Mean x̄ = (2.1+2.5+2.8+3.0+3.2+3.5+3.8)/7 = 21.9/7 = 3.1286  
    SD s ≈ 0.58 (calculated from data)

</br>

5. Shapiro-Wilk W statistic (simplified calculation for small n)  
    W = [∑ a_i (x_{(n+1-i)} - x_{(i)})]² / ∑ (x_i - x̄)²  
    For n=7, coefficients a ≈ [0.547, 0.332, 0.234, 0.0, -0.234, -0.332, -0.547]  
    W ≈ 0.95 (actual calculation yields W ≈ 0.945)

</br>

6. Critical Value  
    For n=7, α=0.05, W<sub>critical</sub> ≈ 0.753

</br>

7. Decision  
    Since 0.945 > 0.753, fail to reject H<sub>0</sub>. Data appears normal.