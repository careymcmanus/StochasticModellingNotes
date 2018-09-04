# Week 1 notes 

Rel freq = Fraction of times ann outcome (or event) occurs

if $f_n = \#$ 
times an outcome occurs in n experimental trials, then 
$Rel.Freq = \frac{f_n}{n}$ 

e.g. Suppose we toss a fair coin n times and count how many times h appears the plot Rel. Freq. vs n

Relative Frequency is bounded by 0 and 1 ie.

$$ 0 \leq Rel.Freq \leq 1$$

In this example Rel.Freq is highly variable in the initial few throws but very quickly settles down to an approximation of a horizontal line. If the coin is a fair coin ie $P(head) = 0.5$ then the rel.freq with settle down at approximately $0.5$ if the probability of heads was different then the rel freq would settle down at that.

Probability === long-run Relative Frequency

$$Pr(H) = \lim_{n\rightarrow \infty} Rel.Freq_n = \frac{1}{2}$$

An Event is any combination of elementary outcomes. Capital letters are often to denote events

eg. A = tails appears on one toss of coin = {T}

B = A number greater than 4 appears on a dice roll = {5, 6}
`
C = At least one H appears in two tosses of a coin = {HT, TH, HH}

$$
\begin{aligned}
Pr(A) &= Pr(T) \\
Pr(B) &= Pr(5 or 6) = Pr(5) + Pr(6) \\
Pr(C) &= Pr(HT \ or \ HH \ or \ TH ) = Pr(HT) + Pr(HH) + Pr(TH)
\end{aligned}
$$

* this is only the case because 5 and 6 (and HT,HH,TH) are E.O and so __Mutually Exclusive__

* Two events are sais to be mutually exclusive if they have no elementary outcomes in common.

For Mutually Exclusive events:

$$Pr(D \cup E) = Pr(D \ or \ E \ or \ both) = Pr(D) + Pr(E)$$

For non mutually exclusive events:

$$Pr(D \cup E) = Pr(D \ or \ E or \ both) = Pr(D) + Pr(E) - Pr(D \cap E)$$

* The formula for the non mutually exclusive events is the general formula due to the probability of the Probability of the intersection between two mutually exclusive events is zero 

In General:

$$
\begin{aligned}
P(A \cup B) &= P(A) + P(B) - P(A \cap B) 
\end{aligned}
$$

## Lecture

$$
\begin{aligned}
P(A \cup B) & = P(A) + P(B) - P(A\cap B) \\
P(A \cap B) &= 0 \leftrightarrow A,B \ are \ mutually \ exclusive
\end{aligned}
$$
Mutually exclusive is NOT the same as Independent

### Axioms of Probability

$$
\begin{aligned} 
0 \leq P(A) &\leq 1 \\
P(S) &= 1 \\
P(A) + P(\bar{A}) &= 1, where \ \bar{a} = A^c \ is \ the \ event \ "A \ does \ NOT \ happen" \\
\therefore P(\bar{A}) & = 1 - P(A)
\end{aligned}
$$

Suppose we do an experiment n times and each time, we observe the value of a RANDOM VARIABLE, say X

$$\bar{X}_n = \frac{X_1 + X_2 +... + X_n}{n} = \frac{\sum_{i=1}^n X_i}{n} = SAMPLE \ MEAN$$

* NOTE: Sample Mean is different from the population mean, sample mean is the mean of n samples where as the population mean is the mean of $\infty$ samples. 

$$
\begin{aligned}
1 + 2 + 3 + 4 + .... + n-1 + n &= \sum_{x=1}^n x \\
n + (n-1) + (n-2) + (n-3) + .... + 2 + 1 &= \sum_{x=1}^n x \\
(n+1) + (n+1) + (n+1) + (n+1) + .... + (n+1) + (n+1) &= 2 \sum_{x=1}^n x \\
\rightarrow n(n+1) & = 2 \sum_{x=1}^n x \\
\sum_{x=1}^n x &= \frac{n(n+1)}{2}
\end{aligned}
$$


### Discrete Sample Spaces

Elements can be listed (separated by commas)

- e.g. {HH, HT, TH, TT}, {1,2,3,4,5,6},{0,1,2,3,...} $=>$ Countably Infinite

### Continuous Sample Space

Doesn't make sense (or it is impossible) to list the elements - Need to describe S using intervals

- e.g Temperature in a room, heights, ....

$$ 
\begin{aligned}
S &= {x: -273.15 \leq x \leq 100} \rightarrow Temperature \\
S &= {x: x \geq 0} \\
\end{aligned}
$$

#### Examples
1. Toss coin 3 times, note # heads
    - $S = \{0, 1, 2, 3 \}$

2. Pick a random number b/w 0 and 1
    - $S = \{x:0\leq x \leq 1 \}$

### Empty Set

$$
\begin{aligned}
\emptyset &= \{ \} \\
P(\emptyset) &= 0 \\
\emptyset &= S^c \\
P(\emptyset) &= 1-P(S) \\
&= 1 -1 \\
&= 0
\end{aligned}
$$

### Other Notation

* $x \in A$ "x is an element of the set A"
* $A \subset B$ "A is a subset of B"
* $A \subseteq B$ "A is a subset of B or identical to B"

### Properties

* De Morgan

$$
\begin{aligned}
(A \cup B)^c &= A^c \cap B^c \\
(A \cap B)^c &= A^c \cup B^c
\end{aligned}
$$  

$$
\begin{aligned}
P(\cup_{k=1}^{\infty}A_k) = \sum_{k=1}^{\infty} P(A_k)
\end{aligned}
$$

## Friday Tut

Example 2.10
* Coin tossed 3 times
    * $S = \{HHH, THH, HTH,HHT,TTH,THT,HTT,TTT\}$
    * $P(2 heads in 3 tosses) = \frac{3}{8} = P(THH)+P(HTH)+P(HHT)$
        * The answer is only true if the coin is fair if isn't then the probability will still be the sum of P(2 heads in 3 toss)
    * $P(at least 2 heads) = \frac{1}{2}$
    * $P(at least 2 tails) = 1 - P(at least 2 heads)$

    * if $P(H) = \frac{3}{4}, P(T)= \frac{1}{4}$ what is P(at least 2 tails)
        * $P(TTH) + P(THT) + P(HTT) + P(TTT) = \frac{3}{64} + \frac{3}{64} + \frac{3}{64} + \frac{1}{64} = \frac{5}{32}$
    
    * We have also assumed that the individual tosses are INDEPENDENT of each other.

### Counting Methods

The number of distinct ordered k-tuples $(x_1,x_2,...,x_k)$ with components x from a set with $n_i$ distinct elements is $\prod_{i=1}^{k} n_i$

* e.g multiple choice test with k questions, such that $Q_1$ has $n_1$ possible answers and $Q_k$ has $n_k$ possible answers

e.g if:

$$
\begin{aligned}
k = 6, n = 4, n_2 = 7, n_3 &=v2 , n_4 =5, n_5 = 3, n_6 = 3 \\
possibilities = 4 * 7*2*5*3*3 &= 2520
\end{aligned}
$$

Sampling with replacement and ordering

* Choosing k objects from n distinct objects, with replacement
    * ie. select object, note what it is, then replace it, select again, ....
    * The number of ordered k-tuples $(x_1, x_2, ..., x_k)$ is $n^k$
