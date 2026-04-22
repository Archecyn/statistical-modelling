# Bayesian Proportion Test

Bayesian inference for proportions uses a beta distribution as a conjugate prior for binomial likelihoods. This allows updating beliefs about a probability (e.g., success rate) based on observed data.

</br>

## Example:
You have a coin and want to estimate the probability θ that it lands heads. You start with a prior belief: Beta(2, 2), meaning you expect θ around 0.5 but with some uncertainty. You flip the coin 10 times and get 7 heads.

</br>

1. Prior: Beta(α=2, β=2)  
   Mean = α/(α+β) = 2/4 = 0.5  
   Variance = (αβ)/((α+β)^2(α+β+1)) = (2*2)/(4^2*5) = 4/80 = 0.05

</br>

2. Likelihood: Binomial(n=10, θ) with 7 successes.  
   P(data|θ) ∝ θ^7 (1-θ)^3

</br>

3. Posterior: Beta(α + successes, β + failures) = Beta(2+7, 2+3) = Beta(9, 5)  
   Mean = 9/(9+5) = 9/14 ≈ 0.643  
   Variance = (9*5)/((14)^2 * 15) = 45/(196*15) ≈ 45/2940 ≈ 0.0153

</br>

4. Interpretation: The posterior mean is 0.643, with 95% credible interval approximately [0.4, 0.8] (using beta quantiles). This updates our belief from 0.5 to favor heads being more likely.