# Week 4 Notes

## Binomial Distribution

$$
\begin{aligned}
P(x) &= P(X=x) = \big(_x ^n)p^x (1-p)^{n-x}, x=0,1,2,...,n \\
(a+b)^n &= \sum_{x=0}^{n} \big(_x ^n) a^x b^{n-x} \ BINOMIAL THEAROM \\
a + b &= 1, 0\leq a,b \leq 1 \ then \ we \ get \sum_{x=0}^{n} \big(_x ^n) a^xb^{n-x} = 1 \\
\end{aligned}
$$

* So the sum of binom. probs = 1

### Example 2.39

In a Group of 8 non-interacting speakers, the prob. that a speaker is active is $\frac{1}{3}$. Find the prob.that the number of active speakers is greater than 6.

let $X = active \ speaker$

$$
\begin{aligned}
P(X>6) &= P(X=7) + P(X=8) \\
&= \big(_7 ^8)(\frac{1}{3})^7(\frac{2/3})^1 + \big(_8 ^8)(\frac{1}{3})^8(\frac{2/3})^0 \\
&= 8 \times \frac{2}{3^8} + 1 \dot \frac{1}{3^8} \\
&= \frac{17}{3^8} \\
&= very \ small \ number
\end{aligned}
$$

## Multinomial Distribution

    Generalisation of Binomial

Let's suppose that the outcomes of a trial can be categorised into m groups, and the probability of falling into group $i$ is $p_i, i = 1,2,3,...,m \rightarrow \sum_{i=1 ^ m} p_i=1$.

If we perform n independent trials f, then $P(X_1=x_1, X_2=x_2,...,X_m = x_m) = \frac{n!}{x_1!x_2! ... x_m!}p_1^{x_1} p_2^{x2} ... p_m^{x_m}$

* Binomial Distribution is a Special Case of the Multinomial Distribution where $m=2, x_1=x, x_2=n-x, p_1 = p, p_2 = 1-p$

### Example 2.41

Dart is thrown at a target with 3 areas.

$$
\begin{aligned}
p_1 &= P(dart \ lands\ area \ 1) = 0.2 \\
p_2 &= P(dart \ lands\ area \ 2) = 0.3 \\
P_3 &= P(dart \ lands\ area \ 3) = 0.5
\end{aligned}
$$

## Tutorial

Suppose we conduct a series of independent Bernoulli trials each with success prob. p until a success occurs or the first time. 

Let $X= #$ trials needed to get first success

Then X is said to have the GEOMETRIC PROBABILITY FUNCTION

$$
\begin{aligned}
P_x(1) &= Pr(X=1) = P(S) = p \\
P_x(2) &= Pr(X=2) = P(FS) = (1-p) \times (p) \\
P_x(3) &= P(X=3) = P(FFS) = P(F) \times P(F) \times P(S) = (1-p)^2 p 
\end{aligned}
$$

The general case for this can be expressed as:

$$P_x(x) = P(X=x) = (1-p)^{x-1} p , x = 1,2,...$$

The sum of the $p_x(x)$ values over all allowable x values has to be 1 (otherwise p(x) is not a prob. function)

Therefor we need to show that $\sum_{x=1}^{\infty}(1-p)^{x-1} p = 1$ is true

PROOF:

$$
\begin{aligned}
LHS &= \sum_{x=1}^{\infty} (1-p)^{x-1} p = p \sum_{x=1}^{\infty} (1-p)^{x-1} = p[1 + (1-p) + (1-p)^2 +...]  \\
\end{aligned}
$$

The sum of an infinite geometric series with first term a and constant multiplying factor r $= \sum_{x=0}^{\infty} a r^x = \frac{a}{1-r} 0 \leq r <1$

What is the probability that more than K trials are needed to get first success?

$$\begin{aligned}
&= P(X=k+1) + P(X=k+2) +... \\
&= (1-p)^k p + (1-p)^{k+1} p + ... \\
\end{aligned}
$$

= Infinite Geometric Series with $a= (1-p)^k p, r= (1-p)$ therefor

$$
\begin{aligned}
= \frac{a}{1-r} &= \frac{(1-p)^k p}{1-(1-p)} \\
&= \frac{(1-p)^k p}{p} \\
&= (1-p)^k
\end{aligned}
$$

We often use $q=1-p$ which gives us $q^k$

