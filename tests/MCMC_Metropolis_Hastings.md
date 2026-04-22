# MCMC: Metropolis-Hastings

Metropolis-Hastings is an MCMC algorithm for sampling from a target distribution π(θ) when direct sampling is difficult. It uses a proposal distribution q(θ'|θ) to suggest new values and accepts/rejects based on the ratio of target densities.

</br>

## Example:
Sample from a Beta(2, 5) distribution (target π(θ) ∝ θ^1 (1-θ)^4 for θ ∈ [0,1]). Use a normal proposal N(θ, 0.1^2) truncated to [0,1]. Start at θ=0.5, run 5 steps.

</br>

1. Target density: π(θ) = [θ^{1} (1-θ)^{4}] / B(2,5) where B(2,5) ≈ 0.0333 (normalising constant).  
   For simplicity, work with unnormalised: f(θ) = θ (1-θ)^4

</br>

2. Proposal: q(θ'|θ) = Normal(θ, 0.01) truncated to [0,1].

</br>

3. Acceptance ratio: r = min{1, [f(θ') / f(θ)] * [q(θ|θ') / q(θ'|θ)]}  
   Since proposal is symmetric, q(θ|θ') = q(θ'|θ), so r = min{1, f(θ') / f(θ)}

</br>

4. Steps:  
   - Step 0: θ = 0.5, f(0.5) = 0.5 * (0.5)^4 = 0.5 * 0.0625 = 0.03125  
   - Step 1: Propose θ' = 0.5 + 0.1*Z where Z~N(0,1), say Z=0.5 → θ'=0.55, f(0.55)=0.55*(0.45)^4 ≈ 0.55*0.0410 ≈ 0.02255  
     r = min(1, 0.02255/0.03125) ≈ 0.722 → Accept (u=0.3 < 0.722), θ=0.55  
   - Step 2: Propose θ'=0.55 + 0.1*(-0.2)=0.53, f(0.53)≈0.53*(0.47)^4 ≈ 0.53*0.049 ≈ 0.026  
     r = 0.026/0.02255 ≈ 1.15 → min(1,1.15)=1 → Accept, θ=0.53  
   - Step 3: Propose θ'=0.53 + 0.1*1.5=0.68, f(0.68)≈0.68*(0.32)^4 ≈ 0.68*0.0105 ≈ 0.00714  
     r = 0.00714/0.026 ≈ 0.274 → Accept (u=0.1 < 0.274), θ=0.68  
   - Step 4: Propose θ'=0.68 + 0.1*(-1.0)=0.58, f(0.58)≈0.58*(0.42)^4 ≈ 0.58*0.031 ≈ 0.018  
     r = 0.018/0.00714 ≈ 2.52 → min(1,2.52)=1 → Accept, θ=0.58  
   - Step 5: Propose θ'=0.58 + 0.1*0.8=0.66, f(0.66)≈0.66*(0.34)^4 ≈ 0.66*0.0133 ≈ 0.00878  
     r = 0.00878/0.018 ≈ 0.488 → Accept (u=0.4 < 0.488), θ=0.66  

   Samples: 0.5, 0.55, 0.53, 0.68, 0.58, 0.66 (discard burn-in if needed). Mean ≈ 0.58, close to Beta(2,5) mean = 2/7 ≈ 0.286 (but with few samples).