# Week 6 notes

## Example 3.19, Continued

$$
\begin{aligned}
n &= 48, p = \frac{1}{3} \\
X &= \# independent \ voice \ packets \ active \\
X & \sim Bin (n=48, p \frac{1}{3}) \\
m &= 20 = max \ \# \ packets \ which \ can \ be \ transmitted. \\
Let \ z &= \ discarded \ packets \\
z &= \big\{ _{0, X=0,1,2,..19,20} ^{X-20, X=21,22,..,48}  \\
\end{aligned}
$$


$$
\begin{aligned}
E(z) &= \sum_{all z} z \cdot P(Z=z) \\
&= 0 \cdot P(z=0) + \sum_{z=1}^{28}z \cdot P(X=z+20) \\

E(z) &= 0 \cdot \sum_{x=0}^{20} (_x ^{48}) \frac{1}{3}^x { \frac{2}{3}^{48-x} + \sum_{z=1}^{28} \cdot (_{z+20} ^{48}) (\frac{1}{3})^{2+20}) ({\frac{2}{3})^{28-z} \\
\end{aligned}
$$

## (POPULATION) VARIANCE OF A RANDOM VARIABLE

$$Var(X) = \sigma_x^2 = E[(x-\mu)^2]$$

* NOTE: whenever you see the equation $(X-\mu)^a$ is the 'ath' moment about the mean.

$$
\begin{aligned}
Var(X) & \geq \rightarrow E(X^2) \geq E^2(X)
\sigma_x &= std. \ Deviation of X = \sqrt{Var(x)}
\end{aligned}
$$

In DISCRETE case

$$
\begin{aligned}
\sigma_x^2 &= E[(X-\mu)^2] = E(X^2) - \mu^2 \\
&= \sum_{all x} (x-mu)^2p(x) = \sum_{all x} x^2 \cdot p(x) - \mu^2
\end{aligned}
$$

If $\sigma_x^2$ is Large, the dist of X is spread out, if $\sigma_x^2$ is small the dist of X is concentrated.

$E(x^k)$ is the kth MOMENT of X (about 0).

$E[(X-\mu)^k]$ is the kth MOMENT of X (about $\mu$)

$E(X^2)$ is the second MOMENT of X (about 0)

$Var(X)$ is the second MOMENT of X about its mean.

### Question

If a,b are constansts, what is $Var(aX + b)$? 

Multiplying the Random Variable X by constant 'a' will change its Variance, but adding constant b will not change the variance.

$$
\begin{aligned}
Var(aX + b) &= Var(aX) \\
&= a^2 Var(X)
\end{aligned}
$$


### Example 3.20

Coin tossed 3 times 

$$
\begin{aligned}
X &= \# \ H \\
E(X^2) &= 0^2 \cdot \frac{1}{8} + 1^2 \cdot \frac{3}{8} + 2^2 \cdot \frac{3}{8} + 3^2 \cdot \frac{1}{8} \\
    &= 0 + frac{3}{8} + \frac{12}{8} + \frac{9}{8} \\
    &= \frac{24}{8} \\
    &= 3 \\
Var(X) = E(X^2) - \mu^2 \\
    &= 3 - (\frac{3}{2})^2 \\
    &= 3 - \frac{9}{4} \\
Var(X) &= \frac{3}{4}
\end{aligned}
$$

A coin tossed 3 times has binomial distribution where n is the number of tosses and p is the probability that a toss will be successful (come up head)

$$X \sim Binomial(n=3, p=\frac{1}{2})$$

For a Binomial random variable the Variance can be ccalculated using

$$
Var(X) = np(1-p) = npq \\
if X \sim Bin(n,p)
$$

### Exampl 3.22

Variance of Geometric random variable with parameter p.

$$
\begin{aligned}
E(X) = Mean of X &= \frac{1}{p} \\
\frac{1}{(1-x)^2} &= \sum_{k=0}^{\infty} kx^{k-1} \rightarrow Diff. \ b.s \ w.r.t \ x \\
-2 \cdot -1 \cdot (1-x)^{-3} &= \sum_{k=0}^{\infty} k(k-1) x^{k-2} \\
let \ x = q \\
\frac{2}{(1-q)^3} = \sum_{k=0}^{infty} k(k-1)q^{k-2} \\
Mult. \ b.s \ by \ pq \\
\frac{2pq}{(1-q)^3} &= pq \sum_{k=0}^{\infty} k(k-1)q^{k-2} \\
    &= \sum_{k=0}^{\infty} k(k-1) p \cdot q \cdot q^{k-2} \\
    &= \sum_{k=0}^{\infty} k(k-1) p \cdot q^{k-1} \\
    &= \sum_{k=0}^{\infty} k^2 p \cdot q \cdot q^{k-2} - \sum_{k=0}^{\infty} k \cdot p \cdot q \cdot q^{k-2} \\
    &= \sum_{k=1}^{\infty} k^2 p \cdot q \cdot q^{k-2} - \sum_{k=1}^{\infty} k \cdot p \cdot q \cdot q^{k-2} \\
    &= \sum_{k=0}^{\infty} k^2 p P(X=k) - \sum_{k=0}^{\infty} k P(X=k) \ if X \sim Geom(p.) \\
    \therefore \frac{2pq}{(1-q)^3} &= E(X^2) - E(X) \\
    Since \ X \sim Geom(p), E(x) = \frac{1}{p} \\
    \Rightarrow E(X^2) &= \frac{2pq}{(1-q)^3} + \frac{1}{p} = \frac{2p(1-p)}{p^3} + \frac{1}{p} \\
    &= \frac{2(1-p)}{p^2} + \frac{1}{p} \\
    &= \frac{2-p}{p^2} \\
\end{aligned}
$$
$$
\begin{aligned}
Var(X) &= E(X^2) - \mu ^{2} \\
    &= \frac{2-p}{p^2} - \frac{1}{p^2} \\
    &= \frac{2-p-1}{p^2} \\
    &= \frac{1-p}{p^2} \\
    &= \frac{q}{p^2}
end{aligned}
$$

THe Mean of Geom(p) r.v is $\frac{1}{p}$. The Variance of Geom(p) r.v is $\frac{q}{p^2} = \frac{1}{p^2} - \frac{1}{p}$

## CONDITIONAL PROBABILITY FUNCTIONS

If X is discrete with prob. function $p_x(x)$, and if C is an event such that P(C) > 0, the the CONDITIONAL PROB. FUNCTION of X fiven C is 

$$P_x(X|C) = P(X=x|c)$$

$$
\begin{aligned}
P_x(X=x|c) &= \frac{P(X=x \cap C)}{P(C)} \\
    &= \Bigg\{ ^{0, if \ x=x \notin C} _{\frac{P(X=x)}{P(C)}, if \ X=x \in C}
\end{aligned}
$$

### Example 3.24

X is time to transit a message, X is uniform on $\{ 1,2,..., L \}$ Suppose the message has already been transmitting for m time units. What is the prob. that the remaining transmission time is j time units.

$$
\begin{aligned}
\rightarrow & X>m \\
\end{aligned}
$$

$$
\begin{aligned}
P(X = m+j)|X>m) = \{ ^{\frac{1}{L-m}, m+j = m+1,m+2,...,L \ j=,1,2,..,L-m} _{0, otherwise}
\end{aligned}
$$

$$P_X(x) = \sum_{i=1}^{n} P_X(x|Bi) P(B_i)$$

### Example 3.25 - Device Lifetimes

* Type 1 Device occur with prob. $\alpha$, have geometric lifetimes with parameter r

* Type 2 Device occur with prob. $1-\alpha$, have geometric lifetimes with parameter s.

$$
\begin{aligned}
P_{X|B1}(x) &= (1-r)^{x-1} \cdot r, x= 1,2,... \\
P_{X|B2}(x) &= (1-s)^{x-1} \cdot s, x=1,2,... \\
P_X(x) &= P(X=x) \sum_{i=1}^2 P_X(x|B_i) \cdot P(B_i) \\
&= P_X(x|B_1) \cdot P(B_1) + P_X(x|B_2) \cdot P(B_2) \\
&= (1-r)^{x-1} \cdot r \cdot \alpha + (1-s)^{x-1} \cdot s \cdot (1-\alpha)
\end{aligned}
$$

