---
layout: default
title: Probability and Statistics
---

- [Combinatorics](#combinatorics)
  - [Permutations](#permutations)
  - [Combinations](#combinations)
  - [Additional notes on Combinatorics](#additional-notes-on-combinatorics)
- [Conditional Probabilities](#conditional-probabilities)
  - [Baye's Rule](#bayes-rule)
- [Expectated Value, Variance, and Covariance](#expectated-value-variance-and-covariance)
- [Common Distributions](#common-distributions)
  - [Continuous](#continuous)
    - [Gaussian](#gaussian)
    - [Uniform](#uniform)
    - [Exponential](#exponential)
  - [Discrete](#discrete)
    - [Bernoulli](#bernoulli)
    - [Binomial](#binomial)
    - [Poisson](#poisson)
    - [Geometric](#geometric)


# Combinatorics

Combinatorics is some flavor of choosing $k$ members from a set of $n$ and finding out how many possible subsets $z$ there are. These are incredibly practical to backpocket in the day to day. 

Basic combinatorics can be split into 2 categories and each with 2 subcategories, making **4 cases in total**. 
- Permutations:  order of selection MATTERS
- Combinations: order of selection DOES NOT MATTER

## Permutations

With replacement: $z = n^k$ 

Without replacement: $z = \frac{n!}{(n-k)!} = n(n-1)(n-2)...(n-k+1)$

*these are the more intuitive of the bunch, convince yourself*

## Combinations

Without replacement: $z = \binom{n}{k} \triangleq \frac{n!}{k!(n-k)!}$

*notice this is just permutation w/o replacement normalized by k! which represents the number of ways to order k elements*

With replacement: $z = \binom{n+k-1}{k} \triangleq \frac{(n+k-1)!}{(k)!(n-1)!}$

*the intuition here is significantly more difficult to grasp without mentally restructuring the problem.  hint: instead of thinking of ways to select k elements, think of ways to partition a set of m elements with k boundaries.*

## Additional notes on Combinatorics

1. The formulas for combinatorics is not difficult, most people could memorize these in 5 minutes.  What is more critical is recognizing which IRL scenarios boil down to what type of combinatorics problem.  
     - **Example of Perm w/o replacement**: all possible 1st, 2nd, and 3rd place podiums among n competitors
     - **Example of Perm w replacement**: creating a 4 digit PIN for you phone
     - **Example of Comb w/o replacement**: All possible 5-card poker hands. 
     - **Example of Comb w replacement**: All possible boxes of a dozen donuts you can buy from a store (assuming none run out). 

2. As an exercise in solidfying intuition, it is also useful to see how these combinatorics scenarios evolve as $n\rightarrow \infty, \bar{k}$ or when $k\rightarrow \infty, \bar{n}$

<figure align="center">
  <img src="/assets/images/combinatorics_k_fixed.png" width="600">
  <figcaption>varying n from (0, 50) with k = 5</figcaption>
</figure>

   - relative order is invariant in $n$ where $n\neq 0$.  ($P_r(n,k) > P(n,k) > C_r(n,k) > C(n,k)$).  
   - blue and orange curves start at $n=k$ because $n<k$ is absurd when not selecting with replacement.
   - as $n\rightarrow \infty$, replacement and no replacement makes less and less of a difference.  ($P \rightarrow P_r$ and $C \rightarrow C_r$)
  
<figure align="center">
  <img src="/assets/images/combinatorics_n_fixed.png" width="600">
  <figcaption>varying k from (0, 20) with n = 10</figcaption>
</figure>

   - relative order is invariant in $k$ where $k > 1$.  ($P_r(n,k) > P(n,k) > C_r(n,k) > C(n,k)$).  
   - blue and orange curves end at $n=k$ for same absurd reason that $n<k$.
   - $C(n,k) is the ONLY combinatoric that is NOT monotonically increasing. 

# Conditional Probabilities

## Baye's Rule

# Expectated Value, Variance, and Covariance

# Common Distributions

## Continuous

### Gaussian

### Uniform

### Exponential

## Discrete

### Bernoulli

### Binomial

### Poisson

### Geometric