# Bartlett's Test

Test for homogeneity of variance that is sensitive to departures from normality. More powerful than Levene's test when data are normally distributed.

</br>

## Example:
A researcher conducts an experiment with four treatment groups and wants to test if the variances are equal before performing ANOVA. Given the following summary statistics, perform Bartlett's test. Use α = 0.05.

</br>

</br>

<table>
<thead>
    <tr>
        <th>Group</th>
        <th>n</th>
        <th>Mean</th>
        <th>Variance (s²)</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td>1</td>
        <td>8</td>
        <td>45.2</td>
        <td>12.4</td>
    </tr>
    <tr>
        <td>2</td>
        <td>8</td>
        <td>52.8</td>
        <td>18.7</td>
    </tr>
    <tr>
        <td>3</td>
        <td>8</td>
        <td>48.5</td>
        <td>9.3</td>
    </tr>
    <tr>
        <td>4</td>
        <td>8</td>
        <td>55.1</td>
        <td>22.1</td>
    </tr>
</tbody>
</table>

</br>

</br>

k (number of groups) = 4    
N (total observations) = 32

</br>

</br>

1. Define H<sub>0</sub> and H<sub>A</sub>   

    H<sub>0</sub>: σ²<sub>1</sub> = σ²<sub>2</sub> = σ²<sub>3</sub> = σ²<sub>4</sub> (All group variances are equal)  

    H<sub>A</sub>: Not all variances are equal

</br>

2. Alpha    
 α = 0.05

</br>

3. Formula
Bartlett's χ² statistic:    

χ² = (N - k) × ln(s²<sub>p</sub>) - Σ (n<sub>i</sub> - 1) × ln(s²<sub>i</sub>)    

Where:    
s²<sub>p</sub> = pooled variance = Σ (n<sub>i</sub> - 1)s²<sub>i</sub> / (N - k)    

Correction factor: C = 1 + (1/(3(k-1))) × (Σ 1/(n<sub>i</sub>-1) - 1/(N-k))    

Adjusted χ² = χ² / C

</br>

4. State Decision Rule
If χ² > χ²<sub>critical</sub> with df = k - 1, reject H<sub>0</sub>

</br>

5. Calculate Test Statistic

**Step 1: Calculate pooled variance**
s²<sub>p</sub> = [(8-1)(12.4) + (8-1)(18.7) + (8-1)(9.3) + (8-1)(22.1)] / (32-4)    
s²<sub>p</sub> = [7(12.4) + 7(18.7) + 7(9.3) + 7(22.1)] / 28    
s²<sub>p</sub> = (86.8 + 130.9 + 65.1 + 154.7) / 28    
s²<sub>p</sub> = 437.5 / 28 = 15.625

</br>

**Step 2: Calculate chi-square**
Σ (n<sub>i</sub> - 1) × ln(s²<sub>i</sub>) = 7[ln(12.4) + ln(18.7) + ln(9.3) + ln(22.1)]    
= 7[2.518 + 2.928 + 2.228 + 3.095]    
= 7(10.769) = 75.383

</br>

(N - k) × ln(s²<sub>p</sub>) = 28 × ln(15.625) = 28 × 2.748 = 76.944

</br>

χ² = 76.944 - 75.383 = 1.561

</br>

**Step 3: Calculate correction factor**
Σ 1/(n<sub>i</sub> - 1) = 4 × (1/7) = 4/7 = 0.5714    
1/(N - k) = 1/28 = 0.0357

</br>

C = 1 + (1/(3(3))) × (0.5714 - 0.0357)    
C = 1 + (1/9) × 0.5357    
C = 1 + 0.0595 = 1.0595

</br>

**Step 4: Calculate adjusted chi-square**
χ²<sub>adjusted</sub> = 1.561 / 1.0595 = 1.473

</br>

6. Results
χ²<sub>adjusted</sub> = 1.473 < χ²<sub>critical</sub> (df = 3, α = 0.05) = 7.815

Fail to reject H<sub>0</sub>

</br>

7. Conclusion   

    Bartlett's test indicates that the variances are homogeneous across the four treatment groups (χ² = 1.47, p > 0.05). The assumption of equal variances required for ANOVA is satisfied. Note: Bartlett's test is sensitive to non-normality, so if the data are not normally distributed, consider using Levene's test or Brown-Forsythe test instead.