# Dunn's Test

Non-parametric post-hoc test for multiple comparisons following Kruskal-Wallis test.

</br>

## Example:
A researcher conducted a Kruskal-Wallis test and found significant differences (H = 12.45, p = 0.014) among four diet groups. Now perform Dunn's test to identify which specific pairs differ. Use α = 0.05.

</br>

</br>

<table>
<thead>
    <tr>
        <th>Group</th>
        <th>n</th>
        <th>Rank Sum</th>
        <th>Mean Rank</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td>Diet A</td>
        <td>8</td>
        <td>145</td>
        <td>18.125</td>
    </tr>
    <tr>
        <td>Diet B</td>
        <td>8</td>
        <td>98</td>
        <td>12.25</td>
    </tr>
    <tr>
        <td>Diet C</td>
        <td>8</td>
        <td>172</td>
        <td>21.50</td>
    </tr>
    <tr>
        <td>Diet D</td>
        <td>8</td>
        <td>109</td>
        <td>13.625</td>
    </tr>
</tbody>
</table>

</br>

</br>

Total N = 32    
k = 4 groups    
Kruskal-Wallis H = 12.45, p = 0.014

</br>

</br>

1. Define H<sub>0</sub> and H<sub>A</sub>   

    H<sub>0</sub>: The distributions of the two groups are equal (no difference)  

    H<sub>A</sub>: The distributions of the two groups are not equal (difference exists)

</br>

2. Alpha    
 α = 0.05

</br>

3. Formulas
Dunn's test uses z-values from standard normal distribution with Bonferroni correction:    
z<sub>α/k(k-1)</sub> = z<sub>0.05/6</sub> = z<sub>0.0083</sub> ≈ 2.39    

Critical difference: CD = z × √[N(N+1)/12 × (1/n<sub>i</sub> + 1/n<sub>j</sub>)]

</br>

4. State Decision Rule
If |R<sub>i</sub>/n<sub>i</sub> - R<sub>j</sub>/n<sub>j</sub>| > CD, reject H<sub>0</sub> for that pair

</br>

5. Calculate Test Statistic

**Step 1: Calculate critical difference for each pair**
For equal sample sizes (n = 8):    
CD = 2.39 × √[32(33)/12 × (1/8 + 1/8)]    
CD = 2.39 × √[1056/12 × (2/8)]    
CD = 2.39 × √[88 × 0.25]    
CD = 2.39 × √22    
CD = 2.39 × 4.69 = 11.21

</br>

**Step 2: Calculate pairwise differences in mean ranks**

| Comparison | Mean Rank 1 | Mean Rank 2 | Difference | Difference | > CD? |
|------------|-------------|-------------|------------|-------------------|-----------|
| A vs B | 18.125 | 12.25 | 5.875 | No |
| A vs C | 18.125 | 21.50 | -3.375 | No |
| A vs D | 18.125 | 13.625 | 4.50 | No |
| B vs C | 12.25 | 21.50 | -9.25 | No |
| B vs D | 12.25 | 13.625 | -1.375 | No |
| C vs D | 21.50 | 13.625 | 7.875 | No |

</br>

**Step 3: Using rank sums directly**
Since all n = 8, we can also compare rank sums directly:

| Comparison | Rank Sum i | Rank Sum j | Difference | Significant? |
|------------|------------|------------|------------|---------------|
| A vs B | 145 | 98 | 47 | No |
| A vs C | 145 | 172 | -27 | No |
| A vs D | 145 | 109 | 36 | No |
| B vs C | 98 | 172 | -74 | Yes |
| B vs D | 98 | 109 | -11 | No |
| C vs D | 172 | 109 | 63 | Yes |

</br>

Using the formula: CD<sub>ranks</sub> = 2.39 × √[32(33)/12 × (1/8 + 1/8)] = 89.68

</br>

- B vs C: |98 - 172| = 74 < 89.68 → Not significant
- C vs D: |172 - 109| = 63 < 89.68 → Not significant

</br>

6. Results
After Dunn's post-hoc test with Bonferroni correction, none of the pairwise comparisons reach statistical significance at α = 0.05.

</br>

7. Conclusion   

    Although the Kruskal-Wallis test indicated significant overall differences among the four diet groups (H = 12.45, p = 0.014), Dunn's post-hoc test with Bonferroni correction does not reveal any specific pairs that differ significantly. This suggests that while there is evidence of some difference across the groups, the differences are not large enough to identify which specific pairs differ after accounting for multiple comparisons. Consider increasing sample size or reporting the preliminary Kruskal-Wallis result with appropriate caveats.