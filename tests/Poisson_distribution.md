# Poisson Distribution Word Problems

Count data occurring randomly over a fixed interval of time or space.

</br>

## Example:
A customer service center receives an average of 3 calls per hour. Assuming calls follow a Poisson distribution, what is the probability of receiving exactly 5 calls in an hour? Use λ = 3.

</br>

</br>

| Parameter | Value |
|-----------|-------|
| λ (average rate) | 3 calls/hour |
| x (desired count) | 5 calls |
| Probability | ? |

</br>

</br>

1. Define H<sub>0</sub> and H<sub>A</sub>   

    H<sub>0</sub>: The number of calls follows a Poisson distribution with λ = 3  

    H<sub>A</sub>: The number of calls does not follow a Poisson distribution with λ = 3

</br>

2. Alpha    
 α = 0.05 (for goodness-of-fit testing)

</br>

3. Formula
The Poisson probability mass function:

    P(X = x) = (e<sup>-λ</sup> × λ<sup>x</sup>) / x!

</br>

4. State Decision Rule
For probability calculations:    
    P(X = 5) = (e<sup>-3</sup> × 3<sup>5</sup>) / 5!    

For hypothesis testing: If observed frequencies significantly differ from expected, reject H<sub>0</sub>

</br>

5. Calculate Test Statistic

P(X = 5) = (e<sup>-3</sup> × 3<sup>5</sup>) / 5!

</br>

Step 1: Calculate e<sup>-3</sup>    
e<sup>-3</sup> ≈ 0.049787

</br>

Step 2: Calculate 3<sup>5</sup>    
3<sup>5</sup> = 243

</br>

Step 3: Calculate 5!    
5! = 5 × 4 × 3 × 2 × 1 = 120

</br>

Step 4: Combine    
P(X = 5) = (0.049787 × 243) / 120    
P(X = 5) = 12.098 / 120    
P(X = 5) = 0.1008

</br>

6. Results
P(X = 5) ≈ 0.1008 or about 10.08%

</br>

7. Conclusion   

    The probability of receiving exactly 5 calls in an hour when the average is 3 calls/hour is approximately 0.1008 (10.08%). This means about 1 out of 10 hours would expect to see exactly 5 calls.

</br>

</br>

## Additional Example: Cumulative Probability

What is the probability of receiving 3 or fewer calls in an hour?

</br>

P(X ≤ 3) = P(X = 0) + P(X = 1) + P(X = 2) + P(X = 3)

</br>

P(X = 0) = e<sup>-3</sup> × 3<sup>0</sup> / 0! = 0.0498 × 1 / 1 = 0.0498    
P(X = 1) = e<sup>-3</sup> × 3<sup>1</sup> / 1! = 0.0498 × 3 / 1 = 0.1494    
P(X = 2) = e<sup>-3</sup> × 3<sup>2</sup> / 2! = 0.0498 × 9 / 2 = 0.2241    
P(X = 3) = e<sup>-3</sup> × 3<sup>3</sup> / 3! = 0.0498 × 27 / 6 = 0.2241    

</br>

P(X ≤ 3) = 0.0498 + 0.1494 + 0.2241 + 0.2241 = 0.6474

</br>

The probability of 3 or fewer calls is approximately 64.74%.