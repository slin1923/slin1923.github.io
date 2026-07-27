---
layout: default
title: Algebra
---

- [Disclaimer](#disclaimer)
- [Polynomials](#polynomials)
  - [Root finding](#root-finding)


# Disclaimer
For the algebra section only, I assume everyone reading this guide is algebraically sound.  This section thus contains only little tips and hacks I have found useful. 

# Polynomials

## Root finding

- Finding the root of a 1st-order polynomial is trivial
- Finding the root of a 2nd-order polynomial uses the quadratic equation. 

$$ \text{for a polynomial of form:  } ax^2 + bx + c = 0$$
$$ \text{use:  } x = \frac{-b \pm \sqrt{b^2-4ac}}{2a}$$

*derived from completing the square. to get the ball rolling, divide both sides by $a$, move $c/a$, add $b^2/4a^2$ to both sides...*

- Finding the root of a 3rd and 4th order polynomial require advanced functions that are not practically seen, however, the **solutions remain analytical**.  
- Find the root of a degree 5+ polynomial **is no longer analytical**. Numerical solvers must be used.
- The matlab $\texttt{root(p)}$ function or python $\texttt{np.roots(coefficients)}$ functions are your best friend for degree 3+ polynomials

