# Levene's Test for Homogeneity of Variances

Levene's test checks if variances are equal across groups, a key assumption for ANOVA. It uses absolute deviations from group medians.

</br>

## Example:
Three groups: A [10,12,14], B [8,10,12], C [9,11,13]. Test equal variances at α = 0.05.

</br>

1. Define H<sub>0</sub> and H<sub>A</sub>   

    H<sub>0</sub>: σ₁² = σ₂² = σ₃² (variances are equal)  

    H<sub>A</sub>: At least one variance differs

</br>

2. Alpha    
 α = 0.05

</br>

3. Calculate group medians and absolute deviations  
    Group A: median=12, deviations: |10-12|=2, |12-12|=0, |14-12|=2  
    Group B: median=10, deviations: |8-10|=2, |10-10|=0, |12-10|=2  
    Group C: median=11, deviations: |9-11|=2, |11-11|=0, |13-11|=2  

    All deviations are 2,0,2 for each group.

</br>

4. Overall mean of deviations: (2+0+2 + 2+0+2 + 2+0+2)/9 = 12/9 = 1.333

</br>

5. ANOVA on deviations: F = (between SS / df_b) / (within SS / df_w)  
    Between: 3 groups, mean dev per group: 1.333, SS_b = 3*(1.333-1.333)^2 = 0  
    Within: SS_w = ∑ (dev - group mean)^2 = 0 (all equal)  
    F = 0 / 0 = undefined, but effectively 0

</br>

6. Critical Value  
    F<sub>critical</sub> (0.05, 2, 6) ≈ 5.14

</br>

7. Decision  
    Since F=0 < 5.14, fail to reject H<sub>0</sub>. Variances are homogeneous.