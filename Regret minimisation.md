# Regret minimisation
See Thomas' slides https://espr2021.slack.com/files/U025RNK40FR/F02C5RYHQAF/multiplicative_weights__espr_2021__1_.pdf

## Key ideas
- We can minimise regret without knowing the future
- You don't need the perfect strategy - just one as good as the best strategy in hindsight
- Hedging is powerful

## The mathematics of regret

Regret = (what you would have done if you'd had your current information) - (what you actually did)

**Formally**
If there are T choices, N strategies or options to choose between:
$$Regret = \sum_{}^{T} (loss\ at\ time\ i) - min\sum_{}^{T} (loss\ of\ strategy\ j\ at\ time\ i) $$
Sum of your losses - sum of the best strategy's losses

**Upper bound for regret**
$$ Regret \leq \ log_2(n) $$
$$N = 2^k $$
$$Regret \leq k $$
Therefore regret is independent of future assumptions.

## Working with imperfect strategies
1) Pick the option with the majority vote
2) If a strategy makes a mistake, eliminate it
3) If no strategy is alive, resurrect all strategies

## Hedging
![[Pasted image 20210829151958.png]]

## Applications
**Differential privacy**
When you want to mess with data without personally identifying anyone.
Give a fake dataset that minimises regret against all possible datasets, whilst preserving privacy.

