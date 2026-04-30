# Tukey Test

Post-hoc pairwise comparison test following ANOVA to determine which specific group means differ.

</br>

## Example:
A one-way ANOVA showed significant differences in test scores across four teaching methods (A, B, C, D). Given the following summary data, perform Tukey's test to identify which pairs differ significantly. Use α = 0.05.

</br>

</br>

<table>
<thead>
    <tr>
        <th>Method A</th>
        <th>Method B</th>
        <th>Method C</th>
        <th>Method D</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td>78</td>
        <td>82</td>
        <td>65</td>
        <td>88</td>
    </tr>
    <tr>
        <td>82</td>
        <td>85</td>
        <td>70</td>
        <td>92</td>
    </tr>
    <tr>
        <td>75</td>
        <td>79</td>
        <td>68</td>
        <td>85</td>
    </tr>
    <tr>
        <td>80</td>
        <td>84</td>
        <td>72</td>
        <td>90</td>
    </tr>
</tbody>
</table>

</br>

</br>

ANOVA Results:
- Between-groups MS = 892.5
- Within-groups MS = 12.8
- k (number of groups) = 4
- N (total observations) = 16
- df<sub>within</sub> = 12

</br>

</br>

1. Define H<sub>0</sub> and H<sub>A</sub>   

    H<sub>0</sub>: μ<sub>i</sub> = μ<sub>j</sub> for all pairwise comparisons (no difference between group means)  

    H<sub>A</sub>: μ<sub>i</sub> ≠ μ<sub>j</sub> for at least one pair (some groups differ)

</br>

2. Alpha    
 α = 0.05

</br>

3. Formulas
Tukey Q critical value from studentized range table    
q<sub>α, k, df<sub>within</sub></sub> = q<sub>0.05, 4, 12</sub> ≈ 4.20    

Standard Error: SE = √(MS<sub>within</sub> / n) = √(12.8 / 4) = √3.2 = 1.79    

Minimum Significant Difference (MSD) = q × SE

</br>

4. State Decision Rule
If |x̄<sub>i</sub> - x̄<sub>j</sub>| > MSD, reject H<sub>0</sub> for that pair

</br>

5. Calculate Test Statistic

**Step 1: Calculate group means**
x̄<sub>A</sub> = (78+82+75+80)/4 = 315/4 = 78.75    
x̄<sub>B</sub> = (82+85+79+84)/4 = 330/4 = 82.50    
x̄<sub>C</sub> = (65+70+68+72)/4 = 275/4 = 68.75    
x̄<sub>D</sub> = (88+92+85+90)/4 = 355/4 = 88.75

</br>

**Step 2: Calculate MSD**
MSD = q × SE = 4.20 × 1.79 = 7.52

</br>

**Step 3: Pairwise comparisons**

| Comparison | Difference | x̄<sub>i</sub> - x̄<sub>j</sub> | Significant? |
|-------------|------------|----------------------|----------------|
| A vs B | 78.75 - 82.50 | 3.75 | No |
| A vs C | 78.75 - 68.75 | 10.00 | Yes |
| A vs D | 78.75 - 88.75 | 10.00 | Yes |
| B vs C | 82.50 - 68.75 | 13.75 | Yes |
| B vs D | 82.50 - 88.75 | 6.25 | No |
| C vs D | 68.75 - 88.75 | 20.00 | Yes |

</br>

6. Results
Significant pairs (p < 0.05):
- A vs C: difference = 10.00 (p < 0.05)
- A vs D: difference = 10.00 (p < 0.05)
- B vs C: difference = 13.75 (p < 0.05)
- C vs D: difference = 20.00 (p < 0.05)

Non-significant pairs:
- A vs B: difference = 3.75
- B vs D: difference = 6.25

</br>

7. Conclusion   

    Tukey's HSD test revealed significant differences between Method C and all other methods (A, B, and D). Method C produced significantly lower test scores (M = 68.75) compared to Methods A (78.75), B (82.50), and D (88.75). No significant difference was found between Methods A and B, or between Methods B and D.