# Brown and Forsythe's Test

Robust test for homogeneity of variance when data are not normally distributed or when sample sizes are unequal.

</br>

## Example:
A researcher wants to compare three different fertilizers on plant growth. Before conducting ANOVA, they test the homogeneity of variance using Brown and Forsythe's test. Given the following data, determine if the variances are equal across groups. Use α = 0.05.

</br>

</br>

<table>
<thead>
    <tr>
        <th>Fertilizer A</th>
        <th>Fertilizer B</th>
        <th>Fertilizer C</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td>24</td>
        <td>28</td>
        <td>19</td>
    </tr>
    <tr>
        <td>28</td>
        <td>31</td>
        <td>22</td>
    </tr>
    <tr>
        <td>22</td>
        <td>25</td>
        <td>18</td>
    </tr>
    <tr>
        <td>30</td>
        <td>35</td>
        <td>24</td>
    </tr>
    <tr>
        <td>26</td>
        <td>29</td>
        <td>17</td>
    </tr>
</tbody>
</table>

</br>

</br>

1. Define H<sub>0</sub> and H<sub>A</sub>   

    H<sub>0</sub>: σ²<sub>A</sub> = σ²<sub>B</sub> = σ²<sub>C</sub> (All group variances are equal)  

    H<sub>A</sub>: Not all variances are equal

</br>

2. Alpha    
 α = 0.05

</br>

3. Formula
Brown-Forsythe test statistic:    
F = (N - k) / (k - 1) × Σ n<sub>i</sub>(z̄<sub>i</sub> - z̄)² / Σ (n<sub>i</sub> - 1)    

Where:    
z<sub>ij</sub> = |Y<sub>ij</sub> - median<sub>i</sub>|    
z̄<sub>i</sub> = mean of z for group i    
z̄ = weighted mean of z̄<sub>i</sub>

</br>

4. State Decision Rule
If F > F<sub>critical</sub> with df1 = k-1 and df2 = N-k, reject H<sub>0</sub>

</br>

5. Calculate Test Statistic

**Step 1: Calculate group medians**
Median<sub>A</sub> = 26    
Median<sub>B</sub> = 29    
Median<sub>C</sub> = 19

</br>

**Step 2: Calculate absolute deviations from median**

| A | Y - 26| B | Y - 29| C |Y - 19 |
|---|---|---|---|---|---|
| 24 | 2 | 28 | 1 | 19 | 0 |
| 28 | 2 | 31 | 2 | 22 | 3 |
| 22 | 4 | 25 | 4 | 18 | 1 |
| 30 | 4 | 35 | 6 | 24 | 5 |
| 26 | 0 | 29 | 0 | 17 | 2 |

</br>

**Step 3: Calculate means for each group**
z̄<sub>A</sub> = (2+2+4+4+0)/5 = 2.4    
z̄<sub>B</sub> = (1+2+4+6+0)/5 = 2.6    
z̄<sub>C</sub> = (0+3+1+5+2)/5 = 2.2

</br>

**Step 4: Calculate grand mean**
z̄ = (2.4 + 2.6 + 2.2) / 3 = 2.4

</br>

**Step 5: Calculate F statistic**
Since all groups have n = 5, we can simplify:

Σ n<sub>i</sub>(z̄<sub>i</sub> - z̄)² = 5[(2.4-2.4)² + (2.6-2.4)² + (2.2-2.4)²]    
= 5[0 + 0.04 + 0.04] = 5(0.08) = 0.40

</br>

Σ (n<sub>i</sub> - 1) = (5-1) + (5-1) + (5-1) = 4+4+4 = 12

</br>

F = (15-3)/(3-1) × 0.40 / 12    
F = 12/2 × 0.0333    
F = 6 × 0.0333 = 0.20

</br>

6. Results
F = 0.20 < F<sub>critical</sub> (df1 = 2, df2 = 12, α = 0.05) ≈ 3.89

Fail to reject H<sub>0</sub>

</br>

7. Conclusion   

    Brown and Forsythe's test indicates that the variances are homogeneous across the three fertilizer groups (F = 0.20, p > 0.05). The assumption of equal variances required for ANOVA is satisfied. This test is more robust to non-normal distributions than Hartley's Fmax test, making it appropriate when the normality assumption cannot be met.