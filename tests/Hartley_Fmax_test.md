# Hartley's Fmax Test

Homogeneity of variance test used before ANOVA to check if groups have equal variances.

</br>

## Example:
A researcher wants to conduct a one-way ANOVA to compare four treatment groups. Before proceeding, they test the homogeneity of variance using Hartley's Fmax test. Given the following sample variances, test if the variances are equal across groups. Use α = 0.05.

</br>

</br>

<table>
<thead>
    <tr>
        <th>Group</th>
        <th>n</th>
        <th>Variance (s²)</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td>1</td>
        <td>10</td>
        <td>12.5</td>
    </tr>
    <tr>
        <td>2</td>
        <td>10</td>
        <td>8.3</td>
    </tr>
    <tr>
        <td>3</td>
        <td>10</td>
        <td>15.7</td>
    </tr>
    <tr>
        <td>4</td>
        <td>10</td>
        <td>9.8</td>
    </tr>
</tbody>
</table>

</br>

</br>

k (number of groups) = 4    
n (sample size per group) = 10

</br>

</br>

1. Define H<sub>0</sub> and H<sub>A</sub>   

    H<sub>0</sub>: σ²<sub>1</sub> = σ²<sub>2</sub> = σ²<sub>3</sub> = σ²<sub>4</sub> (All group variances are equal)  

    H<sub>A</sub>: Not all variances are equal (At least one variance differs)

</br>

2. Alpha    
 α = 0.05

</br>

3. Formula
F<sub>max</sub> = s²<sub>max</sub> / s²<sub>min</sub>    

Where:    
s²<sub>max</sub> = largest sample variance    
s²<sub>min</sub> = smallest sample variance

</br>

4. State Decision Rule
Compare calculated F<sub>max</sub> to critical value from Hartley's Fmax table with:
- df = n - 1 (degrees of freedom)
- k = number of groups

If F<sub>max</sub> > F<sub>critical</sub>, reject H<sub>0</sub>

</br>

5. Calculate Test Statistic

**Step 1: Identify max and min variances**
s²<sub>max</sub> = 15.7 (Group 3)    
s²<sub>min</sub> = 8.3 (Group 2)

</br>

**Step 2: Calculate Fmax**
F<sub>max</sub> = s²<sub>max</sub> / s²<sub>min</sub> = 15.7 / 8.3 = 1.891

</br>

**Step 3: Find critical value**
For k = 4 groups, n = 10 (df = 9), α = 0.05:    
F<sub>critical</sub> ≈ 3.18

</br>

**Step 4: Compare**
F<sub>max</sub> = 1.891 < F<sub>critical</sub> = 3.18

</br>

6. Results
Fail to reject H<sub>0</sub>

</br>

7. Conclusion   

    Hartley's Fmax test indicates that the variances are homogeneous across the four treatment groups (F<sub>max</sub> = 1.89, p > 0.05). The assumption of equal variances required for ANOVA is satisfied. The researcher can proceed with the one-way ANOVA without concern for heterogeneity of variance.