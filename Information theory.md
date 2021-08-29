# Information theory
## Key ideas
Maths stuff happened

## 'Surprisal'/Shannon information

$$\log_2 \frac{1}{P(x)}$$
 quantifying surprise
additive
no total information, surprise doesn't have to sum to 1

## Optimal information encoding
$$log_2 \frac{1}{P(x)}$$
we can't compress smaller than our measure of surprise

## Entropy
$$H(p) = \sum_{x}^{1} p(x) \times log_2 \frac{1}{P(x)}$$

or the sum for all x of:
p(x) \* surprisingness of x

e.g. a fair coin's entropy:
$$(\frac{1}{2} \times log_2 \frac{1}{2}) + (\frac{1}{2} \times log_2 \frac{1}{2}) = 1$$

H<sub>max</sub> = maximal uncertainty (1/2, 1/2
H<sub>max</sub> is a lower bound for compression, which makes sense

## Cross-entropy
Using a code created for a different kind of message
e.g. code optimised for talking a lot about dogs, used for a message talking a lot about cats

$$H(p,q) = \sum_{x}^{1} p(x) \times \frac{1}{log_2(q(x))}$$

Non-symmetrical (duh)

## KL divergence
$$D_{KL}(p||q) = H(p,q) - H(p)$$
How much worse off you are using suboptimal encoding
Δaverage surprise
