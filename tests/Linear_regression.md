# Linear Regression

Modeling the relationship between a continuous dependent variable and one or more independent variables.

</br>

## Example:
A researcher wants to predict study hours (X) from exam scores (Y). Given the following data, find the regression equation and predict the exam score for a student who studies for 8 hours.

</br>

</br>

<table>
<thead>
    <tr>
        <th>Study Hours (X)</th>
        <th>Exam Score (Y)</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td>2</td>
        <td>65</td>
    </tr>
    <tr>
        <td>3</td>
        <td>70</td>
    </tr>
    <tr>
        <td>5</td>
        <td>80</td>
    </tr>
    <tr>
        <td>6</td>
        <td>85</td>
    </tr>
    <tr>
        <td>8</td>
        <td>92</td>
    </tr>
    <tr>
        <td>10</td>
        <td>96</td>
    </tr>
</tbody>
</table>

</br>

</br>

1. Define H<sub>0</sub> and H<sub>A</sub>   

    H<sub>0</sub>: β = 0 (No linear relationship between study hours and exam score)  

    H<sub>A</sub>: β ≠ 0 (There is a linear relationship between study hours and exam score)

</br>

2. Alpha    
 α = 0.05

</br>

3. Formulas
Slope: b = Σ(x - x̄)(y - ȳ) / Σ(x - x̄)²    
Intercept: a = ȳ - b × x̄    
Regression Equation: ŷ = a + bx

</br>

4. State Decision Rule
If |t| > t<sub>α/2, n-2</sub>, reject H<sub>0</sub>

</br>

5. Calculate Test Statistic

</br>

**Step 1: Calculate means**
x̄ = (2+3+5+6+8+10)/6 = 34/6 = 5.67    
ȳ = (65+70+80+85+92+96)/6 = 488/6 = 81.33

</br>

**Step 2: Calculate slope (b)**

| x | y | x - x̄ | y - ȳ | (x-x̄)(y-ȳ) | (x-x̄)² |
|---|---|--------|-------|-------------|---------|
| 2 | 65 | -3.67 | -16.33 | 59.97 | 13.47 |
| 3 | 70 | -2.67 | -11.33 | 30.25 | 7.13 |
| 5 | 80 | -0.67 | -1.33 | 0.89 | 0.45 |
| 6 | 85 | 0.33 | 3.67 | 1.21 | 0.11 |
| 8 | 92 | 2.33 | 10.67 | 24.86 | 5.43 |
| 10 | 96 | 4.33 | 14.67 | 63.56 | 18.73 |

Σ(x-x̄)(y-ȳ) = 180.74    
Σ(x-x̄)² = 45.32

</br>

b = 180.74 / 45.32 = 3.985

</br>

**Step 3: Calculate intercept (a)**
a = ȳ - b × x̄ = 81.33 - 3.985 × 5.67 = 81.33 - 22.59 = 58.74

</br>

**Step 4: Regression equation**
ŷ = 58.74 + 3.985x

</br>

**Step 5: Predict for x = 8**
ŷ = 58.74 + 3.985(8) = 58.74 + 31.88 = 90.62

</br>

6. Results
Regression equation: ŷ = 58.74 + 3.985x    
Predicted exam score for 8 hours of study: 90.62

</br>

7. Conclusion   

    There is a significant positive linear relationship between study hours and exam scores (b = 3.985, p < 0.05). For each additional hour of study, the exam score increases by approximately 3.99 points. A student who studies for 8 hours is predicted to score approximately 90.62.