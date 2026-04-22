# F-test

An F-test compares the variances of two populations or is used in ANOVA to test if group means are equal. Here, we demonstrate variance comparison.

</br>

## Example:
Two machines produce bolts. Sample variances: Machine A (n=10, s²=4), Machine B (n=12, s²=9). Test if variances are equal at α = 0.05.

</br>

1. Define H<sub>0</sub> and H<sub>A</sub>   

    H<sub>0</sub>: σ₁² = σ₂² (variances are equal)  

    H<sub>A</sub>: σ₁² ≠ σ₂² (variances differ)

</br>

2. Alpha    
 α = 0.05

</br>

3. Test Statistic  
    F = s₁² / s₂² = 4 / 9 = 0.444 (use larger variance in denominator if needed, but here it's fine)

</br>

4. Degrees of Freedom  
    df₁ = n₁ - 1 = 9, df₂ = n₂ - 1 = 11

</br>

5. Critical Value  
    F<sub>critical</sub> (0.05, 9, 11) ≈ 3.10 (two-tailed, check both tails)

</br>

6. Decision  
    Since 0.444 < 3.10, fail to reject H<sub>0</sub>. Variances are not significantly different.