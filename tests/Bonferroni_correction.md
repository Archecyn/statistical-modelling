# Bonferroni's Correction

Multiple comparison correction that adjusts the significance level when conducting multiple statistical tests.

</br>

## Example:
A researcher wants to compare three different diets (A, B, C) on weight loss. They conduct three pairwise t-tests without correction, then apply Bonferroni's correction. Given the following uncorrected p-values, determine which comparisons remain significant.

</br>

</br>

<table>
<thead>
    <tr>
        <th>Comparison</th>
        <th>t-statistic</th>
        <th>p-value (uncorrected)</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td>Diet A vs Diet B</td>
        <td>2.45</td>
        <td>0.032</td>
    </tr>
    <tr>
        <td>Diet A vs Diet C</td>
        <td>3.12</td>
        <td>0.008</td>
    </tr>
    <tr>
        <td>Diet B vs Diet C</td>
        <td>2.89</td>
        <td>0.015</td>
    </tr>
</tbody>
</table>

</br>

</br>

Number of comparisons (m) = 3

</br>

</br>

1. Define H<sub>0</sub> and H<sub>A</sub>   

    H<sub>0</sub>: μ<sub>i</sub> = μ<sub>j</sub> (No difference between diet groups)  

    H<sub>A</sub>: μ<sub>i</sub> ≠ μ<sub>j</sub> (At least one pair of diets differs)

</br>

2. Alpha    
 α = 0.05 (original)
α<sub>adjusted</sub> = α / m = 0.05 / 3 = 0.0167

</br>

3. Formula
Bonferroni-adjusted alpha:    
α<sub>adjusted</sub> = α / m    

Bonferroni-adjusted p-value:    
p<sub>adjusted</sub> = p × m (capped at 1.0)

</br>

4. State Decision Rule
If p<sub>adjusted</sub> < α (original), reject H<sub>0</sub>    
Or equivalently: If p < α<sub>adjusted</sub>, reject H<sub>0</sub>

</br>

5. Calculate Test Statistic

**Step 1: Calculate adjusted alpha**
α<sub>adjusted</sub> = 0.05 / 3 = 0.0167

</br>

**Step 2: Calculate adjusted p-values**

| Comparison | p (uncorrected) | p × 3 | Adjusted p | Significant? |
|------------|-----------------|-------|------------|---------------|
| A vs B | 0.032 | 0.096 | 0.096 | No |
| A vs C | 0.008 | 0.024 | 0.024 | No |
| B vs C | 0.015 | 0.045 | 0.045 | No |

</br>

**Step 3: Compare with adjusted alpha**

- Diet A vs Diet B: p = 0.032 > 0.0167 → Not significant
- Diet A vs Diet C: p = 0.008 > 0.0167 → Not significant  
- Diet B vs Diet C: p = 0.015 > 0.0167 → Not significant

</br>

6. Results
After Bonferroni correction, none of the pairwise comparisons remain significant at α = 0.05.

</br>

7. Conclusion   

    Although the uncorrected p-values suggested all three comparisons were significant at the 0.05 level, after applying Bonferroni's correction for multiple comparisons, none reach statistical significance. The more stringent threshold (α = 0.0167) accounts for the increased Type I error risk from conducting multiple tests. The researcher should either report these as non-significant or consider increasing sample size to detect smaller effects.