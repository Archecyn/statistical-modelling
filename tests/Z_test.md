# Z-test

A Z-test is used for hypothesis testing when the population variance is known and the sample size is large (n ≥ 30). It compares a sample mean to a known population mean or compares two sample means.

</br>

## Example:
A factory claims the average weight of their product is 100g with a known standard deviation of 5g. A sample of 50 products has an average weight of 102g. Test if the sample mean differs from 100g at α = 0.05.

</br>

1. Define H<sub>0</sub> and H<sub>A</sub>   

    H<sub>0</sub>: μ = 100 (sample mean equals population mean)  

    H<sub>A</sub>: μ ≠ 100 (sample mean differs from population mean)

</br>

2. Alpha    
 α = 0.05 (two-tailed)

</br>

3. Test Statistic  
    Z = (x̄ - μ) / (σ / √n) = (102 - 100) / (5 / √50) = 2 / (5 / 7.071) = 2 / 0.707 = 2.828

</br>

4. Critical Value  
    For α = 0.05 two-tailed, Z<sub>critical</sub> = ±1.96

</br>

5. Decision  
    Since |2.828| > 1.96, reject H<sub>0</sub>. The sample mean significantly differs from 100g.