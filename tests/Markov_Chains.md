# Markov Chains

A Markov chain is a mathematical system that undergoes transitions from one state to another according to certain probabilistic rules. The defining characteristic is that the next state depends only on the current state, not on the sequence of events that preceded it (memoryless property).

</br>

## Example:
Consider a simple weather model with two states: Sunny (S) and Rainy (R). The transition probabilities are as follows:

- If today is Sunny, there's a 90% chance tomorrow will be Sunny and 10% chance it will be Rainy.
- If today is Rainy, there's a 50% chance tomorrow will be Sunny and 50% chance it will be Rainy.

We can represent this with a transition matrix:

<table>
<thead>
    <tr>
        <th>From/To</th>
        <th>Sunny</th>
        <th>Rainy</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td>Sunny</td>
        <td>0.9</td>
        <td>0.1</td>
    </tr>
    <tr>
        <td>Rainy</td>
        <td>0.5</td>
        <td>0.5</td>
    </tr>
</tbody>
</table>

</br>

1. Initial state: Suppose today is Sunny (probability 1 for S, 0 for R).  
   State vector: [1, 0]

</br>

2. After 1 day: Multiply by transition matrix.  
   New state: [1*0.9 + 0*0.5, 1*0.1 + 0*0.5] = [0.9, 0.1]

</br>

3. After 2 days: [0.9*0.9 + 0.1*0.5, 0.9*0.1 + 0.1*0.5] = [0.81 + 0.05, 0.09 + 0.05] = [0.86, 0.14]

</br>

4. Stationary distribution: After many steps, the probabilities converge.  
   Solve for π where π = π * P (P is the transition matrix).  
   π_S = 0.9π_S + 0.5π_R  
   π_R = 0.1π_S + 0.5π_R  
   And π_S + π_R = 1  

   Solving: π_S = 0.9π_S + 0.5(1 - π_S) → π_S = 0.9π_S + 0.5 - 0.5π_S → 0.1π_S = 0.5 → π_S = 5/6 ≈ 0.833  
   π_R = 1/6 ≈ 0.167  

   So, long-term: 83.3% Sunny, 16.7% Rainy.